---
layout: post
title: "Yourinalyis (Apologies for the pun): IOT Urinalysis Device"
date: 2017-10-28
---

## Inspiration
The information contained in urine about a person's health is incredibly useful, though there exists no easy way for the everyday person to gain this insight. I have always been interested in using data from the body to monitor my health, and this was an extension of that. I wanted to make a urinalysis device that didn't rely on expensive medical laboratories, but instead allowed people to bring these labs to their own toilet: without having to replace it. 

![](https://i.imgur.com/5kxiyD8.jpg)

## What it does
The device essentially measures the concentration of ions in urine to suggest hydration level and kidney function (https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2151744/). My device quickly probes the urine's resistivity and relates that to ion content. After this, it measures the water level to infer the concentration of ions in the urine. The data from the measurement is then sent to your smartphone. If you are dehydrated, a text is sent reminding the user to drink water. 

## How I built it
I built this using the Particle RedBoard. It is a wifi-enabled microcontroller that makes it really easy to rapidly prototype an IOT device. I used a water level sensor to check the change in depth and simply two metal leads to probe the ion content. My algorithm took the change in these two values relative to each other and discerned the ion density. 

![](https://i.imgur.com/QXqs8j7.jpg)

## Challenges I ran into
The sensors I bought are pretty cheap, so it was difficult to get them to give reliable results. In the end, controlling the outside conditions as much as possible helped me to remedy this. I was also new to the Particle RedBoard coming into this Hackathon, but the device's learning curve is relatively forgiving. 

## Accomplishments that I'm proud of
My device works pretty reliably which I am happy about. It was also fun to learn how to use a new micro controller. 

## What I learned
I learned a lot about the Particle RedBoard, which going into the competition I knew nothing about. It took me a while to learn the IDE and how to even connect the board to wifi, but after a lot of trial and error I eventually figured it out. 

## What's next for Yourinalysis
I was able to contact a professor in the medical school here and he gave me some interesting advice and feedback related to the applications of my project. Patients in a hospital who can no longer use the bathroom are forced to use a catheter attached to a foley, where their urine is collected. Currently, nurses periodically check a patients foley and record in a notebook the increase in urine since their last check. They then upload this to the hospital database. My project would not only increases the accuracy and frequency of this data collection, but could also give doctors insight into the patient's urine contents to give them valuable information going forward. 
