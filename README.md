# Multivariate-Time-Series-Analytics
*Analysis of multivariate time series data in R*

This project was completed in partial requirement of the course FOUNDATIONS OF DATA SCIENCE (CS F320) offered during Second Semester 2019-20 at BITS Pilani, Pilani Campus.

The aim of this project was to analyse multivariate time series data by identifying and implementing an application for each of an MVTS regression, classification and clustering algorithm.

## What are Multivariate Time Series (MVTS)?
```
Multivariate time series have more than one time-dependent variable. Each variable depends not only on its past values but also has some dependency on other variables.
```
## 1. MVTS Regression Algorithm
We looked at **_Vector Auto Regression (VAR)_** - a multivariate forecasting algorithm that is used when two or more time series influence each other. It was used to implement regression on MVTS data. 

Using our dataset of Air Quality we predicted the future air quality index values based on the past data and observed that VAR is a robust model to predict future values for MVTS data.
## 2. MVTS Classification Algorithm
We then shifted our focus to MVTS classification problem and observed that due to dependencies among variables, only the k-NN algorithm would work well. 

To measure similarity in the "Nearest-Neighbour" approach, we deployed the euclidean distance measure but realised that it is insufficient since it is prone to errors when encountering distortion in the time axis. Thus we applied **_Dynamic Time Warping to euclidean distance_** to improve the accuracy. 

To reduce the quadratic time complexity of DTW, two approaches were used- first. A locality constraint was imposed upon the time series and second, LB Keogh lower bound method was used. This algorithm was applied on the EEG eye dataset using a single-nearest neighbour approach and binary classification results were obtained.
## 3. MVTS Clustering Algorithm
Our final task required us to cluster similar time series together. For this we used the already-existing **_k-means algorithm_**. 

The aim was to cluster similar companies in the S&P 500 index based on their historical stock prices dataset. As with classification, DTW euclidean distance was used to measure distance and sped up with the use of locality constraint and LB Keough lower bound method. 

The number of clusters was set beforehand and so was the initial choice of seeds. After a reasonable number of iterations, similar time series were clustered together.

#### Want to know more?
Please read the [project report](https://github.com/Vitthal98/Multivariate-Time-Series-Analytics/blob/main/FoDS_Report_%232.pdf) as it contains detailed information about the datasets used, methods implemented, results obtained and discussion.

For any doubts don't hesitate to contact me at vitthalbhandari98@gmail.com

If you find our work helpful, do not forget to :star: the repository!
