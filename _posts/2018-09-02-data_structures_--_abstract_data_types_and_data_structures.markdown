---
layout: post
title:      "Data Structures -- Abstract Data Types and Data Structures"
date:       2018-09-02 21:44:24 -0400
permalink:  data_structures_--_abstract_data_types_and_data_structures
---

While learning how computers process data and, ultimately, organize memory, I've continued to face a lot of names for things or functionality that sound confusingly similar. Many concepts have sounded weirdly similar and the differences appearing as the least important of nuances can actually be completely different... the computational equivalent of "they're, their and there", no similarity but sound.

The simplest explanation I've found is from StackExchange, 'ADT is to an interface (what it does) what a data structure is to a class (how it does it)', but this only gives us an appearance, again. With this, I think the imporant take away is that they are not mutually exclusive.

We've looked at data structures in my [last post](http://jordan-kline.com/data_structures_--_from_linked_list_to_heap), which looked at lists & linked lists. A linked list has methods that describe its shape and how we interact with it, but generally, does not give any information about what is happening under the hood. This is the basis of abstraction.

We can think about a data structure as the physical implementation of a data type. It is a concretized version of an association of data. 

ADTs are the idea of how the data is organized, the shape and the functionality without implementation... a way of presenting this information. ADTs don't have a relation to the specific features of a computer language; they are the 'the mathematical model of the data objects that make up a data type as well as the functions that operate on these objects'. ([Wikipedia](https://en.wikipedia.org/wiki/Abstract_data_type))

And this means what exactly?

Well, it's imporant to understand how and why we discuss these things and what exactly they mean in common parlance. When I have been asked in the past how to implement a queue or a stack, I have also asked what data structure this should be implemented with. That is still confusing to me because the languages that I have learned so far have some impact on how ADTs are implemented. In JS, you can implement a stack or a queue with an Array, but other languages have concrete data structures that can handle them better.

More experience, more practice and a deeper understanding of what common data structures exist and why they are used, as well as the efficiency that comes along with using specific ADTs for specific tasks, but I've found that understanding the fundamental difference between the two will help prevent asking stupid questions during algorithm challenges and in general working with teams. It's most often the nuances that I make mistakes with confidently, never knowing they are mistakes.
