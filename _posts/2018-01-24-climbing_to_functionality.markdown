---
layout: post
title:      "CLImbing to Functionality"
date:       2018-01-24 21:25:21 +0000
permalink:  climbing_to_functionality
---


Working on my first actual, functioning program. Seeing this gem from start to finish (and still leaving space for the ability to grow and further work out kinks and develop features and all the rest) has been one of the most serious steps that I've taken toward programming yet.

Ironing out understanding and realizing the practicality of bits of wisdom that have been included in each lecture I've followed is a task unto itself; I've spent a good deal of time in my life learning to learn and the patience that is required to go back, redouble effort, consider things from another perspective and then implement them in a way that is completely different than how it sounded the first time it encountered your brain is an art and a reassuring effort in consistency and dedication.

The 'culmination' of vanilla OO Ruby in this curriculum made me go back and watch lectures that I'd watched 5 times before and watch them again and learn to put this together in my own way. There is no clear way to finish a project, but after winding myself in knots a couple of times, I can say that there is a very clear way to start a project.

Starting a project requires a programmer to have an idea of functionality that they would like to see by the end of the first version and a framework of functions that can be abstracted into interacting classes. The most important lesson that I took away from watching people make their programs and having my brain in my own code is that making a brief functioning mock-up of interactivity without any deeper information being developed until afterward helps you start simply, in a way that isolates the programs functioning from logic behind the functions.

It is not easy to wire up these documents so that they can communicate, and understanding the flow of information within a gem is now the most salient takeaway from this lesson. Where does a program start, where does it flow through for finding information and where does it end when you need a bit of information returned to the user.

Though there are many ways to do this, I understand better why there is a wrong way to go about this. Tracing a complicated document is frustrating at best and aggravating to a really undesirable point. I found myself, after starting badly, wanting to completely start over. Again, frustrating, but not everything is lost in this. To start a program from scratch is as easy as rebooting a computer or deleting a file, but not all of the effort is wasted, not everything is meaningless.

The time spent in finding CSS selectors that work, the time in control flow that helped to clarify, in my sandbox, what functionality I actually wanted out of this program, things that helped me to understand the way that it fits in with all of the experiences I've had in my life as a user -- nothing is lost except a first draft. You can't have a climb without CLI... okay, that was not funny, but it's a mountain you go up, on a hike, at this point enjoying the view and gleaning as much as you can in order to, hopefully, see things that you haven't noticed before.


That's enrichment -- growth -- it's learning, at it's most fundamental.


In more specific terms, my CLI project was just a slight exploitation of my obsession with Reddit and learning. A simple program that pulls data from the front page of reddit, allows you to open pages, view votes and subreddits. It started simple and has developed a bit more into being able to open specific subreddits and reload information.

One of the main pitfalls has been in avoiding Reddit's API and just trying to hit their servers with Open-URI. It's resulted in completely unpredictable 429 errors and it will be addressed while I continue to develop this as I learn more -- the next steps are going to be to either grab the information through their API, or make a rescue that will cause the application to not simply fail.

Refactoring is life, it's not finished and I imagine there will be edits to this blog post. I am quite pleased with the way that this entire effort helped me to understand the underlying structure of a Gem, to better realize how the class - OO structure functions in practice and to have more experience working within bash, being able to give system commands directly through Ruby.
