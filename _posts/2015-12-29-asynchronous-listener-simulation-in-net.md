---
layout: post
title: Asynchronous Listener Simulation In .Net
tags: [software_engineering]
cover-img: "/assets/img/SE_header.png"
---
Today I had a discussion about how one would implement a program that listens to some input (typically in a high frequency text message scenario), stores that input and asynchronously consumes elements from the message queue with some business logic behind the consumption. This program would be implemented in C# with .Net.
The problem sounded interesting so I took a shot at writing a simulated example, which implements the required behavior and displays live stats (received, consumed, and total message counts).

The interesting bits are mainly the use of the **Task.Run()** method to run asynchronous code, the use of a thread-safe **ConcurrentCollection** , and finally the use of a static long counter accessed concurrently by the receive and consume threads, through the thread-safe **Interlocked.Increment()** and **Interlocked.Read()** methods used respectively to increment and read the counter. This could be a nice introduction to asynchronous programming with C# and .Net.

The code can be found in the following [GitHub repo](https://github.com/YazidHamdi/AsynchronousListener).

Feedback appreciated:)