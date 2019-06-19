---
layout: post
title:      "Routes, Routes, Routes "
date:       2019-06-19 15:38:14 +0000
permalink:  routes_routes_routes
---


Routes - this is what it all came down to when it came time to debug my rails project. 

My advice: 

### 1) `rake routes` is your new best friend 

Other than using the `rails s` and `rails c` commands, `rake routes` was the command that I used most often. This command gives you that glorious list of url helpers, route verbs, URI patterns, and controller actions. It's basically like a built in cheat sheet for finding the exact route that you need for your app.

### 2) Play around with your `routes.rb` file

There is a TON of different strategies that you can use to modify the routes that are available to you, from nesting routes and namespacing, to limiting routes and even customizing them! Take some time to play around with them to see exactly what each has to offer and learn about the possibilities that they can create for your project. 

### 3) Use pry to help you

Pry is another secret weapon that is at your disposal. Pop that `binding.pry` into your controller or directly into your view `<% binding.pry %>` and use it to see that your url helpers and params are putting out what you expect. Make it easier on yourself and put `gem 'pry` into your gemfile to skip the need of `require 'pry'` at the top of your files. 



