---
layout      : post
title       : A Utility Class for Getting JDBC Connection with MySQL
description : A utility class for getting JDBC connection with MySQL
category    : daily
tags        : [jdbc, mysql, daily]
---
{% include JB/setup %}

Most Java developers had experience to develop database program using JDBC, so am I. Although there are lots of sophisticated and powerful frameworks, such as Hibernate, iBatis, JPA, and so force, used to make database programming easier and more professional, deeply understanding JDBC programming is required, in particular to the new comer.

Getting JDBC connection is an essential step before making any query to database. This step involves many important issues as shown below:

1. Setting database parameters and avoiding hard-code.
2. Make sure the connection of database is closed after invoking connection.close().
3. When getting a connection, how long will be taken?

For the first issue, i recommend using outside properties file to store database parameters, which is named database.properties, for example, and the content could be:

{% highlight java linenos %}

// mysql database configuration  
driver=com.mysql.jdbc.Driver  
url=jdbc:mysql://localhost:3306/dbname  
user=user  
password=password  

{% endhighlight %}

And then, a static block can be used to load database parameters and driver class as follow:

{% highlight java linenos %}

// properties object used to load database parameters  
private static Properties prop = new Properties();  

static{  
    try{  
    prop.load(new FileInputStream(PROPERTY_FILE_NAME));// database.properties  
    Class.forName(prop.getProperty(DRIVER)); // driver  
    }...
}

{% endhighlight %}

As the relevant parameters had been loaded into prop object, including username and password, therefore, the connection can be got with the following statement:

{% highlight java linenos %}

DriverManager.getConnection(prop.getProperty(URL), prop);  

{% endhighlight %}

For the second problem, we can examine the number of connection after closing specific connection using MySQL command:

{% highlight java linenos %}

SHOW STATUS LIKE 'Threads_connected';  

{% endhighlight %}

It is very clear to show the number of connection to the database at any moment.

For the last question, it is no doubt the performance of using connection pool is better than not. I think it should be no solution without using connection pool in real, industrial system. Therefore, I just show a small snippet code using AspectJ to profile method getConnection() of class JDBCUtil which is simple util class I defined for getting database connection and clear up relevant resources.

{% highlight java linenos %}

public aspect GetDBConnectionProfillingAspect  {  
    pointcut getConnectionOperation() : execution(* JDBCUtil.getConnection(..));  

    Connection around() : getConnectionOperation()  {  
        long startTime = System.currentTimeMillis();  

        Connection obj = proceed();  

        long endTime = System.currentTimeMillis();  

        System.out.println(thisJoinPointStaticPart.getSignature() + " took "
        + (endTime - startTime) + " nanoseconds.");  

        return obj;  
    }  
}

{% endhighlight %}

The results clearly show that the time of getting one connection is nearly 20 nanoseconds expect the first one. The reason is it is needed to execute static block for the first time which may take more than 400 nanoseconds.

All right, that is all of what i want to show you~ good night!
