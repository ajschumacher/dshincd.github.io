---
layout: post
title: "Feature scaling"
modified:
categories: blog
excerpt: 
tags: []
image:
feature:
date: 2015-05-09
---

The [scikit-learn](http://scikit-learn.org/stable/) module makes it surprisingly easy to implement a wide range of machine learning algoirthms in Python. Often times, the only parameter you need to specify is the model itself, and scikit-learn will do the rest.

But before putting your raw data into the model, it's important that it's in the right format. This means ensuring that your predictor variables are numerical and properly scaled. This post will focus on properly scaling your features.

** Feature scaling **

Many of the model implementations in scikit-learn require that your features are on a similar scale. There are two widely accepted methods for doing this:
* Standard scale
* Min-max scale 


Scikit-learn is an amazing [tool](http://scikit-learn.org/stable/) for implementing a wide array of machine learning algorithms in Python.

