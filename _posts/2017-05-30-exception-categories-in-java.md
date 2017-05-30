---
layout      : post
title       : Two Categories of Java Exception
description : An appropriate sentence of describing two categories of Java Exception
category    : daily
tags        : [jdk, daily]
---
{% include JB/setup %}

Just now, I read an appropriate sentence used to describing Java Exception in terms of its two categories, which is shown as follows:

**"Java specifies two categories of exceptions that a method may throw: checked and unchecked. When an exception is checked, the callers must deal with it either by catching the exception or by declaring that they can throw it. When an exception is unchecked(which directly or indirectly extends RuntimeException or Error), callers need not to deal with it explicitly and the exception is automatically propagated up the call stack"** (AspectJ in Action, second edition, 2010)
