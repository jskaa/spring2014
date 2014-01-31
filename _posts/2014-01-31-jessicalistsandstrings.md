---
layout: post
author: jskaa
title: Jessica's Lists and Strings Exercises
---

#Strings

###Write a function that reverses its string argument

We went over this question in class. I also looked up extended slicing, and found that by omitting a beginning and end in the ```[begin:end:step]``` , by omitting a beginning and end while specifying a step of -1, it will reverse the string. 

My code was:

```
def reverse(astring):
    bstring = astring[::-1]
    return bstring

print reverse("Pretzel")
print reverse("Fonzy")
print reverse("Mike")
```

The output was:

```
lezterP
yznoF
ekiM
```

###Write a function that mirrors its argument

This was the exact same as the last question, but wanted us to concatenate the reverse onto the end of the original string. Doing so was incredibly easy, as it just needed me to make a small tweak by adding the reversed string onto the end of the original.

My code was:

```
def reverse(astring):
    bstring = astring[::-1]
    return astring+bstring

print reverse("Pretzel")
print reverse("Fonzy")
print reverse("Mike")
```

The output was: 

```
PretzellezterP
FonzyyznoF
MikeekiM
```


