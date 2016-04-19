---
layout: post
theme :
  name : bootstrap-3
title: "Working with the accident data"
category: Reports
tagline: Aneesh Makala
tags: [accidents,map,March,Weekly]
image: /assets/themes/bootstrap-3/images/aneesh1.png
---
{% include JB/setup %}


So, earlier, we had contacted one of the Civil Engineering Professors(KVR sir) and procured Warangal's accident data from 2008 - 2013. The data contained bare locations (in name) along with the no of persons injured/died in the accident.


But, we had a more precise idea of a location. We required the exact latitude and longitude of the location. So I googled around a bit, and ofcourse, there was the GoogleMaps Geolocation API. I tried using it, but due to inaccurate naming of the location fields in our data and a few other reasons, I was unable to get the *correct* latitude and longitude for each location. Some values were very far off. Hence I took to webscraping and did a manual Google Map search and retrieved the most relevant latitude,longitude pair for the 300+ accidents' data we had. I was careful not to get myself be blocked and kept a timeout while scraping!

Once I had the data points, it was only a matter of displaying them on a map. I had previously worked with google maps and django. Hence, I had the map up in a matter of minutes! Here's how it looked.

<img src="/assets/themes/bootstrap-3/images/accidents/first_map.png" style="width: 100%;border-width:2px;border-style: solid;border-color: #7C8081;">

But, then we decided to move our architecture to Meteor. I was excited because Meteor is Javascript, something new to learn! I have just ported the map to Meteor. 

We will proceed by building an algorithm that can identify accident-prone zones. We are currently looking at DB-SCAN. I met with Dr. Subramanyam(Our Data Mining professor) a couple of days back. He suggested a few methods. Looking forward to implementing one.