---
layout: post
title: "Machine Learning"
---

Here we will explore the machine learning aspect of the project. We will be using the data we have cleaned and prepared in the previous section to train a model that can predict the severity of an accident based on the features we have selected, such as bumps, crossings, juntions, railway and etc. Firstly we will explore the correlation between the features and the severity of the accidents. Then we will train a model using the data we have prepared and evaluate the model.

<img src="assets/images/Correlation_Matrix.png" alt="Correlation Matrix" width="500"/>

To get a better understanding of the visualization we decided to divide the features into three different sets.
- Common weather metrics as in temperature, humidity, pressure etc.
- Weather conditions description as in most cloudy, scattered clouds, partly cloudy etc.
- Winding condtions including wind speed, wind direction etc.

<img src="assets/images/three_correlariont.png" alt="Correlation Matrix" width="500"/>

After analyzing the data and comparing four sets of correlations, including the one that focused on surrounding features as discussed in the previous section, we discovered that the common weather set exhibited the strongest correlation with severity. This significant finding indicates that weather conditions could play a crucial role in predicting the severity of incidents.

Based on the result above, we have build a decision tree model to further explore the relationship between weather conditions and incident severity. Decision tree as one of the predictive model is known for its explainability. With its tree structure, it provides a clear and intuitive representation of its decision-making process. By constructing a decision tree model, we could identify the most critical weather factors that contribute to the severity of incidents. This knowledge could ultimately help us develop more effective strategies to mitigate the impact of severe incidents.

<img src="assets/images/decision_tree.png" alt="Decision Tree" width="500"/>

As predictive model that built to assess the severity of traffic incidents based on common weather metrics, its performance numberaically good given accuracy is at 91.12% and precision at 83.02%. When accuracy measures the overall correctness of a model's predictions, precision measures the proportion of correct positive predictions out of all positive predictions as what we can observe in the confusion matrix, where both the true label and the predicted label were the same.

As aforementioned, decision tree can help to identify the most important features for predicting traffic incident severity and the thresholds at which these features become significant. In the tree plot, the root node splits on the precipitation feature, suggesting that it is an important feature for the model. The subsequent nodes in the tree split on other features, such as wind speed and temperature, indicating that these features are also important, but when going futher down on the tree, those features become less important while making predictions.

It is important to note that the distribution of severity in the training set is imbalanced, as indicated by previous plots. Specifically, the majority of samples belong to level 2, while the other levels are underrepresented. This imbalanced distribution could have significant impact on the performance of the decision tree model. Hence, the model is currrently only making predictions to level 2, which unfortunately makes it unpractical, and can be improved by feeding balanced data, or other methodes to eliminate this bias.

To conclude based on the above analysis the decision tree model shows promising performance in predicting the severity of traffic incidents based on common weather metrics, and this information might be usefull for the city to take actions to mitigate the impact of severe incidents.