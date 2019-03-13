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

 Time series in this case are describing frequency of bike sharing rides (by observing the total quantity of rents) for each day.
 
 Main dataset used is the BLUEbikes data which includes the period of 2016, 2017 and first 3 months of 2018.
 
 Secondary dataset is weaher data for the same time range.
 
 Methods applied from Keras library include:
 
 - Time Series Generator
 
 - Simple RNN
 
 ---> consider as a next step: more advanced sequential methods like LSTM and GRU instead of RNN for better results
 
 ---
 
## Time Series Generator
 
In a nutshell, sequential models have 3 dimension. These dimensions are: sample size, time steps, and features. Preparing 3D input is not an easy task. So, instead of trying to create a 3D array, TimeSeriesGenerator class is used. The advantage of this class is the ability to set the batch size.

FEATURE ENGINEERING -> not used but could be considered as a next step.

>  Feature engineering is the process of using domain knowledge of the data to create features that make machine learning algorithms work. Feature engineering is fundamental to the application of machine learning, and is both difficult and expensive. The need for manual feature engineering can be obviated by automated feature learning. Feature engineering is an informal topic, but it is considered essential in applied machine learning. [WIKI](https://en.wikipedia.org/wiki/Feature_engineering)

Number of samples is 821.

Total data (2 years and 3 months of worth) is split into:

- Train Data

- Test Data

- Holdout Data

Performance of the model calculated by: 

<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{1-mae}{mean}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{1-mae}{mean}" title="\frac{1-mae}{mean}" /></a>

---

## Data Preprocessing

Attributes:

- <mark>starttime</mark> (year, month and day of aggregated bike share rides) - can be droped out of table for future steps

- <mark>freq</mark> (total number of bike share rides executed on the day observed)

- <mark>freqscaled</mark> (freq scaled and reshaped to be a value between 0 and 1)

- <mark>Year</mark>

- <mark>Month</mark>

- <mark>Day</mark>

- <mark>High Temp (F)</mark>

- <mark>Avg Temp (F)</mark>	

- <mark>Low Temp (F)</mark>

- <mark>High Dew Point (F)</mark>

- <mark>Avg Dew Point (F)</mark>

- <mark>Low Dew Point (F)</mark>

- <mark>High Humidity (%)</mark>	

- <mark>Avg Humidity (%)</mark>

- <mark>Low Humidity (%)</mark>	

- <mark>High Visibility (mi)</mark>

- <mark>Avg Visibility (mi)</mark>

- <mark>Low Visibility (mi)</mark>

- <mark>High Wind (mph)</mark>

- <mark>Avg Wind (mph)</mark>	

- <mark>High Wind Gust (mph)</mark>	

- <mark>Snowfall (in)</mark>

- <mark><mark>Precip (in)</mark>

- <mark>Events</mark> (Rain, Snow, None) - can be droped out of table for future steps

Things to be added in future steps:

- Weekday or Weekend (0 or 1)

- Season (Winter, Spring, Summer, Fall)

- Holiday or not

- User Type (Casual or Registered)

Things to consider for future steps:

- Normalization of values (by dividing each value with the maximum observed)

- Repeat the same procedure but instead of the total number of rentals overall, try and investigate total number of rentals for a single (or multiple) station of interest

---

The following image depicts the number of rentals:

![Markdown Image][1]

Things to consider for future steps:

- what about the anomalies (zero values or close to zero values)? Possibility to replace them with the average of that month?




[1]: /assets/images/plot1.png
