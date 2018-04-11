---
layout: post
title:      "Rails Routing for Beginners"
date:       2018-04-11 17:46:55 +0000
permalink:  rails_routing_for_beginners
---

Working with rails is an undeniably frustrating pleasure. It does so much, but has an obscene amount of rules that can make it so frustrating that it almost seems like a language unto itself. Like learning a language with a grammar snob looking over your shoulder all the time -- the difference is that a grammar snob understands what you're saying, while rails will give you exactly what you said. This, it seems across the board, is the general experience of coding.

Machines are not stupid, but they have no inferential knowledge unless explicitly programmed to do so.

Rails, for a beginner, is particularly difficult becuase this alck of a sense of linguistic humor turns into serious bugs that are frustrating at best and ego shattering at worst. So, after more of the previously blogged about days-long commas, there have been more days long epic syntactic battles that I would have been better off having understood before spending such an obscene amount of time learning them the hard way.

1. Routes are Defined in a Routing File

       The most obvious things are often the easiest to forget or mistake. I find myself looking to the wrong places to solve problems before realizing that if I run 'rake routes', I'm able to see what I have and where I need to make the change. Rails is dynamic enough to handle most of the problems that we might need to address, inside and outside of RESTFUL standards.

2. Routes can Be Dynamically Generated

       Using the 'resources' macro will allow you to dynamically generate every kind of route available as a default in Rails. By using id symbols, :id, and :model_id within nested routes, Rails will be able to control the direction of requests if the controller and the view have adequate informaiton present control what is being rendered as information from the models.

3. Routes are the glue that holds your MVC together

      To the point above, routes effectively manage the interpretation of URLs and therefore the connection to the interface and the user. It's difficult to say that any feature is more important in such a tightly controlled framework, but without well defined routes and dynamic control, each explicity 'get' request in your routes would be previously defined and impossible to accomplish for a webapp that intends to scale.
			
4. Nested routes need to be explicitly pointed to when using helpers

      One of the most confusing parts of rails link_to helpers is that, when working with nested resources, rails will render as best as it can, but it must be presented with both model references and in a syntax that is reflected in the URL. Working with nested resources, I kept encountering '/model1/:model_id/model2/:id' which, when called as 'link_to model2.name, @model2' would render as '/model1/:id/model2/:model_id', thus linking to models that didn't yet exist within the controller.

5. URL data information is passed in params as information

      As HTTP is a stateless protocol, information is passed via information held in URLs, so, amongst a long string of varying symbols and digits, information regarding model ids, form information and HTTP headers will be passed. Rails handles this in a way that parses the information neatly into params that can be intercepted within the controllers. It's important, because this information is used to render information through the controller to the view, but more importantly, when encountering areas of authorization, where it's important to be able to verify the user, the owner or creator or a resource and whether or not they should have permissions for any CRUD abilities. 
			
TL;DR, pay attention to your information, rake routes, follow conventions regarding syntax (especially with automatically generated resources) and don't forget where things happen.

