---
layout: post
title: "Effect JAVA Language"
---
I read this book Chinese editon two years ago when I was a intern. But to be honest saying, I already forget it very clearly.

In serveral months ago, I bouguht the **[effective java](http://www.amazon.com/Effective-Java-2nd-Joshua-Bloch/dp/0321356683)**, but due to the time limit or personal issue, I only touch it a little times, and it still looks so white.

So now, I will use my blog to recode every items to help me better understanding the real spirit of this book.

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
No more need to be mentioned here.

###Item 3 Enforce the singleton property with a private constructor or an enum type

In normal case, we always create the singtlon pattern using the following way:

    pubilc class Demo {
        private static final Demo INSTANCE = new Demo();
        private Demo(){}
        public Demo getInstance(){return INSTANCE)}
	}
This is good and easy to understand. But in some extreme case, this one can not keep strict singleton.

In this book, the second way was created, uging `enum`

    public enum Demo{
        INSTANCE;

    public void dosometing(){}
    }

This way can keep 'absolute' singleton even in the serization.

###Item 4: Enforce noninstantiability with a private constuctor
In the utils classes, we can proivde a private constuctor to avoide instantiability.

###Item 5: Avoid creating unnecessary objects
For exmaple: `String s = new String("abc")` vs `String s = "abc"`. Which one is better?

###Item 6: Eliminate obsolete object references
"The best way to eliminate an obsolete object reference is to let the variable that contained the reference fall out of scope"

Another solution: Try to set the obsolete obj to null is a exception solution.

###Item 7: Avoid finalizers
Just one thing need to be noticed here, in most of cases, dont using the finalizers.

###Item 8: Override equals

###Item 9: Override hashcode

###Item 10: Override toString

###Item 11: Override clone
Notice: **copy && deep copy**

###Item 12: Consider implementing Comparable
 