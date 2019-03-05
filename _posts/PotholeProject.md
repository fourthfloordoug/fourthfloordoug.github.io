# Pothole Project Proposal

## Summary

Potholes constitute a significant fraction of both the DC city budget and the interaction of city residents with their local government.  Currently potholes are reported to the city through use of the 311 system, where locations and status are published by the city.  This project seeks to derive historical trends in pothole formation within the city and an understanding of the influence of various parameters affecting their formation.  As a long term goal, this project will seek to provide a tool for the city to be able to predict the location and intensity of potholes deriving from these parameters.  The project will seek to augment the capabilities of DDOT in this effort.  Using the wide variety of data available to Code for DC, this project will seek to positively impact the city services it studies as well as provide opportunity for Code for DC volunteers to utilize cutting edge data analysis tools.     

## Background

### An ode to the '90's

My mom was the bookkeeper for the township where I grew up in western Pennsylvania.  We lived effectively next door to the building that housed the township offices, police station, and public works garages.  I say effectively, because this was a fairly rural area at the time, so it was a bit of a walk, but not too far at all.  In fact, my bus stop for all 12 years of school was right out front of this building.  As we lived so close, I was the office kid who was around all the time waiting for my mom to get off work and knew everyone on staff.  When I got old enough to want a summer job, it was natural that I would go to work with the township road crew.  

It's not a job that I put on my resume now 25 years later, and most people I tell about it are kind of surprised.  First, I don't think many people in the circles that I'm in at this point know anyone who has ever worked this type of job.  While today, I might be someone with advanced degrees from private schools and in a "thought-based" job.  Back then, I was a kid with working class parents who was going to be the first in his family to go to college.  Second, people probably don't trust me to operate heavy equipment.  Frankly, I don't either.  Still it was an education.  Being responsible for punching a time card for the first time in my life, being on the front lines of government services, learning about working in a union shop, it was a worthwhile experience to gain new perspectives on the world.  Not saying I would work there again for $5 an hour, but back 25 years ago, it was a good gig.  

Much of my time was spent waving a flag to control traffic.  People I tell about this job now are upset to find that our crew was small enough that we didn't actually have one of those reversible "Stop"/"Slow" signs.  Trust me, I am too.  When I wasn't doing that, I was mowing grass at the community park.  But in nooks and crannies of my schedule, usually when one of the regular guys was on vacation, I was pushing asphalt.  My township had moved towards contracting out full repaving jobs to local companies, but the Public Works Department still did patching.  On these days, we'd drive out to a designated street and park all of our trucks at one end.  One guy, usually Frank (He was a guitarist in a metal band in his free time and kind of looked like Frank Zappa) would drive the big dump truck to the asphalt plant to fill up the bed, while the rest of us waited around trying to look not too lazy as some passer-by might call the office. When he came back, we would dutifully fall in line behind the truck, lutes in hand, filling up all the potholes and cracks we could find.  The steamroller would be at the back of the line to finish the job.  We would march down the street or through a neighborhood like this, taking breaks when the truck had to go refill with asphalt, or at lunchtime.  When the street was done, we moved onto a different one that afternoon or the next day.  The plan of attack was driven by calls to the office, location of important people's houses, and some vague system of what sections of the township you'd cover from year to year.  People knew that winter conditions affected street conditions, but that wasn't tightly coupled to the budget, and no one really knew what was coming next.  

### Identifying the Opportunity

The smell of asphalt still brings back memories of those days, and also reminds me that I probably lost more than a few brain cells from the asphalt itself and the gasoline that we used to clean our equipment at the end of the day.  Still, it wasn't surprising to me that I took interested in this article:

