# Pothole Project Proposal

## Summary

Potholes constitute a significant fraction of both the DC city budget and the interaction of city residents with their local government.  Currently potholes are reported to the city through use of the 311 system, where locations and status are published by the city.  This project seeks to derive historical trends in pothole formation within the city and an understanding of the influence of various parameters affecting their formation, allowing city residents and policy makers to better understand the distribution of their budget and augment the capabilities of DDOT.  As a long term goal, this project will seek to provide a tool for the city to be able to predict the location and intensity of potholes deriving from these parameters.  Through this effort we will seek to positively impact the city services it studies and provide opportunities for Code for DC volunteers to develop and use data science skills.     

## Background

### An Ode to the Road

My mom was the bookkeeper for the township where I grew up in western Pennsylvania.  We lived next door to the building that housed the township offices, police station, and public works garages, and my bus stop for all 12 years of school was in front of this building.  My mom walked to work everyday, and I was the "office kid" who was around all the time waiting for my mom to get off work and knew everyone on staff.  When I got old enough to want a summer job, it was natural that I would go to work with the township road crew.  

People are often surprised by the fact that this was one of my first jobs.  It is unlikely that people in the white collar circles that I travel in at this point know anyone who has ever worked this type of job.  Also, people probably don't trust me to operate heavy equipment.  Frankly, I don't either.  While I am glad that I have oved on from $5 an hour and the constant chance of being a traffic fatality, it was an education.  This was my first time punching a time card, working in a union shop, and being on the front line of government services.  I carry lessons and carcinogens with me to this day.    

Much of my time was spent waving a flag to control traffic.  We were too small of a crew to have one of those reversible "Stop"/"Slow" signs.  Sad!  On some occasions, however, I was given the opportunity to push around asphalt.  Our crew didn't do big jobs, that was contracted out to companies, but the Department of Public Works was responsible for patching.    

On patching days, we'd drive out to a designated street and park all of our trucks at one end.  One guy, usually Frank (He was a guitarist in a metal band in his free time and kind of looked like Frank Zappa) would drive our largest dump truck to the asphalt plant in the next town over to fill up, while the rest of us waited around trying to look not too un-busy. (Lounging public works employees could end up on the news.)  Upon his arrival, we would fall in line behind the truck, lutes in hand,

[Picture of an Asphalt Lute]()

filling up all the potholes and cracks we could find.  The steamroller would be at the back of the line to finish the job.  We would march down the street like this, breaking for lunch or when Frank had to refill the truck.  Day after day this process continued through the summer, one street to another.  The plan of attack was driven by calls to the office, location of the houses of town politicians, and some vague plan that was supposed to cover the township over 5 years.  It was obvious that weather conditions were tied to the state of the street surface, but our efforts were not tightly coupled to these effects, and no one really knew what was coming next.  

### Identifying the Opportunity

The smell of asphalt still takes me back.  It also reminds me that I probably lost more than a few brain cells from the asphalt and the gasoline used to clean our equipment at the end of the day.  Accordingly, it wasn't surprising that I took interest in this article:

