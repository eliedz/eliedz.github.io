---
layout: page
title: Chilling Effects
subtitle: The Effects of Possible Government Surveillance on Wikipedia and Google Trends
cover-img: "assets/img/luismolinero161100068.jpg"
---
> As the world continues its exponential rate of digitization, governments have tried their absolute best to keep up with the rate of change.
This has entailed dramatic updates to the most tried and true form of government work, spying on citizens.  

> While these activities were previously hindered by the very high human capital required, digitization has allowed for surveillance to break free of these barriers and scale on machines instead of humans.
As a matter of fact, it is now possible for governments not only to spy on specific targets or even their citizens, but also spy on citizens of other countries.

-----------------------
## "In a legal context, a chilling effect is the inhibition or discouragement of the legitimate exercise of natural and legal rights by the threat of legal sanction"
Following Edward Snowden's June 2013 leaks of classified U.S. government documents, the world finally started to realize the extent of the NSA's surveillance network.
In his 2016 paper, Jonathon W. Penney showed a considerable drop in the number of pageviews for Wikipedia articles that discuss topics related to terrorism after the NSA revelations.
When controlling for other factors such as "exogenous shocks of war" (the effect of mediatized conflicts on the number of Wikipedia pageviews for the relevant topic), Penney showed not only an immediate decline in pageviews, but also a change in the trend of Wikipedia accesses over time.
16 months before June 2013, the total number of monthly pageviews for "terrorism" articles was on the rise, and then right after June 2013 this trend is reversed and the total number of pageviews starts to decline.
The author attributed this to a chilling effect on users who would avoid accessing these topics due to being afraid of being watched by the government.

![original-plot](assets/img/paper-plot-4a.png)

The topics were picked by combining an analysis on a sample of volunteer's perception of the topics as well as a curated list from the Department of Homeland security classifying these topics as 'related to the issue of terrorism'. The author also used a comparator group of topics that are security related but not directly related to terrorism.  
In our own study, we try to verify this claim by extending the duration of the analysis, considering Wikipedia articles in other languages than English, and analysing a different but similar data source that is Google Search Trends.  

Our initial hypothesis being that chilling effects do indeed happen and we will still see their effects in the long term data.
We therefore divided our project into three targeted questions:

1. Are the chilling effects long-lasting, or do they disappear after an extended period of time?
2. Are these chilling effects language-dependent (on Wikipedia)? What different reactions to the NSA revelations are there?
3. Are the observed chilling effects only present on Wikipedia or can they also be seen on Google Trends?


-----------------------
### 1. Are the chilling effects long term?
One of the conclusions of Penny's paper was the need of longer term studies in order to confirm that the chilling effects aren't short lived.
Luckily, a considerable amount of time has passed since his paper was published and a lot more data has been gathered.
In order to offer a more comprehensive overall picture, we not only used fresh data from after the paper was published until the present, but also older data from 2010 for an even more robust historical view of its evolution. 

However, it is important to point out that our data is not perfect and does present some anomalies.
Most notably, the API that we used combined data from two different data sources, the official Wikimedia API (starting in 2016) and another website for legacy data.
In fact, a lot of articles show 0 pageviews for some days before 2016, which even with chilling effects would not be realistic.

![missing-wiki](assets/img/missing-data-wiki.png)

We can see a considerable spike in the amount of missing data during the period between month 55 and 60.
Accordingly, we decided to disregard these months in our regression analysis to avoid biasing the results.
Our analysis will also be two fold, one until the end of 2015 and another untill 2019, this is to take into account the change in API and the possibility of inconsistent data.

<!---
<html><head>
    <style>
body {
    margin-left: auto;
    margin-right: auto;
}
.dropdown-wrapper > div {
    border: 1px solid;
}

.dropdown-wrapper-child {
    margin: auto;
    display: flex;
}

.dropdown-wrapper-child div {
    flex-grow: 1;
    width: 0;
}

.dropdown-wrapper {
    display: inline-block;
}
    </style>

</head><body><div class="dropdown-wrapper">
    <select class="dropdown-wrapper-child" id="ProjectsDropdown">
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
    </select>
</div>
 <object id="plot" style="height: 450pt;width: 100%;" type="text/html" data="assets/html/sample_plot.html" ></object>

<script>
    function loadProjectPlot() {
        var plot = document.getElementById("plot");
        plot.data = this.value;
        return false;
    }
document.getElementById("ProjectsDropdown").onchange = loadProjectPlot;
</script>

</body></html>
-->

![extended-wiki](assets/img/extended-wiki.png)

The results for both analyses were surprising, not only did we not see any long term chilling effects, but pageviews trend rebounds to a pre-June 2013 slope very quickly and suddenly after the last data point of the paper.
When stopping at 2015, we still see a gradually less pronounced decrease in pageviews as time goes on. Extending the data till 2019 shows an almost identical slope to pre-June 2013 levels. Although the missing data might mean the absolute number of pageviews pre-2013 was still higher, the slope is consistent and seems to have completely recovered, indicating a largely diminished chilling effect and a return to normal behavior.
Our best guess as to why that is relates to the "privacy paradox" phenomenon.  
People, when bombarded with news and reminders about government surveillance, are constantly nudged towards thinking about their privacy and how it is being infringed upon.
However, as the story is dropped from the news cycle, people's nonchalance about their privacy and being monitored resurfaces and we observe same trend as pre-June 2013 emerge.


