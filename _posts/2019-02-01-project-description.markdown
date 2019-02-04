---
title: "Project Description"
layout: post
date: 2019-02-01 22:44
image: /assets/images/lab.jpg
headerImage: false
tag:
- MIT
- SCL
- bike sharing
- digital city
- graph mining
- machine learning
- data visualization
- data science
star: true
category: blog
author: Davor Ljubenkov
description: Markdown summary with different options
---

## Proposal

**Data visualization** methods in the domain of digital cities using:
* Data mining
* Graph processing and information network analysis
* Machine learning

Thesis will be conducted at ***Massachusetts Institute of Technology***, SENSEable City Lab.
Director of the Lab is [Carlo Ratti](https://en.wikipedia.org/wiki/Carlo_Ratti), and project responsibles are [Fábio Duarte](https://tedxbeaconstreet.com/speakers/fabio-duarte/) and [Paolo Santi](http://webhost.services.iit.cnr.it/staff/paolo.santi/).

---
![Markdown Image][1]

---

## Background

This study will apply data science methods in order to improve the quality of life in contemporary cities, by investigating ***Bike Sharing Systems***.

> Bicycle sharing system or bike-share scheme, is a service in which bicycles are made available for shared use to individuals on a short term basis for a price or free. The user borrows and returns the bike by placing it in a "dock". If the service doesn't you dock, then it is referred to as "dockless". [wikipedia](https://en.wikipedia.org/wiki/Bicycle-sharing_system "Bicycle-sharing system")

In this study, the focus will be on dock bike sharing systems as datasets from this subcategory of bike sharing systems are easily obtained, and mostly publicly available for research purposes - compared to dockless scheme type.

Datasets taken into consideration were collected from bike sharing systems corresponding to different cities and urban areas in United States of America, Canada, Mexico, Brasil, Spain, and United Kingdom. An overview of cities included for each country can be observed below.

**United states**: Atlanta (Georgia), joint area of Boston-Cambridge-Somerville-Brookline (Massachusetts), Chattanooga (Tennessee), Chicago (Illinois), Columbus (Ohio), Los Angeles and San Francisco (California), Minneapolis (Minnesota), New York (New York), Philadelphia (Pennsylvania), Washington D.C. 

**Canada**: Montreal, Toronto, Vancouver

**Mexico**: Guadalajara, Mexico City

**Brasil**: Porto Alegre, Recife, Rio de Janeiro, Salvador, Sao Paulo

**Spain**: Madrid

**UK**: London

![Markdown Image][2]

For example, Boston area datasets provided by [BLUEbikes](https://www.bluebikes.com/) consists of timespan between year 2011 and 2018, and for each date include: duration (in seconds), start date and time, end date and time, start station ID and name, end station ID and name, bike ID, user's member type (customer or casual), zip code of user's whereabouts, user's gender. Of course, data can be missing or incorrect which will have to be dealt with in a data cleaning pipeline segment. Datasets are in .CSV format and a snippet of data is represented in the image below.

![Markdown Image][3]

## Problem Statement

Investigating the usage of available data and what we can learn from it, applying obtained insights in order to simulate certain optimizations for specific city use cases. The set of problems will be identified based on previously published papers in the domain of bike-sharing systems.
Problem statement will express the relationship between two or more measurable properties which will be empirically tested in the later stages of this thesis.

---

## Problem

---

## Purpose

---

## Goal

---

## Tasks

Research study of the previous work to try and identify common problems, while extracting an unique knowledge gap this thesis will cover in detail.
The very nature of any identified research problem related to this project, being it's property to be translated into a network model, implies that using graph theory and its metrics can answer many questions one might pose about it.

---

## Methods

The code will be provided in the form of a Jupyter notebook. Jupyter is a python module, and is available either preinstalled as an Anaconda module, or can be installed manually with pip. In the case of manual installation, the user will also need to install the modules pandas, numpy, and scipy. The files, having an extension ".ipynb", can be run either directly from Jupyter's GUI, or run from the commandline inside the unzipped folder. Running the second command on a windows machine may require adding the Python scripts directory to the PATH variable, located in the subdirectory "Scripts" under the Python installation directory.

Interesting Python libraries to be used:
* **Folium** - displays spatial data on interactive leaflet maps (e.g. implementing heat maps)
* **GeoPandas** - works with geospatial data and coordinate system



---

![Markdown Image][4]

###### This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/licenses/MIT) file for details.
[MIT](https://mit-license.org/) © Davor Ljubenkov

[1]: /assets/images/lab.jpg
[2]: /assets/images/map.png
[3]: /assets/images/data.png
[4]: /assets/images/bike.jpg

