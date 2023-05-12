---
layout: post
title: "Maps"
---

As our project is centered around San Francisco, we'd like to firstly produce and examine a heatmap of the data. Our geodata comprises of start- and end-coordinates of latitude and longitude of the polylines affected by logged traffic incidents. We use the start coordinates to plot the heatmap.

In the following heatmap, we observe that while traffic incidents occur scattered across most of San Francisco, the highest densities can be found centered around the Oakland Bay Bridge, Dwight D. Eisenhower Highway and Bayshore Freeway (both are parts of Interstate 80 and U.S. Route 101), and the highway roundabout between Route 101 and Interstate 280.

<iframe src="html_plots/heatmap.html" width="100%" height="500"></iframe>

Through an animated heatmap, showing the geomap distribution of the incidents as per their Severity, we observe that Severity 2 clearly makes up for the resulting mapping shapes of previously shown geomaps. Another interesting point to note is the relatively few incidents of Severity 3 and their alignment along the Interstate 280 roadway. While closer examination of damages in each incident is beyond the scope of this project, an interesting observation from this distribution, is that there is rarely long delays caused by traffic incidents along the busy polylines, and even more so anywhere else in San Francisco. Perhaps the traffic incident response procedure is just that good.

<iframe src="html_plots/map_sf.html" width="100%" height="500"></iframe>

By dividing the city as per its districts, we can examine the regional incident distribution with a choropleth map.
As expected in the following choropleth map, we recognize the pattern that most incidents take place in the districts containing the abovementioned passage: Route 101, Interstate 80, and Interstate 280. The district containing the top most incidents is Southern (spanning the SoMa major neighborhood), followed by Mission District and Bayview where the densities follow Route 101 along the coastline.

<iframe src="html_plots/incident_counts_map.html" width="100%" height="500"></iframe>

Upon examining the figure, it becomes apparent that the most dense polyline stretches from the start of the Oakland Bay Bridge to the southern end of the Southern district. This observation underscores the concentration of incidents along this particular route, signifying the need for targeted attention and potential interventions.

Furthermore, the figure suggests varying incident densities in other districts based on their proximity to Route 101. Districts closer to Route 101 exhibit higher densities, indicating a potential correlation between traffic incidents and the proximity to this major road.

In the next plot we have combined the different datasets to show how the incidents are correlated with crime in the area by using clustering tecniques. 

<iframe src="html_plots/traffic_crime_locations.html" width="100%" height="420"></iframe>

The generated plot provides valuable insights into the relationship between traffic accidents and various crimes. By interacting with the plot and clicking on different crime categories, we gain a clear understanding of the number of accidents associated with each category, namely driving under the influence, traffic collision, and traffic violation arrest. Moreover, the plot reveals the specific locations in the city, identified by latitude and longitude, where these incidents occur.

By exploring the plot, we can observe the correlation between certain criminal activities and traffic accidents. It becomes evident that a portion of traffic accidents is linked to criminal behavior, particularly driving under the influence, traffic collisions, and incidents resulting in traffic violation arrests. The ability to interact with the plot allows us to delve deeper into each category, gaining a comprehensive overview of their respective spatial distributions.

By pinpointing the locations of these incidents, politicians or any other stakeholder can identify areas of concern and implement targeted measures to address crime-related traffic accidents effectively. Furthermore, the plot provides a valuable tool for law enforcement agencies to identify areas with high crime rates and traffic accidents, allowing them to allocate resources accordingly.

Last but not least, all reported incidents from San Francisco Police Department are shown in the following map. The map is interactive and allows the user to select the severity of the incidents, to get a better understanding of the distribution of the incidents which are reported to the police.

<iframe src="html_plots/incident_locations_map.html" width="100%" height="420"></iframe>

The interactive map provides insights with driving under the influence which is indicated as level 1 severity. While 2, 3 and 4 represent the original data points. We observe that while the arrests are scattered across all of San Francisco, the higher densities follow the before-mentioned high-density hotspots along Route 66.

