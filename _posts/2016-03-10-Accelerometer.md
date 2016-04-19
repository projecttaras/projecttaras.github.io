---
layout: post
theme :
  name : bootstrap-3
title: "Working with Accelerometer"
category: Weekly Log
tagline: Sreerag Sreenath
tags: [report,Feb,progress,hardware]
image: /assets/themes/bootstrap-3/images/sreerag.png
---
{% include JB/setup %}

This week I have worked on interfacing accelerometer with Arduino. The following are the complied results on the module. I have also included some of the research papers which I refered to.

<br>
<img align="center" src="/assets/themes/bootstrap-3/images/blog/acc.jpg" style="width: 50%;">
<br>
<h2>What is accelerometer?</h2>
An accelerometer is a device that measures proper acceleration ("g-force"). Proper acceleration is not the same as coordinate acceleration (rate of change of velocity).
<br>
<br>
<h2>Which Accelerometer did we purchase?</h2>
 ADXL335 is a small, thin, low power, complete 3-axis accelero-meter with signal conditioned voltage outputs. The product measures acceleration with a minimum full-scale range of ±3 g. It can measure the static acceleration of gravity in tilt-sensing applications, as well as dynamic acceleration resulting from motion, shock, or vibration. 
ADXL335 is 3v3 compatible device, it's powered by a 3.3v source and also generates 3.3v peak outputs. It has three outputs for each axis i.e. X, Y & Z. These are analog outputs and thus require an ADC in a micro-controller. Arduino solves this problem. We will be using the analog functions of Arduino.

<br>
<br>
<h2>Arduino Interfacing with accelerometer</h2>
<img align="center" src="/assets/themes/bootstrap-3/images/blog/sensors_AccelerometerRef_bb-1024.jpg" style="width: 50%;">
The accelerometer module has 5 pins, namely
<br>
<ul>
	<li>1. GND-To be connected to Arduino's GND</li>
	<li>2. VCC-To be connected to Arduino's 5V</li>
	<li>3. X-To be connected to Analog Pin A5</li>
	<li>4. Y-To be connected to Analog Pin A4</li>
	<li>5. Z-To be connected to Analog Pin A3</li>
</ul>
<br>
NOTE: We don't need to power the module from 3.3v because it already has a 5v to 3.3v converter.
<br>
Use 2-pin relimate for connecting Vcc and GND.
Use a 3-pin relimate for connecting X, Y & Z outputs.
Also connect AREF pin to the 3.3v. This is done to set the reference voltage to 3.3v because the output of ADXL335 is 3.3v compatible.
<br>
<br>
<h2>Some good research materials Found</h2>
These are some of the ideal simulation data I have collected during a simulation in the room.

<h3>Stable acclerometer reading</h3>
<img align="center" src="/assets/themes/bootstrap-3/images/blog/stable.png" style="width: 50%;">
<br>
These are the readings found when the acclerometer stays idle on the table

<br>
<br>
<h3>Sudden crash reading</h3>
<img align="center" src="/assets/themes/bootstrap-3/images/blog/suddencrash.png" style="width: 50%;">
<br>
These are the readings found when the acclerometer is subjected to sudden force.

<br>
<br>
<h3>Slide Over reading</h3>
<img align="center" src="/assets/themes/bootstrap-3/images/blog/slideover.png" style="width: 50%;">
<br>
These are the readings found when the acclerometer changes its orientation.

<br>
<br>
<h3>Roll Over reading</h3>
<img align="center" src="/assets/themes/bootstrap-3/images/blog/rollovr.png" style="width: 50%;">
<br>
These are the readings found when the acclerometer performs an rollover.

<br>
<br>
<h2>Some good research materials Found</h2>

I found the following research materials good about accident detection.
<br>
<a href="http://www-nrd.nhtsa.dot.gov/pdf/esv/esv17/Proceed/00041.pdf">Accelerometer Reading Data research</a>
<br>
<a href="http://www.nhtsa.gov/DOT/NHTSA/NRD/Articles/ESV/PDF/18/Files/18ESV-000285.pdf">Accelerometer Reading Data research for Nissan cars</a>
