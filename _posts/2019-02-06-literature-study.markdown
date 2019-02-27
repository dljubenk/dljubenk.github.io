---
title: "Literature Study        :scroll:"
layout: post
date: 2019-02-06 22:44
image: /assets/images/lab.jpg
headerImage: false
tag:
- BSS
- MIT
- SCL
- literature
- papers
- research
- visualization
- python
- fractals
- pandas
category: blog
author: Davor Ljubenkov
description: Paper Research
jemoji: '<img class="emoji" title=":scroll:" alt=":scroll:" src="https://assets.github.com/images/icons/emoji/unicode/1f4dc.png" height="20" width="20" align="absmiddle">'

---

## Acronyms

BSS = Bike Sharing Scheme (Service)

CHS = Cycle Hire Scheme

D.C. = District of Columbia

TfL = Transport for London

EDA = Exploratory Data Analysis

CNN = Convolutional Neural Network

## Collection Process

A reference management software used to cataloguise relevant papers is called [Mendeley](https://www.mendeley.com/newsfeed), and it is quite similar to [Zotero](https://www.zotero.org/).
In total, 142 papers in the domain of smart cities transportation had been collected in categories such as: bike reports (11 papers), bike sharing (77 papers), fostering bicycle usage (4 papers), fractal city (3 papers), gender relevance (5 papers), health, environemnt and risk (14 papers), networks accessibility (7 papers), on-demand ride services (3 papers), sensors (6 papers), urban trajectiry analysis (1 paper), and visualization (5 papers). Of course, neither are all papers going to be relevant, not are all papers provided published yet - so only a smallsubset of this resource will be investigated further in order to construct the appropriate research question and knowledge gap for my thesis. 

---
## Paper 1
---
### "Docked vs. Dockless Bike-sharing: Contrasting Spatiotemporal Patterns"
#### [Grant McKenzie](https://grantmckenzie.com/)
##### [Department of Geography](https://www.mcgill.ca/geography/people-0/mckenzie), McGill University, Montréal, Canada
###### 2018 - 10th International Conference on Geographic Information Science

[LINK](https://grantmckenzie.com/academics/Dockless2018.pdf)

![Markdown Image][1]

MOTIVATION: 
>Explosive growth in U.S. DOCKLESS bikesharing services provided limited time for municipal governments to set regulations or assess their impact on DOCKED bikesharing programs. This paper presents an EXPLORATORY understanding of the differences in activity
PATTERNS between these two services. Results can be used to better inform urban planners, transportation engineers,
and the general public.

Focuses on <mark>Washington, D.C.</mark>

Most of the analysis is just <mark>exploratory</mark>

Results of the paper are <mark>preliminary</mark> due to lack of data

Paper mentions these companies: [Mobike](https://mobike.com/global/), [Spin](https://www.spin.app/) , [Jump](https://jump.com/), [Lime](https://www.li.me/), and [Capital Bikeshare](https://www.capitalbikeshare.com/).

Comparisons were made between Lime (<mark>dockless</mark>) and Capital Bikeshare (<mark>docked</mark>).

Lime is a <mark>private company</mark> and Capital Bikeshare is owned by the <mark>municipial government</mark> of D.C. (also Virginia and Maryland).

Data analysed included only a month of March in 2018. (238,936 individual trips)

Data Attributes: <mark>bike ID</mark>, <mark>time stamps</mark> for the start and end of the trip, start and end <mark>station IDs</mark>.

***Temporal aspects***: <mark>mean</mark> duration, <mark>median</mark> duration, bike trip start times <mark>aggregated</mark> to the nearest hour of a week and independently normalized, pattern <mark>subtraction</mark>

***Spatial aspects***: <mark>Voronoi tessellation</mark> used to partition town map into polygons, subtraction of two voronoi patterns, intersecting these polygons with land use data from D.C.’s Office of Planning

***Networks***: <mark>K-means</mark> was used for clustering the dockless locations with a number of clusters being 269 (= number of docked stations), the average distance between each cluster center and it’s nearest existing dock station was computed -> result = mean distance of 305.4 m with a median of 181.4 m
calculated cluster centers were snapped??? to the nearest road intersection and the average distance to existing stations was
calculated again ->  mean distance to 300.1m and median to 180.2 m. Conclusion: existing dock are well situated

Road network -> shortest path was calculated between each start and end location using <mark>Dijkstra’s algorithm</mark> as implemented in [pgRouting](http://pgrouting.org/).  Once routing analysis was complete, point geometries were generated every 10 m along each of the resulting line geometries. Using these points, kernel density estimates were created for dock and dockless independently, producing the two heat maps. Normalizing the kernel density values, we again calculate subtraction of the two.

Suggestions: other modes of transportations, examine the behavioral motivation for selecting certain services


---
## Paper 2
---
### "Studying Commuting Behaviours Using Collaborative Visual Analytics"
#### [Roger Beecham](http://www.roger-beecham.com/), [Jo Wood](http://www.staff.city.ac.uk/~jwo/cyclehire/), Audrey Bowerman
##### [giCentre](https://www.gicentre.net/) Information Sciences, City University London, United Kingdom
##### [Delivery Planning - Cycling](https://tfl.gov.uk/modes/cycling/), Transport for London, United Kingdom
###### September 2014 - Computers, Environment and Urban Systems Volume 47, Pages 5-15
###### Available online 12 November 2013

[LINK](https://www.sciencedirect.com/science/article/pii/S0198971513001014/pdfft?md5=baa4cb4ef7bbf3c786b640f551aa672e&pid=1-s2.0-S0198971513001014-main.pdf)

![Markdown Image][2]

Focuses on London.

Automatic label classification of commuting behavior? - inferring wokplace of individuals

1) Weighted mean-centres
2) K-means clustering
3) Kernel density estimation

Community detection - 2 types identified (those outside London and those living close to docks)

FLEET MANAGEMENT? -> To keep the BSS as balanced as possible, bikes are manually transported across the city at peak times, and in priority areas docking stations are continually replenished with bikes or bikes continuously removed from docking stations. -> which is expensive!

commuting behaviour - not necessarily a 2-way ride (a so called closed peak-time ‘loop’), can be only in one directon (due to possible scarcity/abundance of bikes at the start/end dock)

Contribution 1 - a new technique for deriving customers’ workplace areas and labelling commuting journeys, based on a spatial analysis of travel behaviours. (-> spatial + temporal used combined and not separately)

Contribution 2 - a visual analytics approach that facilitates a data-driven discourse between a diverse set of stakeholders in a project (data analysts, domain scpecialists, etc.) ->  a process of chauffeuring??? -> computer-supported collaborative work -> Collaborative visual analytics

EDA showed: Journeys at peak-times seemed to be dominated by particular types of people: male users and those living outside of London, and other observations... 

Three Research Questions:

1. What are the characteristics of people who take part in commuting based activities? (their geodemographic profile)

2. Where do commuting events happen?

3. Under what circumstances are journeys made during the working day?

4. How can commuting journeys and commuting LCHS cyclists be reasonably detected?

Customer database attributes: postcode, registration date, genders

Journeys dataset attributes: start and end time, origin - destination (OD) pair

Two datasets are related by a unique customer ID

Data observed between 14th September 2011 and 14th September 2012 =  82,874 LCHS members -> 5,048,000 journeys

Calculated: median of journeys, average journeys per user, percentage of long travels (>30min), average straight-line distance

HINT: To preserve customers’ anonymity - use dummy values are shown, and copyright on database if applicable

Some new attributes have been created: e.g. distance from user's home to the closest docking station, Recency–Frequency (RF) segmentation

How to find frequent job commuters?

* filter for peaks and restrict repeated cycling on working days

But how to choose suitable metrics to differentia between the commuters and casual cyclists? (here, they use: making more than 20 repeated peak-time journeys in the 12 months)

Order cyclists by # of peak-time journeys -> frequency distribution -> POWER LAW??

- observing the visual spatio-temporal anaylsis = lines on a map (visual saliency) + fluctuation for each day of the week

How to derive workplace centres for each cyclist? 

1) Calculate the (frequency) weighted centroid of docking station locations  We speculate -> mean-centre + a standard deviation ellipse (Yuill, 1971)?

2) Even better, use k-means clustering to ommit multiple centres identified as workplaces in a previous method - we feed it the outout of method 1 (standard deviation ellipses) or choose k=2,3 -> after evaluating this method we see that outliers are a problem

