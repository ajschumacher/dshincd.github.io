---
layout: post
title: "Overfitting"
modified:
categories: blog
excerpt: 
tags: []
image:
feature:
date: 2015-05-02
---

**The Problem of overfitting**

A common issue in machine learning or mathematical modeling is overfitting, which occurs when you build an overly complex model that not only captures the signal but also the noise in a dataset. 

Because we want to create models that generalize and perform well on different data-points, we need to avoid overfitting.

In comes regularization, which is a powerful mathematical tool for reducing overfitting within our model. It does this by adding a penalty for model complexity or extreme parameter values, and it can be applied to different learning models: linear regression, logistic regression, and support vector machines to name a few. 

Below is the linear regression cost function with an added regularization component.

![Regularization](/images/regularization.png)

The regularization component is really just the sum of squared coefficients of your model (your beta values), multiplied by a parameter, lambda. 

**Lambda**

Lambda can be adjusted to help you find a good fit for your model. However, a value that is too low might not do anything, and one that is too high might actually cause you to underfit the model and lose valuable information. It's up to you to find the sweet spot, but a good place to start is with lambda = 1, multiplying or dividing by 3.

**Regularization methods (L1 & L2)**

The equation above is called Ridge Regression (L2) because the beta coefficients are squared. However, you can also use Lasso Regreesion (L1) which takes the absolute value of the beta coefficients. Even more, you can combine Ridge and Lasso to get Elastic Net Regression (which includes both squared and absolute value summations in cost function).

Although there is an argument for using L1 [in certain use cases](http://qr.ae/0P069), L2 is often the go to in practice. Also note that your features should be on a comparable scale for regularization to be used. 

[An in-depth look into theory and application of regularization](https://www.stat.berkeley.edu/~bickel/Test_BickelLi.pdf).

In the words of the great thinkers:

* ["when you have two competing theories that make exactly the same predictions, the simpler one is the better." - William of Ockham](http://math.ucr.edu/home/baez/physics/General/occam.html)

* ["Everything should be made as simple as possible, but not simpler." - Albert Einstein](http://c2.com/cgi/wiki?EinsteinPrinciple)
