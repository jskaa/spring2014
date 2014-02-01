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

###Write a function that removes the first occurrence of a string from another string.

This one was a little tricky to figure out, and I took a peek at the provided answer tab to give myself a hint in what direction I should go. I saw immediately that they used slicing and concatenation together, and I went back to my console to work. What I found was that I could use the ```.index()``` method to find the first occurrence of a parameter (substring) within a string. The index was saved as the variable ```index```, and used in slicing to find the letters in the input string up until but not including the index (which is the substring we want to remove!). The next step was to get rid of the full substring. But what if it was more than a single character? This is where the ```len(substring)``` came in, as when added to the index, it would give an index of where the full substring ended. Then, it was a simple matter of using this as the starting point of the slice, and concatenating it onto the end of the previous portion. 

My code was:

```
from test import testEqual

def remove(substring,inputstring):
    index = inputstring.index(substring)
    if index < 0: 
        return inputstring
    return inputstring[:index] + inputstring[index+len(substring):]

print remove('on', 'Fonzy') 
print remove('water', 'waterbottle')
testEqual(remove('an', 'banana'),'bana')
testEqual(remove('cyc', 'bicycle'), 'bile')
testEqual(remove('iss', 'Mississippi'), 'Missippi')
testEqual(remove('egg', 'bicycle'), 'bicycle')
```

The output was: 

```
Fzy
bottle
Pass
Pass
Pass
```

###Write a function that removes all occurrences of a string from another string

At first, i was trying to edit my code from the previous question in order to answer this. However, after looking online, I found a ```.replace()``` method, which seemed MUCH easier to use. Using ```.replace()```, I could just "replace" all of the substring occurrenes with a blank string, essentially 'deleting' them. 

My code was:

```
from test import testEqual

def remove_all(substring,inputstring):
    remove_substring = inputstring.replace(substring, "")
    return remove_substring

print remove_all("app","snappappappi")
print remove_all("foo","snoofoobloofookoofoo")
testEqual(remove_all('an', 'banana'), 'ba')
testEqual(remove_all('cyc', 'bicycle'), 'bile')
testEqual(remove_all('iss', 'Mississippi'), 'Mippi')
testEqual(remove_all('eggs', 'bicycle'), 'bicycle')
```

The output was:

```
sni
snooblookoo
Pass
Pass
Pass
Pass
```

#Lists

###Write a function to count how many odd numbers are in a list.

I knew I needed to use the modulo operator in my code. Once I saw down and wrote out the steps for myself, it was fairly simple to fill in the steps with actual code. 

My code was: 

```
def count_odd(list):
    odd_count = 0
    for i in list:
        if i % 2 ==1:
            odd_count += 1
    return odd_count

print (count_odd([5,8,9,3,1,44,45])) 
print (count_odd([2,4,6,8,10]))
```

The output was:
```
5
0
```


