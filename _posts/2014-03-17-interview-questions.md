---
layout: post
title: Interview Questions
categories: Tech
tags: interview
---

DAY1：
===

1. double 的存储与计算都会丢失精度
2. 字符流与字节流

  流分类： 
  1.Java的字节流 
   InputStream是所有字节输入流的祖先，而OutputStream是所有字节输出流的祖先。 
  2.Java的字符流 
  
  [JavaIO](http://www.cnblogs.com/lich/tag/java%20IO/)
  
  Reader是所有读取字符串输入流的祖先，而writer是所有输出字符串的祖先。 
  InputStream，OutputStream,Reader,writer都是抽象类。所以不能直接new  


  字节流在操作的时候本身是不会用到缓冲区（内存）的，是与文件本身直接操作的，而字符流在操作的时候是使用到缓冲区的

  字节流在操作文件时，即使不关闭资源（close方法），文件也能输出，但是如果字符流不使用close方法的话，则不会输出任何内容，说明字符流用的是缓冲区，并且可以使用flush方法强制进行刷新缓冲区，这时才能在不close的情况下输出内容


3. Exception与Error

    Exceptions 
    
    1．可以是 可被控制(checked) 或 不可控制的(unchecked) 
    
    2．表示一个由程序员导致的错误 
    
    3．应该在应用程序级被处理 
    
    
    
    Errors 
    
    1．总是 不可控制的(unchecked) 
    
    2．经常用来用于表示系统错误或低层资源的错误 
    
    3．如何可能的话，应该在系统级被捕捉 


4. synchronized this 与 带码块， 线程状态， wait 与 sleep

  [link](http://www.cnblogs.com/GnagWang/archive/2011/02/27/1966606.html)
 

5. List与Set， TreeSet与HashSet
  List

  Is an Ordered grouping of elements.
  List is used to collection of elements with duplicates.
  New methods are defined inside List interface.
  Set
  
  Is an Unordered grouping of elements.
  Set is used to collection of elements without duplicates.
  No new methods are defined inside Set interface, so we have to use Collection interface methods only with Set   subclasses. 

