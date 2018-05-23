---
layout: post
title:      "Transitioning from Ruby to Javascript"
date:       2018-05-23 15:38:40 +0000
permalink:  transitioning_from_ruby_to_javascript
---


Learning to code is a lot. It's possible to leave it there and everyone reading this would agree.

Going between languages, as is required when working with JS front ends and Rails backends, feels like something that becomes natural, like riding a bike, but dangerous, like riding a bike down a steep hill with no breaks. Not forgetting, as well, that there are all varieties of DSL (domain-specific language) grammars in the folds of every language.

The transition from Ruby to Javascript was surprisingly not terrible, but if it weren't for the training wheels of quick scanning references and very cultivated Google-fu skills, it would likely have taken a bit longer to work my brain from one language to another, understanding better what each respective langauge has available, what it lacks that were so enjoyed in the other language, and what ways there are of referencing to use or conjuring up, through logic or library, some way of getting what it is that you need.

After having met many opinionated and proud Rubyists, I have learned that they are a proud and quirky people. From here out, I should use 'we' when refering to these people as I, too, have been converted. Not for reasons of computer science allure, sleek data management, (quite-clearly not) speed; no, Rubyists clearly cherish their presence in infrastructure, the elegance of the language, and the community that continues to develop.

Enter Javascript, a language pulled from the mire of the internet's long-suffering third and fourth decades, which has absorbed more than what can be considered a coherent set of influences. Generally disorganized and lacking the svelt readibility of Ruby, when writing in it, despite these qualities, it's clear to see why it has become actually ubiquitous.

This transition is what should take the focus here, however. It seems that the simplest parts of the language, the nuances of where to add a bracket or a semi-color, or when not add anything, were the first to become confusing. In balancing the two languages, it is easy to read both, but the smallest parts are the most difficult to adjust to.

For me, the JS shift brought out the worst, but I noted the following:

   - Put parentheses EVERYWHERE. If you don't, everything will break. All conditions, all chained functions.
   - Blocks are separate functions in JS. You must declare the function, nothing is implied.
   - Semi-colons, too, go everywhere, but they won't break anything.
   - 'def' and 'end' are replaced with curly braces and a 'function()' definition that takes in params.
   - None of your favorite methods are present, but where there is a will, there is a library that you can find to do that.

 The most difficult part of this transition was, for me, was adjusting to different means of debugging and being able to trace information. Bringing these slight variations to the forefront and not making constant mistakes with these smallest parts, without the ready access to information like a 'binding.pry' will give, with direct access to the entire self object, 'debugger' takes patience and, although arguably more accurate and with more relative information to the entire source/network devtools suite that most modern browsers offer, querying specific information is not quite as foolproof.

Ruby is comparatively low maintenance and simple, but JS on web has the DOM, and you can do almost anything to your view. Where Ruby can get you hard connections to data, JS can take those connections and turn them into lighter weight rendering and provide a user experience that doesn't rely on constant reloads and the limitations of simple MVC, but, through Rails and other frameworks, harnesses them.
 

