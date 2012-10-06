---
layout: post
title: "Effect JAVA Language"
---
I read this book Chinese editon two years ago and can not understand all of the meaning of this book due to the translate issue and my personal skill issue.

In serveral months ago, I bouguht the **[effective java](http://www.amazon.com/Effective-Java-2nd-Joshua-Bloch/dp/0321356683)**, but due to the time limit or personal issue, I only touch it a little times, and it still looks so white.

Next, I will use my blog to recode every items to help me better understanding the real spirit of this book.

###Item 1 Consider the static factory method instread of constructor

####What is the advatage of static factory method?    
1.Unlike constructors, it have concrect names.    
2.Dont need to create new object every time.    
3.Can return a subtype of thier return type.
4.Reduce the verbosity of creating parameterized type instances.

####Like the coin has two sides, the disadvantage is: 

1.No public/protected contructor but only proivde static factory methods can not be subclassed.    
2.The factory methods looks the same with other static methods.

###Item 2 Consider a build pattern when faced many constructor parameters