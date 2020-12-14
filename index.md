---
layout: page
title: Chilling Effects
subtitle: The Effects of Possible Government Surveillance on Wikipedia and Google Trends
cover-img: "assets/img/luismolinero161100068.jpg"
---
> As the world continues its exponential rate of digitization, governments have 
tried their absolute best to keep up with the rate of change. This entails 
dramatic updates to the most tried and true form of government work, spying on 
citizens.  
> Whereas before these activities were hindered by the very high human capital 
required, digitization has allowed for surveillance to break free of these 
barriers and scale on machines instead of humans. Indeed it is now possible for 
governments not only to spy on specific targets or even their citizens, but 
also spy on citizens of other countries.

-----------------------
## "In a legal context, a chilling effect is the inhibition or discouragement of the legitimate exercise of natural and legal rights by the threat of legal sanction"
Following Edward Snowden's July 2013 leaks of classified US government 
documents, the world finally started to realize the extent of the NSA's 
surveillance network. In his 2016 paper, Jonathon W. Penney showed a 
considerable drop in the 16 months after June 2013 for Wikipedia articles 
that discuss topics related to terrorism. When controlling for other factors 
such as the exogenous shock of war Penney showed a decline not only in overall 
pageviews but also a reversal of the slope in the data trend. 16 months before 
June 2013 the total number of pageviews for the articles were increasingly each 
month, right after June 2013 this trend is reversed and the total number of 
pageviews started to decline. The author attributed this to a chilling effect 
on users who were afraid of being watched by the government.
![original-plot](assets/img/paper-plot.png)

In this study, we try and verify this claim by examining the same data over a 
longer period of time as well cross-checking if the hypothesis holds with a 
seperate but similar data source that is Google Search Trends. Our initial 
hypothesis was that chilling effects do indeed happen and will be more 
pronounced in the US and in Arabic countries than in countries being less 
affected by the "war on terror" and therefore presumably the NSA surveillance.
This led us to ask the following 2 research questions

1. Are the observed chilling effects only present on Wikipedia or can they 
also be observed on Google Trends?
2. Are the chilling effects long-lasting, or do they disappear after an 
extended period of time?

<!---
2. What are the different patterns of chilling effects accross different 
languages?
-->



-----------------------
###  1. Are chilling effects also observed on Google Trends?
Although Wikipedia articles are a very popular and widely used source of 
information, it usually constitutes the second layer in an average person's 
information search. People would usually land on the Wikipedia page after 
searching for the term on Google. Therefore, we're going straight to the source 
to try and gather a more representative and complete dataset that would include 
more complex queries that involve the specific topics examined for a similar 
timeframe.  

After applying the same analysis, this is the view we got:

![google-plot](assets/img/google-plot.png)

Due to the nature of the Google Trends API, we had to use 
[EPFL D-lab's g-tab](https://github.com/epfl-dlab/GoogleTrendsAnchorBank) 
library to get calibrated results for each topic that we could aggregate on 
the same scale. As can be seen, there does not appear to be any noticeable 
chilling effects. We tried to control for exogenous shocks as well but we did 
not observe any significant ones that had significant affects on any single 
datapoint.

![indv-goog-plot](assets/img/indv-google-plots.jpeg)

This weakens the initial hypothesis somewhat and raises some new questions on 
the possible reasons of such an unexpected discrepancy between Google Search and 
Wikipedia. These effects are largely based on people's perceived levels of risks 
and not the actual risks posed. For our hypothesis to still stand there needs to
some reason people are assuming that search queries involving these terms do 
not present the same perceived risk. One possible explanation could be that 
users perceive Google searches, involving mostly results from more mainstream
sources and media outlets, with less worry  opposed to Wikipedia which might be 
perceived as a less legitimate and a shadier source of information, especially 
given the widespread campaign in the past of western schools to dissuade 
students from using Wikipedia as a valid source of information in their 
schoolwork.

### 2. Are the chilling effects long term?
One of the conclusions of Penny's paper was that there needed to be longer term 
studies in order to establish a clear chilling effect consequence. A considerable 
amount of time has passed since his paper was published and Wikipedia has kept 
publishing their pageview data. In order to also offer an even better overall 
picture, we not only took the remaining data since the paper was published 
until the present, but also take 2011 data which was not included in the paper 
for an even more robust historical view of its evolution. Sadly, there was a 
widespread Wikipedia outage between June and December 2014 causing inconsistent 
data. We decided to represent this data in our graph but disregard it in the 
regression line.