[WTOP:  Record Rainfall Worsened DCs Pothole Problems](https://wtop.com/dc/2019/02/record-rainfall-worsened-dcs-pothole-problems-costly-settlements-included/)

and started thinking about how you could combine the data available in the Code for DC Data Portal to form a project that could be useful to the city or its residents.        

The development of a 311 system to intake calls for pothole repair and to record the work that has been done is a large advance over the process flow we had 25 years ago.  The city publishies the status of open 311 pothole requests here:

[DC Pothole Map](https://ddot.dc.gov/potholes)

Still, it seems that other aspects are similar likely focusing on a large amount of running around for the workers.  Street repair is reported to cost a fair amount of money in terms of materials, people, and equipment.  Further, in DC it seems that residents can reach a settlement with the city if their car is damaged by a pothole, leading to further costs.  As mentioned in the article, the weather matters, but it's cited as a given with no formal relationship specified.   

## Proposed Effort

The proposed effort below comes in four prongs, each somewhat building upon the previous.  It would seem that even performing the first one and providing a means for publicizing the output and automating data ingest would provide benefit to many residents of the city.  Touching on all four would provide a system that was far beyond what other cities seem to possess.

### Historical 311 Data

The fact that the city uses the 311 system to collect pothole reports allows us to examine what the state of pothole repair over time.  It appears that this analysis is limited in the public domain, however.  NBC4 did a report 4 years ago on the ability of the city to respond to 311 pothole calls.  

[The Hole Story](https://www.nbcwashington.com/investigations/The-Hole-Story-294060751.html)

In this report, they looked at 3 years of data 2012-15 and determined how quickly DDOT responded to calls.  They found that a repair was made within 72 hours some 71% of the time.  They noted, however, that some potholes came back quickly and repeatedly, while others were never fixed.  DDOT explained that some of the roads were not fixed because they were scheduled to be fully resurfaced in the near future.  The graphic supplied by NBC4 doesn't capture this, and may lead to false impressions of the city's level of effort.  There also seemed to be wide disparities in the number of calls received from the different Wards.  It is unclear whether this is consistent with other 311 call rates.

In this section of the effort, we will extract pothole and related data from the existing 311 datasets possessed by Code for DC.  We will develop visualizations of this data which will allow residents to understand where potholes form, their persistence over time, and when/how they are repaired.  The visualization(s) will be published on the web so that they are freely available.

### Extending the Data Analysis

During my time working on the road crew it would have been difficult to obtain the types of data that could have shed insight into when and where potholes form. Today, however, this is not the case.  Along with the actual pothole data described above, 311 call data also contains other information that may be strongly related to pothole formation, e.g. street cleanliness, standing water, snow removal, construction equipment, etc.  We can further augment this dataset by including weather information.  The National Weather Service provides extensive historical temperature, rain, and humidity data which can be joined up with the 311 data to form short or long term models of pothole formation.  Finally, ancillary city data such as construction permits, water/sewer projects, and traffic flows, and budgetary information could be matched to these sets as well to derive input as well as monetary output parameters.

For this thread of the project, we will build upon the data collection and visualizations of the prior section by incorporating new datasets.  We will need to engineer these datasets to match features and develop models that represent important information across the sets.  This step will allow us to move towards the prediction task described below.    

### Detecting Potholes with Other Sensors

Stretching beyond typical "big data" analytics, there is also interest in the problem of potholes from the computer vision and autonomous driving communities.  (Note that I have a very dim opinion on autonomous driving in real practice, but I do appreciate that they push a lot of money into this type of research.)  A quick search provides several articles that employ various types of sensors on cars to identify when and where cars are hitting potholes.  Some articles use somewhat lower intensity sensors that could be available in phones to identify potholes through up/down and vibrational motions in cars.

[Road Surface Monitoring Using Smartphone Sensors](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6263868/)

[Gap Trap: A Pothole Detection and Reporting System Utilizing Mobile Devices](https://www.cs.umd.edu/sites/default/files/scholarly_papers/Burgart.pdf)

While others utilize car mounted optical sensors to see potholes.

[Pothole Detection: An Efficient Vision Based Method Using RGB Color Space Image Segmentation](https://www.researchgate.net/publication/317358184_Pothole_Detection_An_Efficient_Vision_Based_Method_Using_RGB_Color_Space_Image_Segmentation)

There is some discussion on using remote sensing to discover potholes as well:

[Pothole Detection and Road Condition Assessment Using Hyperspectral Imagery](https://www.ugpti.org/smartse/research/citations/downloads/Jengo-Potole_Identification_using_HSI-2005.pdf)

[Detection of Asphalt Pavement Potholes and Cracks Based on the Unmanned Aerial Vehicle Multispectral Imagery](https://ieeexplore.ieee.org/document/8454262)

A city such as DC possesses a great deal of traffic camera data that might be employed for this type of work.  Further, other more traditional remote sensing could be used.  The city publishes lidar data of the environment, which would have high spatial resolution, but time sequences would be important.  Additionally, satellite data is now (or becoming) available for the majority of Earth's surface with rapid refresh rates.  For example, Planet Labs claims that it can or will so offer 3m resolution data with daily updates.  While potholes are typically smaller than this size, techniques in super-resolution are available as well as the fact that temporal changes in surface color may provide equally relevant information to the changing material composition of the surface.

We will accomplish this step by acquiring sensor data from a variety of sources not typically engaged by the city.  In order to incorporate this data we will need to perform significant image processing tasks and implement image understanding algorithms to automate the process.  This should provide new information to the city as well as provide the Code for DC volunteers with the opportunity to utilize cutting edge tools.  

### Predicting Potholes

While I have not to this point dug deeply into the literature of pothole prediction, there are a small number of interesting articles available on the web.  It seems that Kansas City, MO has hired a data firm to perform the study that I'm outlining here.  

[To Combat Potholes Cites Turn to Technology](http://www.govtech.com/fs/infrastructure/To-Combat-Potholes-Cities-Turn-to-Technology.html)

No results seem to have been released at this point, but that effort could provide some boundaries of the possible for this work.  Further, a paper released by a group in Indiana dives deep into the material properties of road surfaces to predict how and why road surfaces degrade.

[Algorithm and Software for Proactive Pothole Repair](https://docs.lib.purdue.edu/cgi/viewcontent.cgi?article=3140&context=jtrp)

A prediction tool for potholes should have significant benefit to the city as it will be able to marshal the appropriate amount of resources for the task at hand.  Code for DC volunteers will be able to engage in significant model building activities.  We will look to publicize the results on the web with an interactive tool for users to explore.

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
