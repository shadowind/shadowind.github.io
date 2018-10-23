---
layout: post
title: "Maximam likilihood"
date: 2014-10-15 20:04:07 -0500
comments: true
categories: stats
---
When I learn new things during class, I feel everything is familiar, then I review, all I know is the terminology, what it is, I have no idea. I've heard maximam likilihood for years, and I knew it's a way to get best estimate theta(θ).    
I'm the [Greek Letter magic keyboard](http://greek.typeit.org/)  

Enough of this digression,let's return to our story. Given   I have a MKT test tmr, I need to make sure these basic concepts are correct. It's turn out to be very simple. And I will put it in a simplier way.  

In real world, what we can see is a set of observations, like a sample from the population. But we never know what the true population is. Statistician's job is find the best description(estimation) for the true population, which is called likilihood. In mathematics, P(X|θ), given X, find θ.  

In order to find it, first we need to make a few assumptions: the distribution type of the population, like binominal, linear etc. This means we know it's probability function with a (set of) unknown θ. Then we can apply maximam likilihood estimation:  
```
P target=P(X1)&#42;P(X2)&#42;...&#42;P(Xn)  
max(P target)
```  
Then it's a math problem, in most cases, first we use a log function to get exponent value, then derivative the to get the extreme value. That's the θ we are looking for.  
For more info, see this short video:  
<a href="http://www.youtube.com/watch?feature=player_embedded&v=BFHGIE-nwME
" target="_blank"><img src="http://img.youtube.com/vi/BFHGIE-nwME/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>

