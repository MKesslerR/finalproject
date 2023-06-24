# Proposal for Semester Project


<!-- 
Please render a pdf version of this Markdown document with the command below (in your bash terminal) and push this file to Github

quarto render Readme.md --to pdf
-->

**Patterns & Trends in Environmental Data / Computational Movement
Analysis Geo 880**

| Semester:      | FS23                                     |
|:---------------|:---------------------------------------- |
| **Data:**      | Posmo Data  |
| **Title:**     | Analysis of movement patterns of dog walking                |
| **Student 1:** | Mirjam Nötzli                        |
| **Student 2:** | Margarita Kessler                        |

## Abstract 
<!-- (50-60 words) -->

## Background and Research Questions

Walking is inherently a social activity, often performed with others, and there is a sense of pleasure gained from sharing the experience. Walking can occur both as an integrative practice and a dispersed practice (Harries and Rettie, 2016). Walking as an integrative practice occurs, where the purpose of the walking is actually to experience the walk. In contrast, dispersed walking is walking that occurs as part of a different integrative practice, such as shopping or traveling to work; walking is not the purpose of the practice but a means to achieve it (Westgard et al. 2021). Walking with a dog has been assumed to be leisure time or recreational. However, dog walking can also be an integrative practice when walking is just a way to achieve the purpose of satisfying the basic needs of the dog. Westgarth et al. classify dog walks into two broad categories: functional and recreational walks. Functional walks are primarily for the purpose of meeting the needs of the dog. In contrast, recreational walks catered to both the dog owner’s needs as well as those of the dog. They constitute an integrated practice where the purpose of the walk for the owner is to enjoy the walk, not just meet the needs of the dog to have a walk. As dog walking is a specific behavior different from general physical activity or even other types of walking, it requires a context-specific approach to examining these correlates. Specifically, dog walking is determined by the physical environment, social environment, and personal and dog-related factors (Westgard et al. 2014). Certain environments and contexts are deemed more conducive to functional than recreational dog walks (Westgard et al. 2021). Here, we aim to characterize the two types of dog walking behaviors. Our research questions are the following: 

How do recreational- differ from functional dog walks?
Are dog walks influenced by weather (precipitation)? 
How do the recreational dog walking patterns differ through the day? weekdays and weekends?
How are the moving behavior patterns during dog walks?

## Results


## Data and Methods

### Data set
We tracked our own daily movement behavior with the tracking app Posmo over the course of about two months (April & May 2023. We then filtered our dog walks, which contain 25´455 data points of 103 trajeectories in total. The following attributes are part of the movement dataset of the two tracker users:

1. user_id: Name that identifies the walker     
2. datetime: Timestamp
3. weekday: Day of the week 
4. geometry: Coordinates
5. trajectoryID: Unique integer that identifies the trip
6. Type: Type of walk (functional/recreational)       
7. Shape: Shape of trajectory (axial/loop/semi-loop)   

Attributes 5-7 were manually added to the two csv files. 

Of the weather data we filtered the precipitation data of the two weather stations that are closest to the two towns of the two tracker users, which are Hinwil and Schaffhausen. We kept the three attributes that were relevant to us:

1. stn: Name of weather station   
2. time: Time
3. rco150z0: Ten minute precipitation sum

### Pre-processing
Because we were only working with data from our dog walks, we had to look at all the walks in Posmo and exclude the walking modes and segments that were not part of our dog walks. There were issues in our data that the app created duplicate time stamps with different sets of coordinates. These ereneous had to be cleaned out first. Several pre-processing steps had to be done before we could join our two movement datasets. First, we had to store the coordinates into two seperate columns (X-coordinates and Y-coordinates). Next, the precipitation data was joined to the individual movement datasets and we added a new column for rain/no rain before we joined the two data frames. We categorized trajectories that had precipitation of more than 50% of the walk as rain and no rain for values below the set threshold. A new column was added for weekday vs. weekend, as well as for the time of day (morning/evening/afternoon). 

### Analysis



## Results


## Discussion and conclussions


## References



