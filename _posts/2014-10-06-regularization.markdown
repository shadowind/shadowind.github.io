---
layout: post
title: "regularization"
date: 2014-10-06 11:17:11 -0500
comments: true
categories: stats
---
I find it's a good way to understand by paraphrasing stat terms.   

In simple terms, regularization is tuning and selecting the weight of variables. By giving less weight to those unimportant variables while keep important variables almost reamin same weight. If you don't do this, then all the variable will be regard as same importance, so for a model contains many variables, it will overfit; for a simple model, it will underfit.   

In other words, regularization has two reason:  
1) Avoid overfitting by not generating high coefficients for predictors that are sparse  
2) Stabilize the estimates especially when there's collinearity in the data

![image](http://qph.is.quoracdn.net/main-qimg-c8436cb17c8797831f857289eb2d0876?convert_to_webp=true)

More info:  
http://www.quora.com/What-is-the-difference-between-L1-and-L2-regularization