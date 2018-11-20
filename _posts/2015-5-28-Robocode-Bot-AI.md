---
layout: post
title: "Making a Bot AI for the Competition: Robocode"
date: 2015-5-28
---

I decided to make a bot AI for the programming game [Robocode](http://robowiki.net/wiki/Main_Page). The code for my bots can be found [here](https://github.com/16francej/My-first-bot/tree/master/src). 

Check my robot out in action at the links below: 

[Video 0](https://www.youtube.com/watch?v=QeSxsuZ-kws&t=8s)

[Video 1](https://www.youtube.com/watch?v=9PadLRQHhak)

### Targeting
I used a predictive targeting method called "Guess Factor" to statistically generate a good firing angle based on the current and previous movement of my opponent. It generates the minimum and maximum possible angles of firing based on the top speed of the other bot for the current distance, and calculates the angle in that range to fire. The robot logs its opponents angle relative to the last calculation every step, and then fires depending on the target's current bearing offset and position in relation to previous data. 

### Dodging
I used the movement algorithm "Wave Surfing" to dodge bullets from incomeing opponents. A "Wave" represents all possible location that an incoming bullet could have, and the respective probabilites of each derived from previous data. It works by detecting a drop in energy from the opponent to detect a bullet being fired, generating a wave of probabilities depending on previous data gathered from each onHitByBullet event, then identifying, and moving to the area of the wave with the lowest probability of bullet collision. "Surfing" from high areas of probability to low areas of probability is how the algorithm got the name "Wave Surfing" 

### Challenges
Its always fun learning a new technology, but figuring out all of the elements of Robocode definitely took a bit of getting used to. Once I overcame that, one of the big challenges was creating something that was better than the open source out there right now. It is a "zero-sum" game, because almost every robot is as good as the open source code, so in order for the robot to have a positive win rate you need to improve upon open source algorithms which are already pretty sophisticated. It took a while to find places to improve upon what was already out there. 

### Learnings
The relationship between being able to improve on open source code and success stood out to me as a big takeaway from this project. While effective high level, it has become relatively easy for beginners to pick up on open source algorithms and impliment them in some of their first bots. This increases the overall standard of competition because if you aren't improving upon open source then you won't have a positive win rate. I think this is true for software/hardware in general. In order to actuall sell a product, it has to be noticeably better than what is out there as open source. This can be tough to achieve because of how advanced certain open source technologies already are. An example of this is IntelliJ IDEA, an enterprise Java IDE that also has a free community version. I recently switched from community to the enterprise edition and was really surprised with all of the improvements between the community edition and the paid edition. They iron out a lot of headaches that come with dependencies, and deliver much more intelligent tools to the user. The UX is overall much better, and i've had a great time using the IDE so far. From a business perspective, it is probably tough for Jet Brains to keep innovating and adapting to beat the open source technology that is already out there. Overall, this is definitely for the benefit of tech as a whole as it pushes businesses to keep improving upon what they already have and forces them to be really creative in thinking about their product. 


