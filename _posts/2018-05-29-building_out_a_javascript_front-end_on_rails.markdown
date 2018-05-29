---
layout: post
title:      "Building Out a Javascript Front-End on Rails"
date:       2018-05-29 21:00:40 +0000
permalink:  building_out_a_javascript_front-end_on_rails
---


There is no surprise why JS is the fancy kid on the block. It works seamlessly thanks to constantly improved integration with everything that is used to access the internet and provide for growing and more immersive/responsive experience online.

Rails, to this end, is a great companion to a JS client-side app. It provides access to a wide variety of tools that don't necessarily exist in the JS ecosystem. Although my current application, Succulence, was built as a full scale MVC Rails app, it would have been largely easier to not have to consider the difficulties of mitigating information presentation with Rails helpers, .erb files, and Javascript as an afterthought. In the future, to keep an app like this as svelt and integrated as possible, I would imagine HTML based Ruby will be out of absolutely necessity rather than a planned feature.

Understanding, also, that this application is not using Webpack or any means of restricting JS loading. Scope is very broad in the presentation of this app. One other note and something that gave me all of the trouble with this application: Turbolinks, a gem that's automatically added when building out a Rails application, causes unexpected consequences for how JS will load on a page. The gem itself is problematic because it attempts to do much of what a progressive JS app would do, by loading the page partials only, not entire pages.
