---
title: "Secondary Datasets :chart_with_upwards_trend: :chart_with_downwards_trend:"
layout: post
date: 2019-03-01 22:44
image: /assets/images/lab.jpg
headerImage: false
tag:
- data
- weather
- temperature
- Boston
- csv
- data cleaning
category: blog
author: Davor Ljubenkov
description: Markdown summary with different options
jemoji: '<img class="emoji" title=":chart_with_upwards_trend:" alt=":chart_with_upwards_trend:" src="https://assets.github.com/images/icons/emoji/unicode/1f4c8.png" height="20" width="20" align="absmiddle">'
jemoji: '<img class="emoji" title=":chart_with_downwards_trend:" alt=":chart_with_downwards_trend:" src="https://assets.github.com/images/icons/emoji/unicode/1f4c9.png" height="20" width="20" align="absmiddle">'

---

## Weather

Weather dataset had been acquired from [Kaggle](https://www.kaggle.com/jqpeng/boston-weather-data-jan-2013-apr-2018). Dataset contains highs, lows, and averages of temperature, dew point, wind speeds, sea level pressure, and precipitation levels for every day from 1/1/2008 - 4/8/2018 inclusive. Data is publicly available and retrieved from the Weather Underground website.

![Markdown Image][1]

Upon closer examination, it is important to notice that for the entry of, for example, 1.15 inch of snowfall it should be read as 1.15 foot which is 13.8 inch in total or around 35 cm. This conversion matches with the report for March 13 2018. when record snowfall was measured in Boston. ([LINK](https://www.boston.com/news/weather/2018/03/13/massachusetts-snow-accumulation-totals-march-13-2018))

Not only that, but certain days were missing from the dataset. As detailed inspection was performed for the year 2018, two days in March (21st and 22nd Of March 2018) were completely missing from the dataset and those rows needed to be somehow filled in or recreated.


[1]: /assets/images/weather.png