3) hierarchical cluster analysis (HCA) is not scalable for a very large amount of cyclists

4) density-estimation method (O’Sullivan & Unwin, 2002) -> tackles outliers better -> but we lose spatial coordinates of workplace
-> two parameters: the size of the kernel and density threshold











---
## Paper 3
---
### "Community Structures, Interactions and Dynamics in London’s Bicycle Sharing Network"
#### [Fernando Munoz-Mendez](https://www.researchgate.net/profile/Fernando_Munoz_Mendez), [Konstantin Klemmer](https://warwick.ac.uk/fac/sci/dcs/people/research/u1690815), [Ke Han](https://www.imperial.ac.uk/people/k.han), [Stephen Jarvis](https://www.dcs.warwick.ac.uk/people/academic/Stephen.Jarvis/)
##### AECOM, University of Warwick, Alan Turing Institute, Imperial College London, UK 
###### August 2018

[LINK](https://arxiv.org/pdf/1804.05584.pdf)

![Markdown Image][3]


Suggestion: instead of pure unsupervsed learning, use extended layers of urban systems (e.g. amenities? and weather data)

Suggestion: more holistic approach needed to draw meaningful conclusions (e.g. use other transportation networks or include further cities)

Suggestion:  address time-varying networks of bike stations and communities, where different
motifs (loop, chain, star) and temporal evolution dynamics with extended time windows could potentially provide deeper insights into inherent relationships of spatially heterogeneous nodes (stations) or sub-networks (communities)



---
## Paper 4
---
### "Comparing Cities’ Cycling Patterns Using Online Shared Bicycle Maps"
#### [Advait Sarkar](https://advait.org/), [Neal Lathia](http://nlathia.github.io/), [Cecilia Mascolo](https://www.turing.ac.uk/people/researchers/cecilia-mascolo)
##### University of Cambridge, UK 
###### Springer, April 2015

[LINK](https://link.springer.com/content/pdf/10.1007%2Fs11116-015-9599-9.pdf)

![Markdown Image][4]

MOTIVATION: 
>Bikesharing Systems have the problem of balancing between system USAGE and DEMAND, which leads to a lack of available bicycles or free parking spaces at stations at various times of the day ([Shawcross et al. 2010](https://www.london.gov.uk/sites/default/files/gla_migrate_files_destination/FINAL%20REPORT.pdf))


Time span: 4.5 months

Number of cities: 10

Number of stations: 996

Number of samples: 10<sup>8</sup>

Focuses on <mark>fullness of stations</mark>, and NOT mobility flows!

<mark>Unsupervised learning</mark> used to show the intrinsic similarities between the cities.

<mark>Predictability</mark> of stations' <mark>occupancy</mark> (and comparing cross-city <mark>error</mark> for each)

<mark>unsupervised clustering</mark> techniques used to determine the similarity of patterns (heterogeneity found only in bigger systems)

<mark>random forest & neural network</mark> used to compare the <mark>accuracy</mark> of forecasting how many bicycles will be at a given station and time to two baselines + EVALUATION 

Studies of shared bicycle systems have recently appeared in the data mining literature, and are often subjects for online data visualisations. -----> http://bikes.oobrien.com/global.php

Froehlich et al. (2009) were the first To apply clustering techniques and forecasting models to identify patterns of behaviour in
stations in Barcelona’s ‘‘Bicing’’ system, explaining results according to stations’ location and time of day. 

a recurring conclusion across analyses is that spatiotemporal system usage patterns are tied to, and reflect, city-specific
characteristics. By focusing on single cities’ systems, these works seem to indicate that each city has a unique pattern, and that forecasting algorithms applied to each one may not be generalisable across the world!!!!

O’Brien et al. (2014) and Austwick et al. (2013) characterise systems at the city-level, comparing them in terms of system size (both by station count and geographic area), daily usage, and compactness; they build a hierarchy of cities that share similar characteristics and apply community detection algorithms to analyse similarities within systems.

- station occupancy data is gathered by scraping bike sharing web services every 2 min for a number of months

- pre- and post-cleaning statistics is presented (percentage of data retained)

- calculating the station capacity (as it is not available from web services) -> problems: malfunctioning docks (i.e.,
erroneous data), docks added/removed -> those station were removed from data (=pruning inconsistent
and inaccurate samples and stations from the dataset)!

- How do we know station location is correct -> pairwise ground distances are computed  between all locations recorded for a single
station using the Haversine formula (Robusto 1957). Larger distances (>10m) were removed from the analysis.

Aggregate occupancy time series are calculated -> Pearson correlation used for comparison week-day and weekend

- Which individual stations share similar behavioural traits across different cities -> used hierarchical clustering using an agglomerative strategy (bottom–up approach)

- selected a metric to measure the similarity between station vectors -> distance metric based on the dynamic time warping (DTW) algorithm (Berndt and Clifford1994) = technique for finding the optimal alignment of two temporal sequences - also uses a 1-h Sakoe–Chiba band (1978)


---
## Paper 5
---
### "Mobility Modeling and Prediction in Bike-Sharing Systems"
#### Zidong Yang, Ji Hu, [Yuanchao Shu](https://kabru.eecs.umich.edu/yuanchao/), Peng Cheng, Jiming Chen, [Thomas Moscibroda](https://www.microsoft.com/en-us/research/people/moscitho/)
##### [Zhejiang University in Hangzhou](https://www.zju.edu.cn/english/), [Microsoft Research Asia](https://www.microsoft.com/en-us/research/lab/microsoft-research-asia/)
###### June 2016

[LINK](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/mobisys16bike.pdf)

![Markdown Image][5]

MOTIVATION: 
>The primary issue for both users and operators is the uneven distribution of bicycles due to the demand and supply changing trends. This demands better bike re-balancing strategies which depend highly on bicycle modeling and prediction.

CONTRIBUTION:
> 1.) spatio-temporal bicycle mobility model based on historical data

> 2.) traffic prediction model mechanism per each station with sub-hour granularity

EVALUATION:
> relative error of an obtained prediction

- focuses on Hangzhou in China

- around 2800 stations and 103 million records

- 1 year span

PART 1: spatio-temporal model

PART 2: estimate the number and time of check in at different stations

PART 3: random forest theory -> predict check outs given: time, weather, real-time bike availability

---
## Paper 6
---
### "Predicting Bike Sharing Demand Using Recurrent Neural Networks"
#### Yan Pan, Ray Chen Zheng, Jiaxi Zhang, Xin Yao
##### The High School Affiliated to Renmin University of China, Beijing
##### Institute of Remote Sensing and Geographical Information Systems, Peking University
###### 2018

[LINK](https://www.sciencedirect.com/science/article/pii/S1877050919302364/pdf?md5=17d9747c4ced4e4bd10d4345573588e0&pid=1-s2.0-S1877050919302364-main.pdf)

![Markdown Image][6]

MOTIVATION: 
>bike sharing demand and supply

CONTRIBUTION:
> 1.) a real-time predicting method

> 2.) community detection + LSTM (Long Short-Term Memory) RNN (Recurrent Neural Network) model

> 3.) bike data + meteorology data

