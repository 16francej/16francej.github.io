---
layout: post
title: "Making a Bot AI for the Competition: Robocode"
date: 2015-5-28
---

I decided to make a bot AI for the programming game [Robocode](http://robowiki.net/wiki/Main_Page). The code for my bots can be found [here](https://github.com/16francej/My-first-bot/tree/master/src). 

Check my robot out in action at the links below: 
https://www.youtube.com/watch?v=QeSxsuZ-kws&t=8s
https://www.youtube.com/watch?v=9PadLRQHhak

### Targeting
I used a predictive targeting method called "Guess Factor" to statistically generate a good firing angle based on the current and previous movement of my opponent. It generates the minimum and maximum possible angles of firing based on the top speed of the other bot for the current distance, and calculates the angle in that range to fire. The robot logs its opponents angle relative to the last calculation every step, and then fires depending on the target's current bearing offset and position in relation to previous data. 

### Dodging
I used the movement algorithm "Wave Surfing" to dodge bullets from incomeing opponents. A "Wave" represents all possible location that an incoming bullet could have, and the respective probabilites of each derived from previous data. It works by detecting a drop in energy from the opponent to detect a bullet being fired, generating a wave of probabilities depending on previous data gathered from each onHitByBullet event, then identifying, and moving to the area of the wave with the lowest probability of bullet collision. "Surfing" from high areas of probability to low areas of probability is how the algorithm got the name "Wave Surfing" 



