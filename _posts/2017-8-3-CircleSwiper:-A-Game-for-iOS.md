---
layout: post
title: "CircleSwiper: A Game for iOS"
date: 2017-8-3
---

Live demo: https://youtu.be/N-RbBzLItNM

### Intro
I spent most of the summer after my freshman year in Guatemala repairing medical equipment, but after coming back to the US I had a month left
of summer and a lot of free time. I decided to explore app development, and completed the online course: "Developing iOS 10 Apps With Swift" by Profressor Paul Hegarty
at Stanford. Overall I enjoyed the course, I liked how he incorporated lessons about overall program design along with Swift and Xcode. It was sometimes
frustrating to not be able to ask questions, but I was able to find most answers through the discussion forums. You make a few different apps throughout the couse, and after
finishing I wanted to build something of my own. 

### Overview
CircleSwiper is a game where a player races to swipe circles off of their screen, while avoiding red squres that pop up as time goes on. I was inspired by the trend
of simple game designs that are popular on the app store, and wanted to build one of my own. Here are some photos of the project: 

![](https://i.imgur.com/Gx0MH7w.png)
![](https://i.imgur.com/BaasCD6.png)

### Challenges
If a circle initially spawned onto a square, the user would immediately lose for something that was not their fault. This obviously isn't a great game mechanic,
so one of the technical challenges I ran into was calculating possible spawn positions in the most efficient way possible. I based my algorithm off of the collision detection
technique of "Spatial Partitioning". The area of the screen is split into quadrants, and each quadrant contains all of the red squares residing in it. When a green circle spawns it
randomly selects one of these quadrants, then checks if it is colliding with any of the squares in this quadrant. If not, the circle is added. This is faster from my original method, 
where I compared the new circle to every other circle on the screen. This algorithm had an O(n^2) runtime and was not very efficient as the game progressed, because checking for each intersection
itself added a heavy time constraint. 

### Learnings
I learned how to use Xcode and Swift for this project which was initially difficult, but one of the biggest things I learned about through this project was the MVC design pattern. This made it 
really easy for me to seperate the different components of my program, and will make it easy for me to add onto the project if I want to come back to it in the future. 

The code for this project can be found at https://github.com/16francej/CircleSwiper
