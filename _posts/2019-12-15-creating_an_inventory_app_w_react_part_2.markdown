---
layout: post
title:      "Creating an Inventory App w/ React (Part 2)"
date:       2019-12-16 04:04:30 +0000
permalink:  creating_an_inventory_app_w_react_part_2
---


This week I continued to work on my Kitchen Inventory App and built my back-end API database. I chose to use Rails and because I am creating a simiple app, decided to stick with SQLite, which is the default relational database management system (RDBMS) for Rails. To create my app I used `rails new kitchen-inventory-api` and marked it with the `--api` and `--database` flags to streamline the files that would be generated. 

In order to utilize my back-end app with the front-end portion that I built last week, I had to make a few changes to my files so that my server would run on localhost:3001 (under config>locales>puma.rb) I also enabled Rack CORS under the initializers folder and cors.rb file, setting the origin for my front end to "http://localhost:3000", making sure to uncomment this gem in my gemfile and subsequently running bundle install to ensure that everything would run properly. 

Next I used this handy Rails feature to generate my models: `rails g scaffold Model attribute:type`
For my inventory app, I needed just two models. The first was a location (ie fridge, freezer, spice rack) with a name attribute as a string. The second was the item model with `name:string`, `amount:integer` and `measurement:string`.
Because I want to be able to access items in my fridge from my app, I utilized ActiveRecord associations and set my items up with `belongs_to :location`and my locations with `has_many :items`. Once this was set up, I created the database and ran the migrations. 

I started up my rails server and navigated to localhost:3001/items and /locations. All that showed up on both pages was an empty array [ ]. Success!!! To test out my models, I opened the rails console and created several locations. 
![](https://i.imgur.com/In5JDGtl.png)

I refreshed my page at /locations and *Voila!*
![](https://i.imgur.com/bXtbYNBl.png)

I then added an item to my fridge and double checked to make sure that my association had worked by testing `Item.last.location` to be sure that it pulled up fridge
![](https://i.imgur.com/dcDmPmYl.png)
![](https://i.imgur.com/pwMPN8Yl.png)

Next week, I will be integrating the back-end with the front-end and playing with the javascript, html, and css to get it looking stylish.
