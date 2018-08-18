---
layout: post
title:      "Static Typing in Dynamically Typed Languages"
date:       2018-08-18 18:20:57 +0000
permalink:  static_typing_in_dynamically_typed_languages
---

As languages have become further abstracted and capable of performing more abstract control over certain data flow and memory maintenance, the strict requirements of choosing which type of data is to be stored and accessed in memory have become an afterthought for most people who are new to programming.

I recall, well over a decade now, studying C++ as a first language these, as long as the painful level of patience required to deal with compiling times, were one of the hardest hurdles to overcome. To be obvious, this instant gratification, instant response cycle of REPLs and console programs that provide instant feedback is likely why I, and most of the people who are approaching this deluge of coders coming to meet the continuing demand, is a major factor to overcoming that frustration.

## What are data types?

In Javascript, there are 7 data types, readable/writable data with associated truthy-falsy values, associated with each, including 6 'primitive' values and the all-encompassing 'Object'.

### Primitives:

Boolean which has two possible, opposite values: true or false.
Null is the specified absence of any value.
Number encompasses both 'float' and 'integer', as most other languages would distinguish, and uses 'the double-precision 64-bit binary format IEEE 754 value', which is rather less precise than the name would have believe.
Undefined is the value held by a variable before it receives a value.
String includes all '16-bit unsigned integer values' in an indexed set.
Symbol is a key used for an object property when the property is internally used and private.

### Object:

Objects resemble real world things and are the 'cell-structure' of Object oriented programming. They can encompass simple hashes that hold primitive values with key-symbols, or they can hold functions that can be accessed as methods by calling their key.

## What selects a variable type and why do we worry about this?

Javascript is one of the 'looser' languages with regard to typing. From ES2015, the 'let' and 'const' variables have changed the way that hoisting and scope works in a way that give coders more control of the immediate effect and future mutations than the pre-ES2015 'var'. Understanding this variation, when a variable is defined, it holds a space in memory, and then receives a value, of one of the above types. 

In vanilla JS, the V8 engine decides the type, which is especially confusing with JS coercion of integers to strings. So, what happens when V8 decides a type that isn't desired? Generally, an error will be thrown or you'll receive bad data. Neither of those, in a production runtime environment is acceptable. This is especially true in large documents and spaghetti coded codebases & monoliths.

Along with errors, dynamically typed, interpreted languages suffer from performance issues in comparison to strictly typed language where memory is specifically allocated, improving efficiency and allowing for less ambiguity (necessary buffer) in memory maintenance.

## What can be done to address this and who needs it?

Some language modifications have brought strict-ish typing into the language and some internal, native modifications have been made recently to allow JS to compete in this realm of speed optimization and typing to improve code reliability and aid DevOps work.

A recent addition to JS in ES2017 is the introduction of static arrays that can have a specific buffer size added to them. It's not something that most people will use, but for game developers and people who need extreme levels of efficiency and predictability for memory, it's a step in a direction to compete better with languages like C# that currently dominate. Another language, TypeScript, is compiled to JS and has all of its features, but adds strict typing for robustness on larger projects, which can suffer from tedious debugging with no express errors on certain failures.

Typing is something that I am trying to understand better because, although it's understood that abstraction away from explicit instruction in code is usually related to a decline in performance to some degree or another. I do not intend on bringing strict typing into my immediate workflow, but I think understanding the possible benefits of typing is something that being aware of will help to see the limitations in your own code and eventually learn to need the things that you haven't seen need for previously.


Source & Further Reading: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management
