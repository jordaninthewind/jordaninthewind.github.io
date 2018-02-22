---
layout: post
title:      "Original Sinatra"
date:       2018-02-22 21:43:31 +0000
permalink:  original_sinatra
---

It's not an easy task to find something original in this world where every possibility seems to be being made reality, more readily every day.

So, with the breadth in modularity in MVC as a concept, I wanted to make something that people could use locally and adapt to their needs.

This turned out harder than expected.

My first idea has been largely what I've stuck with since starting; an application to let people communicate resources available, so that people nearby might find use of them. It happens to me often that I buy too much of something in bulk and it goes bad before I'm able to use it. It also happens that I need a stick of butter at the last minute while cooking or something similarly trivial.

This is where I started and it grew into a complicated mess very quickly. Trying to find an MVP, I decided to make it rather a place where people would be able to add items that they have, give them a quantity and then allow people to comment and make a connection through that.

To develop it further, in the future, I will likely add the ability to have these expire relative to an ActiveRecord timestamp and to allow some automatic garbage collection to avoid orphan or unnecessary date.

The app has three classes that interact, a User which has many Items, Items that have many Comments and belong to Users and Comments that belong to Items and Users. The last bit has been the hardest part in trying to make a reasonably effortless interaction between classes as the logic became difficult to handle.


