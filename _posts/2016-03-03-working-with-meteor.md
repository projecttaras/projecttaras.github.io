---
layout: post
theme :
  name : bootstrap-3
title: "Working with meteor"
category: Reports
tagline: Vivek Unnikrishnan
tags: [report,March,Weekly]
image: /assets/themes/bootstrap-3/images/vivek.png
---
{% include JB/setup %}

We had been busy due to the Mid Semester examinations but now we have started working in full swing. Some of the key decisions we took during this week are

- Use Meteor JS for backend
- Work in collaboration with Hospitals and Police Stations for real time accident management

I would like to elaboarate about Meteor JS and why we decided to go with it.

#Meteor JS: Real time 

Meteor JS focuses on real time data transfer between the clients and the server. Build on top of Node Js, the artitechture is really simple but complex at the same time. Being a Python user, javascript was not out of the world but it took some time to get used to. Nevertheless Aneesh and I started working on some example applications, mainly a real time todo application. That is when I noticed some key difference in the way Meteor and Django functioned.

- Meteor uses collections and MongoDb: This means that it is schema independent. Although it offers creative independence in terms of data storage, it bothered me a lot. Later I found a Schema api that can be used to augment and restrict Meteor Data.
- Meteor structure is open: Structure in meteor is pretty open. On further reading I found that meteor compiles all the Js and css to produce one common file. We found a structure consisting of splitting up client, server and public files enabling easier management of files.
- Out of the box Android application building

For now we are learning how to build applications and utilize the full extend of meteor js capabilities. Will update regarding how far we have reached in the next post.

<img align="center" src="/assets/themes/bootstrap-3/images/meteorlogo.png" style="width: 50%;">
