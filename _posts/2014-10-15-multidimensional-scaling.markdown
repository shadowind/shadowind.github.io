---
layout: post
title: "Multidimensional Scaling"
date: 2014-10-15 00:10:58 -0500
comments: true
categories: stats
---
Multidimensional Scaling(MDS) is a way to reduce dimensionality for non-linear high dimensional data. As opposed to PCA, which is used for linear multidim data, MDS aims to place each object in N-dimensional space perserving between-object distances are preserved as well as possible. Here N < dim(data).  
 
There are a couple of algorithm for MDS, seems very dull to delve. One is generalized MDS, useful for surface data, allowing a surface embedding.  

To choose proper N, first it's very hard to visualize 4D data, so N generally <=3. Second, use Scree Plot to show the diffculty of fitting the data.  
![image](http://i.imgur.com/H2RGrux.png)  
This plot shows to compress all the data in a certain dimension(x axis), how diffcult it is(y axis). In this case, 3 is a compromise choice.  

Here is a more professional definition: The primary outcome of an MDS analysis is a spatial configuration, in which the objects are represented as points. The points in this spatial representation are  arranged in such a way, that their distances correspond to the similarities of the objects: similar object are represented by points that are close to each other, dissimilar objects by points that are far apart.  

See more on: [MDS introduction](http://homepages.uni-tuebingen.de/florian.wickelmaier/pubs/Wickelmaier2003SQRU.pdf)