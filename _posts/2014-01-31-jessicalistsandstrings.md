---
layout: post
author: jskaa
title: Jessica's Lists and Strings Exercises
---

#Strings

###Write a function that reverses its string argument. 

We went over this question in class. I also looked up extended slicing, and found that by omitting a beginning and end in the ```[begin:end:step]``` , by omitting a beginning and end while specifying a step of -1, it will reverse the string. 

My code was:

```
from test import testEqual

def reverse(astring):
    bstring = astring[::-1]
    return bstring

testEqual(reverse("happy"), "yppah")
testEqual(reverse("Python"), "nohtyP")
testEqual(reverse(""),"")

```

the output was:

```
Pass
Pass
Pass

```
