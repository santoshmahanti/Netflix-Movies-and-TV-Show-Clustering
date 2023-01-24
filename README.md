# Netflix Movie and TV Show Clustering
Netflix is the world's largest online streaming service provider, with over 220 million subscribers as of 2022-Q2. It is crucial that they effectively cluster the shows that are hosted on their platform in order to enhance the user experience, thereby preventing subscriber churn.

## Table of Content
  * [Problem Statement](#problem-statement)
  * [Objective](#objective)
  * [Dataset](#dataset)
  * [Data Pipeline](#data-pipeline)
  * [Project Structure](#project-structure)
  * [Conclusion](#conclusion)


## Problem Statement
In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. 
It will be interesting to explore what all other insights can be obtained from the same dataset.
We will be able to understand the shows that are similar to and different from one another by creating clusters, which may be leveraged to offer the consumers personalized show suggestions depending on their preferences.


## Objective
The goal of this project is to classify/group the Netflix shows into certain clusters such that the shows within a cluster are similar to each other and the shows in different clusters are dissimilar to each other.


## Dataset
The dataset is collected from Flixable which is a third-party Netflix search engine. This dataset consists of tv shows and movies available on Netflix as of 2019. It includes over 7787 records and 12 attributes. Each attribute is provide information about movies/TV shows. 

## Data Pipeline
1. Analyze Data:
   - In this initial step we went to look for different features available and tried to understand the
data . During this stage, we looked for the shape of data, data types of each feature, statistical summary etc.
2. EDA:
   - EDA or Exploratory Data Analysis is the critical process of performing the initial investigation on the
data. So, through this we have observed certain trends and dependencies and drawn certain conclusions
from the dataset that will be useful for further processing
3. Data Cleaning:
   - Checked duplicated values present in the dataset. After that comes the null value and
outlier detection and treatment. For the null values imputation we simply replace with empty string and
drop some of the null rows then analyze outlier and handling.
4. Textual Data Preprocessing: 
   - During this stage, cluster the data based on the attributes: director, cast,
country, genre, rating and description. Data preprocessing include Remove all stop words and punctuation
marks, convert all textual data to lowercase. Stemming to generate a meaningful word out of corpus of
words. Tokenization of corpus and Word vectorization. We used Principal Component Analysis (PCA) to
handle the curse of dimensionality.
5. Clusters Implementation: 
   - Use K Means and Agglomerative Hierarchical clustering algorithms to cluster
the movies, obtain the optimal number of clusters using different techniques.
6. Build Content Based Recommendation System:
   - A content based recommender system was built using
the similarity matrix obtained after using cosine similarity. This recommender system will display 10
recommendations to the user based on the type of movie/show they watched.
    


## Conclusion
In this project, we worked on a text clustering problem wherein we had to classify/group the Netflix shows into certain clusters such that the shows within a cluster are similar to each other and the shows in different clusters are dissimilar to each other.

*	It was interesting to find that majority of the content available on Netflix is Movies.
*	But in the recent years it has been focusing more on Tv-Shows.
*	United States and India are among the top 5 countries that produce all of the available content on the platform.
*	Also 6 of the actors among the top ten actors with maximum content are from India.
*	TV-MA tops the charts, indicating that Most content on Netflix is rated for Mature Audiences and over 14 years old
*	Most movies on Netflix have a duration range from 90 to 110 minutes
*	Most TV shows on Netflix have a span of only one season
*	We first built clusters using the K-Means Clustering algorithm, and the optimal number of clusters came out to be 6. This was obtained through the elbow method and Silhouette score analysis.
*	Then clusters were built using the Agglomerative clustering algorithm, and the optimal number of clusters came out to be 12. This was obtained after visualizing the dendrogram.
*	Using the given data a simple recommender system was created using cosine_similarity and recommendations for Movies and Tv Shows were obtained.
