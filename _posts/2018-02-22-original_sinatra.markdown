---
layout: post
title:      "Original Sinatra"
date:       2018-02-22 16:43:32 -0500
permalink:  original_sinatra
---

It's not an easy task to find something original in this world where every possibility seems to be being made reality, more readily every day.

So, with the breadth in modularity in MVC as a concept, I wanted to make something that people could use locally and adapt to their needs.

This turned out harder than expected.

My first idea has been largely what I've stuck with since starting; an application to let people communicate resources available, so that people nearby might find use of them. It happens to me often that I buy too much of something in bulk and it goes bad before I'm able to use it. It also happens that I need a stick of butter at the last minute while cooking or something similarly trivial.

This is where I started and it grew into a complicated mess very quickly. Trying to find an MVP, I decided to make it rather a place where people would be able to add items that they have, give them a quantity and then allow people to comment and make a connection through that.

**Update:**

After considering how the app worked, I decided that having a location based app would not be wise without having a location class to which users belong. 

The app originally had three classes that interact, a User which has many Items, Items that have many Comments and belong to Users and Comments that belong to Items and Users. The last bit has been the hardest part in trying to make a reasonably effortless interaction between classes as the logic became difficult to handle.

I tried to add a location column to the User class, but this offers no protections against bad information and it doesn't help organization. So, ultimately, this app uses a Location which has many Users and Items. The ability to control the number of locations makes sense from an admin perspective to ensure that people don't end up writing in any location that they want, which would remove all order.

To develop it further, in the future, there could be subcategories within locations to enable people within a city to create a more finite location, like an apartment complex. I am sure that using location services in the near future will help in creating this organization in a more natural way. At this point, in a very Web 1.0 manner, we have organization and a functioning MVC that alludes to order, allows CRUD abilities, and removes users from impacting order too much.
