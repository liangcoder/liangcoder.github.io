---
layout      : post
title       : Yosemite Upgrade and Install JDK
description : install jdk6 on the yosemite
category    : daily
tags        : [yosemite, jdk, daily]
---
{% include JB/setup %}

Today, 2014-11-01, I upgraded the Mac OS X Yosemite which version is 10.10. However, I found that the jdk6 installed in the past is missing without any warning.

Only jdk7 is presented, the home path of which is

> "/Library/Java/JavaVirtualMachines/jdk1.7.0_60.jdk/Contents/Home
>

Because of the legacy system, jdk6 is required. To be honest, it's really difficult to find a jdk version for the mac os x, especially for a Java developer. Oracle and Apple!

Finally, I made it, the jdk6 for mac os x can be downloaded in the following address:

> [Java for OS X 2014-001](http://support.apple.com/kb/DL1572?viewlocale=en_US&locale=en_US "Java for OS X 2014-001")
>
> "http://support.apple.com/kb/DL1572?viewlocale=en_US&locale=en_US"
>

I do not know why it is labelled with "...2014-001", there is no related at all to the jkd6.

After installation, jdk6 home can be found in the following path:

> "/System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
>

Notice that, the path of jdk7 home begins with "/Library/Java/", however, the jdk6 home is "/System/Library/Java/". It's really a bad example of the consistency.
