---
layout: post
title: "Maps"
---

In our in-depth exploration of San Francisco's traffic landscape, we delve into the analysis of geospatial data representing start coordinates of traffic incidents. By visualizing this data in the form of a heatmap, we aim to uncover the underlying patterns and densities of incidents throughout the city. Join us as we embark on this journey to unravel the intricacies of San Francisco's traffic incident landscape.

Upon generating the heatmap, a captivating picture of San Francisco's traffic incidents begins to emerge. Scattered across the city, these incidents paint a vivid picture of the challenges faced by commuters and transportation authorities alike. However, it is the areas of highest incident densities that truly capture our attention and warrant a closer analysis.


<iframe src="html_plots/map_sf.html" width="100%" height="500"></iframe>

As we examine the heatmap, we are drawn to specific regions where traffic incidents appear to be concentrated. Prominently featured are the areas surrounding the iconic Oakland Bay Bridge, the bustling Dwight D. Eisenhower Highway, and the vital Bayshore Freeway - both integral sections of Interstate 80 and U.S. Route 101. Additionally, our analysis reveals a notable hotspot at the highway roundabout connecting Route 101 and Interstate 280.

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

The interactive map provides compelling insights into the distribution of reported incidents based on their severity levels. It is evident that the majority of incidents reported to the police fall into severity levels 1 and 2, while incidents categorized as severity levels 3 and 4 appear less frequently. This discrepancy in the distribution of severity levels suggests a potential correlation with the overall quantity of incidents.

By visualizing the data on the map, we can discern that severity 1 and 2 incidents are more prevalent throughout the city, indicating a higher frequency of less severe incidents being reported to the police. On the other hand, severity 3 and 4 incidents appear to be relatively fewer in number, suggesting a lower occurrence of more severe incidents requiring police intervention. This might be weird due to the fact that if an accident is severe, it is more likely that the police will be called to the scene. However, it is important to note that the data is based on the incidents reported to the police, and not the actual number of incidents. Therefore, the data might be skewed due to the fact that some incidents are not reported to the police. Conversely, incidents of lower severity may be underreported, potentially due to their lesser impact on public safety or the involvement of other authorities in handling such incidents.

