---
layout: post
title:      "Data Structures -- From Linked List to Heap"
date:       2018-08-26 22:55:31 +0000
permalink:  data_structures_--_from_linked_list_to_heap
---

A data structure is a way of organizing data in a storage format that enables efficient access and modification.

To some degree, this builds immediately on my last post which covered data types. Types of data, to reiterate, can be from the 'primitive' realm or can be of an object realm within Javascript. A data structure, in contrast with primitives, will be a way that data is organized or, better, connected.

Most people who have some experience with programming can identify common data structures like an array, which holds values organized by indices and has associated methods to manipulate the data. In Javascript, an Array is a type of hash which has key value pairs in which the keys are numeric and sorted from 0 to the length of the associated memory space.

From array, we usually begin to look at hashes as a data structure of their own, which changes in that the order of the key is accessed and stored. In some computer languages that have a closer connection to manual data manipulation, we can see that this association works in referencing an exact place in memory, which holds a value. The place in memory is accessed by the key. (See hash tables)

So, with these basic data structures, we have a foundation for understanding the basics of how data can be stored, but we lack the 'why' and the 'how', as well as the 'what else'.

In brief, this is an intro into a project that I am going to undertake in explaining certain data types and their applications and benefits. It's a work in progress because I am working to understand better optimization and efficiency so that I can improve my own code and my own understanding of CS theory and best practices.

From Linked List starts us at a 'list', which according to Wikipedia, 'in computer science, a linked list is a linear collection of data elements, whose order is not given by their physical placement in memory. '

Linked lists, in contrast with arrays, are bits of memory that normally store a value and a pointer that points to another linked list. Something like the below:

![](https://en.wikipedia.org/wiki/Linked_list#/media/File:Singly-linked-list.svg)

This is a 'singly linked list', which points in one direction, to the linked list that follows. If you are on a linked list, the start being called the 'head' and the end being called the 'tail', you have only the value and the pointer to the location of the next linked list. This is in contrast with 'doubly linked lists' which have a pointer to the previous value, being null at the head, and to the next value, being null at the tail.

### What are some of the implementations of a linked list?

If you can use a web browser, you have used a linked list. Linked lists can hold the value, in order, of a previous page that you have visited. This is a bit of data that is connected relative to the time that it was added, in similarity with a stack, which can be used to perform a similar function in a particular order.

### What are the benefits of using a linked list?

Again, the above idea of pushing and popping or splice into an array is fine, but in terms of efficiency, a variety of data structures give more control over how quickly a task can be performed.

Considering a linked list, there is no way to find a value because the linked list values are only connected through a linear relationship. Whereas, in JS, we can query a value in the array using <.includes()> or something similar, but in a linked list, the list must be iterated over until a value is found. This is O(n), but not particularly efficient because *every* value must be iterated over. What can you do if you have a million values? This is unreasonably ineffient.

In contrast, however, to replace a value when the location in memory is known for a linked list is as simple as updating the next value of the previous node (and the previous value of the next node in the case of a doubly linked list) and updating each respective pointer of the new node to those nodes.

This should be updated with more info as I continue to implement and get better with linked lists.