[WTOP:  Record Rainfall Worsened DCs Pothole Problems](https://wtop.com/dc/2019/02/record-rainfall-worsened-dcs-pothole-problems-costly-settlements-included/)

and started thinking about how you could combine the data available (or possibly available) with the Code for DC data portal to form a project that could be useful to the city or its residents.        

It seems based on the article that there isn't that not a whole lot has changed in the 25 years since I was doing my best not to get run over.  People call in complaints about potholes to 311, the city tracks them, and tries to get out to them in a certain amount of time.  There is a published map on the DC data page of the pothole 311 calls which tells which ones they've gotten to:

[DC Pothole Map](https://ddot.dc.gov/potholes)

This is an advance over my experience, but isn't overly involved, and probably involves a large amount of running around for the workers.  Street repair is reported to cost a fair amount of money in terms of materials, people, and equipment.  Further, in DC it seems that residents can reach a settlement with the city if their car is damaged by a pothole, leading to further costs.  As mentioned in the article, the weather matters, but it's cited as a given with no formal relationship specified.   

## Proposed Effort

### Potholes from Data Analytics

Back in the dark ages of the mid-90's, it would have been difficult to obtain the types of data that could have shed insight into these problems.  Today, however, this is not the case.  We know, because we have the data, that the city has a collection of 311 call data for potholes.  We can look historically to see how sets of potholes have evolved over time.  Further, because we have all of the 311 data for all resident concerns, we can identify calls that are related, or may be related in the future to pothole concerns, e.g. street cleanliness, standing water, snow removal, construction equipment, etc.  Weather data is available and can be matched to historical 311 information to draw trends on when and how much rain and snow matter.  Additional data could be brought to bear such as construction permits, water/sewer projects, and traffic flows to indicate likely trouble spots in the future.  Finally, budgetary information could be matched to these sets as well to determine the fiscal impact of potholes.     

### Detecting Potholes with Sensors

Stretching beyond typical "big data" analytics, there is also interest in the problem of potholes from the computer vision and autonomous driving communities.  (Note that I have a very dim opinion on autonomous driving in real practice, but I do appreciate that they push a lot of money into this type of research.)  A quick search provides several articles that employ various types of sensors on cars to identify when and where cars are hitting potholes.  Some articles use somewhat lower intensity sensors that could be available in phones to identify potholes through up/down and vibrational motions in cars.

[Road Surface Monitoring Using Smartphone Sensors](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6263868/)

[Gap Trap: A Pothole Detection and Reporting System Utilizing Mobile Devices](https://www.cs.umd.edu/sites/default/files/scholarly_papers/Burgart.pdf)

While others utilize car mounted optical sensors to see potholes.

[Pothole Detection: An Efficient Vision Based Method Using RGB Color Space Image Segmentation](https://www.researchgate.net/publication/317358184_Pothole_Detection_An_Efficient_Vision_Based_Method_Using_RGB_Color_Space_Image_Segmentation)

There is some discussion on using remote sensing to discover potholes as well:

[Pothole Detection and Road Condition Assessment Using Hyperspectral Imagery](https://www.ugpti.org/smartse/research/citations/downloads/Jengo-Potole_Identification_using_HSI-2005.pdf)

[Detection of Asphalt Pavement Potholes and Cracks Based on the Unmanned Aerial Vehicle Multispectral Imagery](https://ieeexplore.ieee.org/document/8454262)

A city such as DC possesses a great deal of traffic camera data that might be employed for this type of work.  Further, other more traditional remote sensing could be used.  The city publishes lidar data of the environment, which would have final spatial resolution, but time sequences would be important.  Additionally, satellite data is now (or becoming) available for the majority of Earth's surface with rapid refresh rates.  Planet Labs claims that it can or will so offer 3m resolution data with daily updates.  While potholes are typically smaller than this size, techniques in super-resolution are available as well as the fact that temporal changes in surface color may provide equally relevant information to the changing material composition of the surface.  

### Predicting Potholes

While I have not to this point dug deeply into the literature of pothole prediction, there are a small number of interesting articles available on the web.  It seems that Kansas City, MO has hired a data firm to perform the study that I'm outlining here.  

[To Combat Potholes Cites Turn to Technology](http://www.govtech.com/fs/infrastructure/To-Combat-Potholes-Cities-Turn-to-Technology.html)

No results seem to have been released at this point, but that effort could provide some boundaries of the possible for this work.  Further, a paper released by a group in Indiana dives deep into the material properties of road surfaces to predict how and why road surfaces degrade.

[Algorithm and Software for Proactive Pothole Repair](https://docs.lib.purdue.edu/cgi/viewcontent.cgi?article=3140&context=jtrp)

### Benefits to DC and Code for DC Volunteers

This proposed project is similar in many respects to the Rat Hack.  It aims to take 311 data that is published by the city and develop upon that base through the inclusion of other datasets that are possibly either not being used by or unavailable to the city.  In that sense, I expect to be able to provide value to the city through further knowledge of a larger, but somewhat opaque portion of the city's budget and responsibilities.

In terms of the benefit to volunteers, the Rat Hack project engaged multiple volunteers in tasks ranging from data cleaning to implementation and testing of advanced statistical algorithms.  This project has the opportunity to engage with computer vision techniques including image processing and object/change detection.  Possibly this work would be done utilizing current edge technologies involving deep belief nets (DBNs) for detection, classification, and generation of imagery.    

## Initial Tasks    

* Develop Project infrastructure - github, trello board, place to hold datasets
* Identify relevant data types within 311 datasets
* Create a visualization of allowing for historical data (use what the rat hack has or foster development of something new?)
* Identify historical weather data resources
* Identify historical DC budget information relating to potholes


## Bunch of Other Links

[Pothole Patrol: How to Report Potholes in your Area](https://wtop.com/weather-news/2019/02/pothole-patrol-how-to-report-potholes-in-your-area/)

[Review of remote sensing methodologies for pavement management and assessment](https://link.springer.com/article/10.1007/s12544-015-0156-6)

[Bad weather or bad management? What’s really driving New York City’s notorious pothole problem.](https://www.informs.org/ORMS-Today/Public-Articles/June-Volume-41-Number-3/POTHOLE-ANALYTICS)

[Pothole Prognosis Spring 2018](https://wtop.com/dc-transit/2018/01/pothole-prognosis-spring-2018/)

[2018 Pothole Palooza](https://ddot.dc.gov/2018-potholepalooza)

[The Hole Story](https://www.nbcwashington.com/investigations/The-Hole-Story-294060751.html)
