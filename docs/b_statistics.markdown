---
layout: post
title: "Analysis"
---

We convert incident time details to datetime to examine the frequency distributions of weekdays and hours. In the resulting figures, we observe particular details: the majority of the incidents happen during the daytime, with Thursday being the most dominant weekday in our data, although only slightly edging Friday. The daily peak of incidents happens 12:00 AM every day bar Sunday.

Furthermore, we observe that December is the month with most incidents, followed by the months leading up to December. The figure also shows how May and June are plagued with traffic incidents, but sees a steep fall in July.

<img src="assets/images/datetime_1.png" alt="datetime_1">

<img src="assets/images/datetime_2.png" alt="datetime_2">

<hr class="page-content-divider">

<h3>Severity</h3>

The "Severity" column provides information about the severity of the impact of a traffic incident on the road polyline, rated on a scale of 1 (short delay) to 4 (long delay). However, there are no clear guidelines on what qualifies as a "short" or "long" delay.

Most of the logged incidents fall under Severity 2, with Severity 3 being the second most common category. On a geomap displaying the distribution of all incidents, we can see that the Severity 4 incidents are concentrated around the high-density hotspots. Notably, there are no Severity 4 incidents recorded on the Oakland Bay Bridge road segment.

By observing an animated heatmap that displays the geomap distribution of incidents according to their Severity, we can see that Severity 2 is the most prevalent category, dominating the resulting mapping shapes seen in previous geomaps. We can also see that the incidents of Severity 3 are relatively few, and mainly concentrated along the Interstate 280 roadway. It is worth noting that while we cannot examine the damages caused by each incident in detail within the scope of this project, this distribution suggests that there are rarely long delays caused by traffic incidents along the busy polylines or anywhere else in San Francisco. This may indicate that the traffic incident response procedure is effective.

<img src="assets/images/severity_1.png" alt="severity">