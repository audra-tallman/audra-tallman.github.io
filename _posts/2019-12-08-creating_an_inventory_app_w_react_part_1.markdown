---
layout: post
title:      "Creating an Inventory App w/ React (Part 1)"
date:       2019-12-09 00:26:50 +0000
permalink:  creating_an_inventory_app_w_react_part_1
---


To become more comfortable with React and build my coding skills, I decided to create a Kitchen Inventory app. To get started, I used `npx create-react-app kitchen-inventory` followed by a quick `npm audit fix` to correct any dependency vulnerabilities. I then started to modify App.js by removing the unncessary React code and added my main parent component `<Inventory />`, not forgetting to import it at the top of course!

From there I started to construct my individual components. I used the class constructor to create my Inventory component, included some event handlers and a form so that I could add items to my inventory.  I also imported my Item component so that each item added would be listed on the same page once it had been added.

 ![](https://i.imgur.com/wc7khLzl.png)

I wanted to be able to keep track of the amount of each item that I have on hand, so I created a Quantity component with buttons to increase and decrease the amount.

![](https://i.imgur.com/JvDY9wpl.png)

Below is a snapshot of the App after having added several items and changing the amounts for each: 

![](https://i.imgur.com/evFMCPOm.png)

Check in next week for Part 2 as I continue to work on this app and create a back-end database to store and update my items. 
