---
layout: post
title: "Analysis"
---
The introductory of the project emphasizes on exploratory analysis to gain a better understanding of the data and to investiage various categories and statistics of the traffic incidents at hand.  Our first point of interest is to investigate the incidents using datetime analysis. We consider the following figures:



<img src="assets/images/datetime_1.png" alt="datetime_1">

By converting the logged incident time details to datetime, we are able to examine the frequency distributions as per weekdays and hours. The resulting figures indicates that the majority of the incidents happen during the daytime, with Thursday being the most prevalent weekday in our data, although only slightly edging Friday. The daily peak of incidents happens 12:00 AM every day bar Sunday. Furthermore, we observe that December is the month with most incidents, followed by the months leading up to December. The figure also shows how May and June are plagued with traffic incidents, but sees a steep fall in July.

The findings are roughly in consensus with U.S standards of non-fatal crashes tend to happen during daytime [Source: [National Safety Council](https://injuryfacts.nsc.org/motor-vehicle/overview/crashes-by-time-of-day-and-day-of-week/)]. Our data comprises mainly of incidents causing intermediate delays as explained later in the Analysis-section. In conclusion, datetime analysis of San Francisco traffic incident yields that the city roughly follows the national tendencies and frequencies.

The following figure depicts the geographic distrubtion of the the incidents happening either during sunrise or sunset. The demographic shape of the incidents is further explained in the menu option "Maps". Here, the presented figure shows a rather random scatter of the incidents as per their sunrise or sunset hue. However, this visualization further reinforces our understanding that incidents are more prevalent during the day as explained earlier.

<img src="assets/images/datetime_2.png" alt="datetime_2">

The majority of accidents tend to occur during daylight hours, as indicated by the dominance of data points in that area of the plot. This observation aligns with our previous analysis, which also highlighted higher accident rates during daytime hours.

By corroborating the findings from our previous analysis, this jointplot reinforces the understanding that accidents are more prevalent during the day. However, it provides an additional layer of insight by visualizing the distribution of accidents based on their exact location.

<hr class="page-content-divider">

<h3>Severity</h3>

The "Severity" column represent the severity of the impact of the traffic incident on the road polyline, ranging from 1 (short delay) to 4 (long delay).There are, however, no given thresholds or indicators on what constitutes a "short" and "long" delay. 

<img src="assets/images/severity_1.png" alt="severity">

We observe the vast majority of the logged incidents to be of Severity 2 with a great distance to the runner up, Severity 3. The following figures displays the frequency distribution of the severity counts (left) and a geographic distribution of the incidents as per their logged severity level (left). In the geographic distribution of the incidents, we note that the slight majority of the Severity 4 incidents are centered around certain high density hotspots explained in the menu option "Maps". These include the Route 66 interstates. 

It is, however, interesting to note that there are no Severity 4 incidents on the Oakland Bay Bridge polyline, which is the highest density polyline for road incident in our data. As the data does not contain information about the damages involved in each traffic incident,, thus not allowing for closer examination of damages in each incident, an interesting observation from the displayed distribution is that there is rarely long delays caused by traffic incidents, even along the busy polylines. 

in 2014, San Francisco government pledged to eliminate traffic fatalities by 2024 through better education on public safety, stricter enforcement of traffic laws, and continously adopting policy changes. This commitment is known as the city's "Vision Zero" policy [Source: [SF Gov](https://sfgov.org/scorecards/transportation/traffic-fatalities)].

<iframe src="html_plots/severity_bokeh.html" width="100%" height="370"></iframe>

The plot indicates an upward trend in the overall number of incidents from 2016 to 2020. However, in 2021, there was a significant surge in the number of incidents compared to the previous years. Notably, this increase was predominantly observed in severity level 2 incidents.

This suggests that while the total number of incidents increased, severity level 4 incidents remained relatively lower in comparison. Severity level 2 incidents accounted for a substantial portion of the overall increase in 2021, warranting attention and further investigation into the factors contributing to this rise.

Based on the analysis, we observe a general increase in the number of incidents over the years, with severity level 2 incidents being particularly prominent in the surge witnessed in 2021. These findings emphasize the need for proactive measures to address the underlying causes of accidents, especially focusing on severity level 2 incidents, to ensure the safety of motorists and pedestrians in San Francisco.

The plots above drove us to investigate the severity of incidents in more detail. We examined the correlation among different features in the dataset to identify the factors that contribute to the severity of incidents. The heatmap below shows the correlation between the features in the dataset. Among all low correlation observed, we have found that "Stop" has the "highest" correlation comparing to other features. To highlight this correlation, we have plotted "Stop" with an 'x' on the plot.

<img src="assets/images/severity_indicator.png" alt="severity_2">

It is understandable that it may not necessarily display Severity and 4 incidents with x'es due to the sheer amount of Severity 2 incidents. An alternative approach would be to assign different weights to the incidents as per their severity, however, this is beyond the scope of the project. For now, the finding concludes that the relationship between nearby "STOP" signs and an incident has the highest correlation, but we note that this does not correlate to most incidents being directly related to this correlation - only that this particular feature amongst all of the features in the dataset was found most prevalent in connection to the incidents.

As correlation famously not does equal to causation, these findings prompt further investigation of confounding elements. In the menu option "Maps" we investigate traffic incident relation to crimes, using city government's self-published crime data. As we dive deeper into the correlation dimension, we note the need for further types of correlation to be investigated before any definitive conclusions can be reached