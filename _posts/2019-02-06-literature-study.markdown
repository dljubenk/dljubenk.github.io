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

Suggestions: other modes of transportations, examine the behavioral motivatio for selecting certain services


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

Collaborative visual analytics?

1) Weighted mean-centres
2) K-means clustering
3) Kernel density estimation

Community detection - 2 types identified (those outside London and those living close to docks)

To keep the BSS as balanced as possible, bikes are manually transported across the city at peak times, and in priority areas docking stations are continually replenished with bikes or bikes continuously removed from docking stations. -> which is expensive!

commuting behaviour - not necessarily a 2-way ride (a so called closed peak-time ‘loop’), can be only in one directon (due to possible scarcity/abundance of bikes at the start/end dock)

Contribution 1 - a new technique for deriving customers’ workplace areas and labelling commuting journeys, based on a spatial analysis of travel behaviours. (-> spatial + temporal used combined and not separately)

Contribution 2 - a visual analytics approach that facilitates a data-driven discourse between a diverse set of stakeholders in a project (data analysts, domain scpecialists, etc.) ->  a process of chauffeuring???

---
## Paper 3
---
### "Community Structures, Interactions and Dynamics in London’s Bicycle Sharing Network"
#### [Fernando Munoz-Mendez](https://www.researchgate.net/profile/Fernando_Munoz_Mendez), [Konstantin Klemmer](https://warwick.ac.uk/fac/sci/dcs/people/research/u1690815), [Ke Han](https://www.imperial.ac.uk/people/k.han), [Stephen Jarvis](https://www.dcs.warwick.ac.uk/people/academic/Stephen.Jarvis/)
##### AECOM, University of Warwick, Alaan Turing Institute, Imperial College London, UK 
###### August 2018

[LINK](https://arxiv.org/pdf/1804.05584.pdf)

![Markdown Image][3]


Suggestion: instead of pure unsupervsed learning, use extended layers of urban systems (e.g. amenities? and weather data)

Suggestion: more holistic approach needed to draw meaningful conclusions (e.g. use other transportation networks or include further cities)

Suggestion:  address time-varying networks of bike stations and communities, where different
motifs (loop, chain, star) and temporal evolution dynamics with extended time windows could potentially provide deeper insights into inherent relationships of spatially heterogeneous nodes (stations) or sub-networks (communities)








[1]: /assets/images/paper1.png
[2]: /assets/images/paper2.jpg
[3]: /assets/images/paper3.png
