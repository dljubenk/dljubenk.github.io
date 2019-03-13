---
title: "Prediction :space_invader:"
layout: post
date: 2019-03-08 22:44
image: /assets/images/lab.jpg
headerImage: false
tag:
- RNN
- machine learning
- neural networks
- recurrent
- prediction
- deep learning
category: blog
author: Davor Ljubenkov
description: Prediction

jemoji: '<img class="emoji" title=":space_invader:" alt=":space_invader:" src="https://assets.github.com/images/icons/emoji/unicode/1f47e.png" height="20" width="20" align="absmiddle">'

---

# Using RNN (Recurrent Neural Network) for time series prediction

 Time series in this case are describing frequency of bike sharing rides for each day.
 
 Main dataset used is the BLUEbikes data which includes the period of 2016, 2017 and first 3 months of 2018.
 
 Secondary dataset is weaher data for the same time range.
 
 Methods applied from Keras library include:
 
 - Time Series Generator
 
 - Simple RNN
 
 ---
 
 ## Time Series Generator
 
In a nutshell, sequential models have 3 dimension. These dimensions are: sample size, time steps, and features. Preparing 3D input is not an easy task. So, instead of trying to create a 3D array, TimeSeriesGenerator class is used. The advantage of this class is the ability to set the batch size.

FEATURE ENGINEERING -> not used but could be considered as a next step.

>  Feature engineering is the process of using domain knowledge of the data to create features that make machine learning algorithms work. Feature engineering is fundamental to the application of machine learning, and is both difficult and expensive. The need for manual feature engineering can be obviated by automated feature learning. Feature engineering is an informal topic, but it is considered essential in applied machine learning. [WIKI](https://en.wikipedia.org/wiki/Feature_engineering)

Total data is split into:

- Train Data

- Test Data

- Holdout Data

