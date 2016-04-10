---
layout: post
theme :
  name : bootstrap-3
title: "SMS Integration"
category: Reports
tagline: Vivek Unnikrishnan
tags: [report,March,Weekly]
image: /assets/themes/bootstrap-3/images/vivek.png
---
{% include JB/setup %}

Our hardware development had made a lot of progress, thanks to Sreerag. We had decided on getting accidents using a POST request
to our server when the accident occurs. But there were some problems related to this approach
- Accidents may happen in areas with bad cellular reception. POST request on 2g tend to be slow
- We may loose a lot of accidents due to the unreliablity of this method

Hence we decided to try and integrate sms. We did this by using MSG91 as our SMS Partner. Using the virtual number they provide
we managed to pull of an SMS triggered accident. Since Meteor is real time the lag between sms and its appearance on a portal page
is really negligible.

SMS is much more reliable since even in low reception areas there is a much higher chance that the sms will go through. Thus it
helps us fetch help for accidents even faster. The sms is sent with a unique token, latitute and longitute of the accident and the
remaining work is done on the server side.

We will soon publish a demo video showing how this works.
