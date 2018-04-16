---
layout: post
title:      "Desert Survival with Rails"
date:       2018-04-16 20:49:10 +0000
permalink:  desert_survival_with_rails
---

Rails offers a lot of functionality; with a deep dive into convention and a lot of imagination, you can do anything. I learned this with a lot of struggling, trail and error, and of course patience.

### Project:

My rails project is called 'Succulence'. It's not just a simple CRUD app, as I learned; it offers all of that and then some. I tried to implement everything that I learned in the lessons, in my Google-fu and in some creative implementations of things that I've learned and inferred.

Succulence is a project that allows a user to create gardens, into which they can add garden plants to through a selection of plants, or by creating a plant themselves. The purpose of the app is that there is a single source of truth to the plants, in that they have a name, a genus, and a watering frequency. When added into the garden, the plants create a new instance of a garden_plant which immediately associates a last_watered time stamp into the database.

#### Schema:

![Imgur](https://i.imgur.com/C4wliu8.png)

#### Implementation:

The plants are able to be created by users, but only updated by admins because they are used by various garden plants in order to create a unified location for information. This is ensured by validations on the uniqueness of the common plant name within the database.

Users are able to CRUD their gardens, they are able to create and automatically add plants into their gardens and they can destory garden_plants individually. The reason for this is that, with the understanding that this app is the foundation for the JS project, I would like for users to be able to add photos to the individual garden_plants and be able to control their information in a more unique and dynamic way.

The user model is managed with Devise because it worked seamlessly; despite hearing varying reviews of how difficult it is to work with and despite having had to make a couple of work arounds to manipulate an otherwise invisible registrations controller, it worked very well. The third party authentication is mitigated through omniauth-devise using omniauth-github with connection to the Github API.

#### Difficulties:

The hardest part about this project was trying to wrap a join table into the interface. I doubted my model, but after discussing with a few technical coaches and working to implement it, I found that it worked and will likely be a more solid foundation for the further development of this as a maintainable project. 

Understanding that having a single source of truth for a referencable model was what initiatially came to me as the right idea, but doubting myself and wanting to work with different ideas, I worked the project into a simple CRUD app where users could make their own plants, but it seems more problematic to allow users the ability to create thousands of the same plants and now have anything other than reference.

If a mistake were made, for instance, it would not be able to be corrected by one simple model, it would have to be corrected across the board in every instance.

#### Recap:

Learning how to implement an entire project and work between convention and need seems characteristic of all programming. Languages always have constraints and when abstracting on top of languages with other languages (DSLs), it becomes a double edged sword where you are able to make use of incredible power, but not necessarily in the exact way that you would like to and therefore, you end up having to work around to the best of your ability. 

I found this to be extremely helpful in learning the limits that I was able to reach with Rails and I am most definitely better off for future projects knowing that I have stirred and tried my best to fit within convention, but am able to adapt where necessary.