### 2. Are these chilling effects language-dependent?
Although the NSA is a US Government agency, the US' influence as a world superpower means that everything happening in the US also affects the rest of the world. It is also worth considering that the people with the highest probability to be monitored or perceive to be monitored are immigrants and expats who might not necessarily use English Wikipedia. In addition, the leaks themselves directly mention that the espionage was not only targete at American citizens or even residents but also foreign residents as well.  

We explored the pageview data for the same articles in 6 different languages of Wikipedia in order to see the possible effects of this and help support our hypothesis.


<!---
<html><head>
    <style>
body {
    margin-left: auto;
    margin-right: auto;
}
.dropdown-wrapper > div {
    border: 1px solid;
}

.dropdown-wrapper-child {
    margin: auto;
    display: flex;
}

.dropdown-wrapper-child div {
    flex-grow: 1;
    width: 0;
}

.dropdown-wrapper {
    display: inline-block;
}
    </style>

</head><body><div class="dropdown-wrapper">
    <select class="dropdown-wrapper-child" id="ProjectsDropdown">
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
        <option value="assets/html/sample_plot.html">Sample1</option>
    </select>
</div>
 <object id="plot" style="height: 450pt;width: 100%;" type="text/html" data="assets/html/sample_plot.html" ></object>

<script>
    function loadProjectPlot() {
        var plot = document.getElementById("plot");
        plot.data = this.value;
        return false;
    }
document.getElementById("ProjectsDropdown").onchange = loadProjectPlot;
</script>

</body></html>
-->

![all-lang-plot](assets/img/all-lang-plot.jpeg)

To our continued surprise, we could not notice any significant chilling effects or downward trend that was drastically different to the comparator group. Some languages even showing the comparator group articles with a larger decrease in pageviews following June 2013 compared to the terrorism topics.   

Even though there are some obvious outliers in each language, we do not believe these could explain the lack of chilling effects symptoms as seen in the paper, some even have a higher average monthly pageview than before. The plot showing all language views aggregated should allow for the outliers to cancel each other out as they happen on different months. But, as can be seen, it also paints a similar picture and again makes us reconsider our initial hypothesis.

###  3. Are chilling effects also observed on Google Trends?
Although Wikipedia articles are a very popular and widely used source of information, they usually reside at the second layer in an average person's information search.
Indeed, one would usually land on a Wikipedia page after having searched for the term on Google.
Therefore, we're going straight to the source to try and gather a more representative and complete dataset that would include more complex queries that involve the specific topics examined for a similar timeframe.  

After applying the same analysis, this is the view we got:

![google-plot](assets/img/google-plot.png)

<!---
 <object id="plot" style="height: 450pt;width: 100%;" type="text/html" data="assets/html/sample_plot.html" ></object>
-->

Due to the nature of the Google Trends API, we had to use [EPFL dlab's g-tab](https://github.com/epfl-dlab/GoogleTrendsAnchorBank) library to get calibrated results for each topic that we could aggregate on the same scale.
As can be seen in the plot, there does not appear to be any noticeable chilling effects.
We tried to control for exogenous shocks as well but we did not observe any significant ones that had noticeable effects on any single topic.

This really puts into question the initial hypothesis and raises some new ideas about the possible causes of such an unexpected discrepancy between Google Search and Wikipedia.
Chilling effects are largely based on people's perceived levels of risks and not the actual risks posed.
For our hypothesis to still stand there needs to exist some reason people are assuming that search queries involving these terms do not present the same perceived risk. 
One possible explanation could be that users perceive Google searches, involving mostly results from more mainstream sources and media outlets, with less worry  opposed to Wikipedia which might be perceived as a less legitimate and a shadier source of information, especially given the widespread campaign in the past of western schools to dissuade students from using Wikipedia as a valid source of information in their schoolwork.  
Another possible explanation would be the introduction of "in-depth articles" by Google as well as Google Hummingbird to their search algorithm, both updates that improve Google's knowledge graph feature considerably.
Google Knowledge graphs show people information, usually from a topic's Wikipedia article, right in the search page and therefore might cause a lot of users to not need to visit the full Wikipedia page.
This has already been widely believed to have caused a [considerable decrease in Wikipedia pageviews](https://www.theregister.com/2014/01/13/google_stabs_wikipedia_in_the_front) after the features were introduced.



## What does this tell us
Neither the Google Trends data nor the extended Wikipedia data support our (and the author's) hypothesis.
In the best case scenario, the chilling effects only happen short term but eventually diminish after some time.
Another possible theory would be that these pageview drops are because of the introduction of new features to Google's search function that circumvents people's need to visit Wikipedia pages.
This caused a significant drop at the launch of the feature and then the pageviews started to increase again along with general internet usage. 
This would explain why a similar phenomenon is seen for the comparator group losing a significant amount of pageviews in the same period as well.

So in conclusion, the two possible scenarios are either that people do not care enough about their privacy, or Google has a really remarkable grip on how people use the web and visit websites, even for other huge Websites such as Wikipedia.   

Honestly, we can't really decide which scenario is scarier.
