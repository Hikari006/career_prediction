# Career Prediction using personality traits (OCEAN)
## Overview

The model aims to predict career paths based on personality traits (OCEAN scores) and aptitude scores. The steps involved are as follows:
1.	Exploratory Data Analysis (EDA) to understand the relationships and distributions of the data.
2.	K-means Clustering to group similar data points.
3.	K-nearest neighbors (KNN) to classify unknown data points based on the clusters formed.

## Step 1: Exploratory Data Analysis (EDA)

EDA involves visualizing the data to identify patterns, correlations, and distributions.
1.	Correlation Heatmap
o	A heatmap to show the correlation between OCEAN scores and various aptitude scores.
o	Helps in identifying which variables are strongly or weakly correlated.
 ![heatmap](https://github.com/Hikari006/career_prediction/assets/91669143/a629cfb8-c3b0-4914-a557-66b50a45d03e)

2.	Violin Plot
o	A violin plot to show the distribution of OCEAN scores by career.
o	Provides insights into the spread and density of scores across different careers.
![violinplotdistri](https://github.com/Hikari006/career_prediction/assets/91669143/6d4c2b9b-84ff-43b0-863b-ed009b403cb5)

 


3.	Pairplot
o	A pairplot to visualize relationships between numerical variables across different careers.
o	Helps in understanding the interaction between different variables.
![output](https://github.com/Hikari006/career_prediction/assets/91669143/b7d5229e-9fae-4bf8-af6d-563d06b7c03c)



4. Box Plot
•	Axes:
o	X-axis: Various scores and aptitudes, including O_score, C_score, E_score, A_score, N_score, Numerical Aptitude, Spatial Aptitude, Perceptual Aptitude, Abstract Reasoning, and Verbal Reasoning.
o	Y-axis: Score values ranging from approximately 2 to 9.
•	Observations:
o	O_score (Openness): High median with a range mostly between 6 and 8. Some outliers below 4.
o	C_score (Conscientiousness): Lower median around 4, with outliers both below and above.
o	E_score (Extraversion): High median around 8, with a wide range and a few low outliers.
o	A_score (Agreeableness): Median around 5, moderate spread with few outliers.
o	N_score (Neuroticism): Median around 6, wide range, with outliers on both ends.
o	Aptitudes and Reasoning: Numerical Aptitude has a median around 5, with a wide spread. Spatial Aptitude has a wider spread with high outliers. Perceptual and Abstract Aptitude show significant variability with high outliers. Verbal Reasoning has a high median around 7 with a few low outliers.
![boxplotdistribution](https://github.com/Hikari006/career_prediction/assets/91669143/19eb5ead-0c88-4161-922c-51354c737115)

  
  
## K-Means Clustering and K-Nearest Neighbors (KNN) Analysis
### K-Means Clustering

K-Means clustering is applied to partition the career data into distinct clusters based on the scores and aptitudes. Here’s an outline of the steps involved:
1.	Data Preprocessing:
o	Standardize the scores and aptitudes to have a mean of 0 and standard deviation of 1.
2.	Choosing the Number of Clusters:
o	Use methods like the Elbow Method or Silhouette Analysis to determine the optimal number of clusters.
3.	Applying K-Means:
o	Fit the K-Means algorithm to the standardized data.
o	Obtain the cluster centers and labels.


### K-Nearest Neighbors (KNN)
After clustering, KNN can be applied to predict the career of an unknown data point based on its proximity to the clusters:
1.	Training KNN:
o	Use the labeled data (from K-Means clusters) to train the KNN algorithm.
2.	Predicting Career:
o	For a new data point, calculate the distance to all points in the training set.
o	Assign the career based on the majority class of the nearest neighbors (determined by the chosen 'k').
 
![scores](https://github.com/Hikari006/career_prediction/assets/91669143/634a9bb6-0a8e-4f38-a84d-3758f1d3a8a6)
FIG: METRICES (accuracy , f1,recall,precision scores)


![confusion_matrix_testvspred](https://github.com/Hikari006/career_prediction/assets/91669143/fb59f660-8cd9-4f51-9d43-38aa82054ec1)
FIG: CONFUSION MATRIX (truth vs predicted)


![elbow](https://github.com/Hikari006/career_prediction/assets/91669143/de6ca9fb-bc7d-4693-bb4f-e38d19bad202)
FIG: DETERMINATION OF K (ELBOW METHOD)


![career_detection](https://github.com/Hikari006/career_prediction/assets/91669143/6f9908cd-9861-4cf1-932e-5c9d88d40147)
FIG: CAREER PREDICTION 1

Here  as seen the based on the predicted personality trait value the careers are being fetched , So here since the cluster / group value is 1 so the career options that belong to tht cluster 1 are being showcased .. eg: journalist,lawyer , etc …


![career_detection _3PNG](https://github.com/Hikari006/career_prediction/assets/91669143/f965239f-2c1a-49dc-bc03-a9ce9242f925)
FIG: CAREER PREDICTION 2

Here  as seen the based on the predicted personality trait value the careers are being fetched , So here since the cluster / group value is 4 so the career options that belong to tht cluster 4 are being showcased .. eg: Financial Analyst ,Data Analyst , etc…


