---
layout: post
title: "Multivariate Adaptive Regression Splines--MARS(what)"
date: 2014-11-02 10:28:51 -0600
comments: true
categories: stats
---
Multivariate adaptive regression splines (MARS) is a form of regression analysis. It uses surrogate features (like linear piecewise function) instead of the original predictors. 

The model is a weighted sum of **basis functions** BFi(x).

y = 25 + 6.1 BF1-3.1 BF2 

Each basis function BFi(x) takes one of the following three forms:

1. Constant 1.
2. Hinge function.
3. Product of two or more hinge functions.

**Hinge functions** takes the form of:

	Max(0,x-c) 
	Or
	Max(0,c-x)
 
Where c is a constant, call knot.

![image](http://i.imgur.com/Ghi77CG.png)

As we can see on the plot, if using a linear regression model, it's very likely to draw a single line from upper left to lower right, which in the middle most data will below the regression line. It will result an unrandom error. Besides transforming the data to log, inverse or knn form, we could also use MARS model to split the data. Identify which area have the same distribution(basis function). The split point is completely determined by original data, called knot. 

An example of multi variable MARS model is:  
Housing Price(Y) =26.5927 - 0.5718 * max(0, Lstat -6.07)+ 2 * max(0,6.07-Lstat)+7.6303*max(0,RM-6.431) - 9.9023 *max(0,DIS-1.425)+ ...  

![image](http://upload.wikimedia.org/wikipedia/commons/9/9e/Friedmans_mars_ozone_model.png)  
This is how it looks like in higher dimension.

####Pros 
+ more flexible than linear regression models.
+ simple to understand and interpret.
+ make predictions quickly.
+ can handle both continuous and categorical data.
+ suitable for handling fairly large datasets.
+ requires little or no data preparation.

####Cons
+ do not allow missing values in predictors.
+ do not give as good fits as boosted trees(But higher speed and interpretability).

Also the term "MARS" is trademarked and licensed to Salford Systems(the following video is also conducted by Salford Systems). In order to avoid trademark infringements, many open source implementations of MARS are called "Earth". r-package "[earth](http://cran.r-project.org/web/packages/earth/earth.pdf)"

[Video Here](https://www.youtube.com/watch?v=gk7L7vcfpWc)