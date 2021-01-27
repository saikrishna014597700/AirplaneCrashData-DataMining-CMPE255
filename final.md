# Milestone 3

## Abstract
Data Mining refers to the extraction of information from huge datasets. In this Airplane crash dataset, crash investigation and analysis of flights are done. Crashes can be caused due to various crashes like, low turbulence maintenance, pilot error, mechanical failure, bad weather etc. This paper investigates flight crashes since the 1900's. This paper investigates crashes through K-means, hierarchical and DBSCAN Clustering. Clustering helps to put objects in the same group. It helps in finding similarity among different texts. 

## Experiment/Analysis

### Preprocessing
Our dataset contains a large number of categorical variables. Many of them are disordered and many of them contain missing values. These data values are unacceptable for visualization and model building. First we recode these categorical variables to make them concise and reliable. Below are the columns that were changed. These transformations would greatly increase the model performance.

### Visualizations

1. Fatalities Per year
An overall rise in the flight crashes can be seen over the years from 1908 until 1970s. years between the 1960s until 2000s have witnessed the most crashes. The graph shows an overall declining trend in aircraft crashes from 2000 onwards.

2. Fatality Operator per trend
This graph shows the different trends of flight accidents based on operators.

### Clustering Techniques

1. K-Means Clustering for Airplane Crash Data:
We have used K-Means to group similar reasons for Airplane crashes, group them together and discover underlying patterns that are a cause for crashing airplanes. We used the ‘Summary’ column from the dataset which summarizes the reason for the crash in the form of text.

The K-Means model is applied mainly on the number/ statistics of a dataset. But here the ‘Summary’ column in our Airplane Crash dataset in text. So we did feature extraction using TF-IDF to demonstrate how important each word in the ‘Summary’ column related to the Airplane Crash Data.

Using TfidfVectorizer from sklearn, we calculated the weight related to each word in the summary column. Using the elbow method, we calculate the optimal number of clusters to be used, for the K-Means model.

We had calculated the optimat k using the Elbow method and plot a graph, for each value of a k until a predefined KMax. The optimal value of k is at the elbow of the plotted graph of the plotted graph. Once we get the optimal k, we find the most common terms from each of the clusters using the cluster centroids formed from the K-Means model. To plot a graph in 2D, we have reduced features using Principal Component Analysis. 

K-Means allows us to find the observations and the measures of variance in finally formed clusters.


2. Hierarchical Clustering:

To analyze the data in the form of nested clusters and which can be  represented as a tree, hierarchical clustering is used in this airplane crash dataset.

Performing the Hierarchical clustering on this data enabled us to view interesting observations on the survival rate for the given people who boarded the flight.

The Dendrogram is used to analyze the results after applying the hierarchical clustering to the dataset.

Then a scatter plot is plotted against the values of survival rate and number of people boarding the flight. It concludes that as the number of people boarding the flight increases, the chances of survival rate also increases.


3. DBSCAN Clustering:

DBSCAN is a density based clustering algorithm which is similar to mean shift but with more advantageous than mean shift.

DBSCAN initially has an arbitrary starting point which has not been visited and using the distance epsilon the neighbourhood of the non visited starting point is calculated. All the points which are within epsilon distance are findout. 

After calculating the different points, if the number of total points are sufficient then the clustering process is executed. The current data point is considered as the starting point in the new cluster. If otherwise, the current point will be marked as noise and in either of cases the point will be marked as visited.

Again, the current point neighbourhood points are calculated which lie within epsilon distance and the points are marked and above steps are repeated. Once all the points within the distance have been visited and marked, the process in the current cluster is done. Next one unvisited point is retrieved which leads to discovery of new cluster or noise. The process is repeated until all points are marked as visited and at the end all points have been either marked as belonging to clusters or noise. 

DBSCAN poses some great advantages over other clustering algorithms. Firstly, it does not require a pe-set number of clusters at all. It also identifies outliers as noises, unlike mean-shift which simply throws them into a cluster even if the data point is very different. Additionally, it can find arbitrarily sized and arbitrarily shaped clusters quite well.

### Models
We have worked on three models which are (i) Random Forest (ii)SVM Model and (iii) XG Boost model. 

Random Forest is an ensemble method for classification, regression which operates by constructing a multitude of decision trees.

Support - Vector Machines is a supervised learning model which is a point mapped in space so that examples of separate categories are divided by a clear gap.

XGBoost, in this model the weak learners are regression trees and each regression tree maps an input data point to one of its leafs that contains a continuous source.

## Comparisions

Clustering :  multiple types of clustering are applied to the dataset and the resulted observations are compared with each of the above clusters.

##### Hierarchical Clustering
Hierarchical clustering is applied on the features survival rate, people aboard to the flight. From the resulting clustering it is observed that as the number of people boarding the flight increases the survival rate also increases.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/hierarchical.PNG)

##### K Means Clustering

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/kmeans.PNG)

##### DBSCAN Clustering
DBSCAN clustering is applied on the features survival rate. From the results, it is evident that survival rate has been increasing over the time as the flights are safer to trave now.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/dbscan.PNG)

#### Model Comparisions
Random Forest Model : 84% accuracy is achieved using the random forest model

Heat Map For Random Forest

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/random.PNG)

SVM Model : 29% accuracy is achieved using the SVM model

Heat Map for SVM

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/svm.PNG)

XG Boost: 82.54% accuracy is achieved using the XGBoost model.

Heat Map for XG Boost
![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/XGBoost.PNG)

## Conclusion

The fatality rate has decreased and thus the survival rate of passengers have increased over time. Even though the flight crashes become more frequent during the mid 19th century however the survival rate of passengers is also showing a slight increase over the last few decades. The trends from various data features shows that the future of the aircraft is becoming more and more safer. From 2000 onwards the number of aircraft crashes are declining and are expected to go further down in coming years. On top of that, the fatality rate of aircraft accidents are also declining steadily. Thus it can be concluded based on the provided data the aircraft traveling is becoming more and more safer. 

A Random forest based prediction model predicts that the fatality rate in aircraft accidents are expected to decrease further in future based on the Severity future. Similar to previous results the prediction accuracy drops drastically as the prediction time moves further from the original data(timeline).


