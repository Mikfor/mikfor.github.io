---
layout: post
title: "Analysis"
---

We convert incident time details to datetime to examine the frequency distributions of weekdays and hours. In the resulting figures, we observe particular details: the majority of the incidents happen during the daytime, with Thursday being the most dominant weekday in our data, although only slightly edging Friday. The daily peak of incidents happens 12:00 AM every day bar Sunday.

Furthermore, we observe that December is the month with most incidents, followed by the months leading up to December. The figure also shows how May and June are plagued with traffic incidents, but sees a steep fall in July.

<img src="assets/images/datetime_1.png" alt="datetime_1">

In the next plot we examined the relationship between the time of day and accident occurrence. One interesting aspect we explored was the contrast between accidents that happen during the day and those that occur in darkness.

To differentiate between accidents that occurred during the day and those that took place in darkness, we added the "Sunrise_Sunset" variable as the hue. This attribute highlights the two distinct categories and enables us to compare their distributions visually.

<img src="assets/images/datetime_2.png" alt="datetime_2">

The majority of accidents tend to occur during daylight hours, as indicated by the dominance of data points in that area of the plot. This observation aligns with our previous analysis, which also highlighted higher accident rates during daytime hours.

By corroborating the findings from our previous analysis, this jointplot reinforces the understanding that accidents are more prevalent during the day. However, it provides an additional layer of insight by visualizing the distribution of accidents based on their exact location.

<hr class="page-content-divider">

<h3>Severity</h3>

The "Severity" column provides information about the severity of the impact of a traffic incident on the road polyline, rated on a scale of 1 (short delay) to 4 (long delay). However, there are no clear guidelines on what qualifies as a "short" or "long" delay.

Most of the logged incidents fall under Severity 2, with Severity 3 being the second most common category. On a geomap displaying the distribution of all incidents, we can see that the Severity 4 incidents are concentrated around the high-density hotspots. Notably, there are no Severity 4 incidents recorded on the Oakland Bay Bridge road segment.

By observing an animated heatmap that displays the geomap distribution of incidents according to their Severity, we can see that Severity 2 is the most prevalent category, dominating the resulting mapping shapes seen in previous geomaps. We can also see that the incidents of Severity 3 are relatively few, and mainly concentrated along the Interstate 280 roadway. It is worth noting that while we cannot examine the damages caused by each incident in detail within the scope of this project, this distribution suggests that there are rarely long delays caused by traffic incidents along the busy polylines or anywhere else in San Francisco. This may indicate that the traffic incident response procedure is effective.

<img src="assets/images/severity_1.png" alt="severity">

The next plot visualizes the incident counts by year, categorized according to severity levels. The severity levels range from 1 to 4, with 1 being the least severe and 4 being the most severe. Each severity level is represented by a different color in the plot.

<iframe src="html_plots/severity_bokeh.html" width="100%" height="370"></iframe>

The plot indicates an upward trend in the overall number of incidents from 2016 to 2020. However, in 2021, there was a significant surge in the number of incidents compared to the previous years. Notably, this increase was predominantly observed in severity level 2 incidents.

This suggests that while the total number of incidents increased, severity level 4 incidents remained relatively lower in comparison. Severity level 2 incidents accounted for a substantial portion of the overall increase in 2021, warranting attention and further investigation into the factors contributing to this rise.

Based on the analysis, we observe a general increase in the number of incidents over the years, with severity level 2 incidents being particularly prominent in the surge witnessed in 2021. These findings emphasize the need for proactive measures to address the underlying causes of accidents, especially focusing on severity level 2 incidents, to ensure the safety of motorists and pedestrians in San Francisco.

The plots above drove us to investigate the severity of incidents in more detail. We examined the correlation among different features in the dataset to identify the factors that contribute to the severity of incidents. The heatmap below shows the correlation between the features in the dataset. Among all low correlation observed, we have found that "Stop" has the "highest" correlation comparing to other features. To highlight this correlation, we have plotted "Stop" with an 'x' on the plot.

<img src="assets/images/severity_indicator.png" alt="severity_2">

We examined the relationship between the presence of stops and the severity of incidents. We expected that the presence of stops would be highly correlated with severe incidents, leading us to anticipate observing many red crosses (indicating stops) in areas associated with severe incidents.

In the plot above, we have not observed many red x's on the plot, which we would have expected if "Stop" was highly correlated with severe incidents. This finding suggests that severe incidents were not necessarily correlated with the presence of stops nearby, even it is already the most correlated one in this surrounding set.

This discovery implies that the relationship between stops and incident has the highest correlation, but it does not mean that most of the accidents are directly correlated with stops.

We must remember that correlation does not indicate causation. While "Stop" exhibited the highest correlation with severity in our analysis, there may be confounding variables or interactions that impact the relationship. Therefore, we cannot conclude that the presence of stops causes severe incidents based on this analysis alone.