DATA:
>TRAINING SET: Citi Bike System Data of 2017

>TEST SET: January, February, and March of 2018 

>800 Stations

>New York City + Jersey City

EVALUATION:
>Root Mean Squared Error (RMSE)

Deep LSTM = more than 1 layer LSTM -> here, 2-layer LSTM is used

Why Deep LSTM?

It can handle large mount of data in a small amount of time.

SUGGESTIONS:
>How to use these predictions in order to suggest how to distribute the bikes specifically to each station

---
## Paper 7
---
### "Analytics and Bikes: Riding Tandem with Motivate to Improve Mobility"
#### Daniel Freund, Shane G. Henderson, Eoin O’Mahony, David B. Shmoys
##### School of Operations Research and Information Engineering, Cornell University, Ithaca
##### Marketplace Labs, Lyft Inc.
##### Uber Technologies Inc.
###### 2018

[LINK](https://people.orie.cornell.edu/shane/pubs/RidingTandemWithMotivate.pdf)

![Markdown Image][7]

PROBLEM:
> asymmetric demand due to “tidal” commuter flows

> process of rebalancing = largest operational expense

MOTIVATION:
> Improve the allocation of docks to stations, and the creation of an incentive scheme to crowdsource rebalancing

CONTRIBUTION:
> rebalance more efficiently = mathematical optimization model

> system designs that require less rebalancing = incentive program called "Bike Angels" that crowdsources rebalancing through the help of user base


[1]: /assets/images/paper1.png
[2]: /assets/images/paper2.jpg
[3]: /assets/images/paper3.png
[4]: /assets/images/paper4.png
[5]: /assets/images/paper5.png
[6]: /assets/images/paper6.png
[7]: /assets/images/paper7.png

