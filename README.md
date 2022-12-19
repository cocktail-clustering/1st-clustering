#K-Means Clustering

#Data Check
Loading data Wholesale customers data.csv as dataframe
and check the value of each feature.

#Preprosessing 

Normalization

For numeric features, there are some well known data preprosessing, standardlization and normalization.
Our numeric features need to be normalized so we used minmax scaler for min max normalization. 

About Outliers

After normalization, we check byplot of each features and we can find out there are some outliers-based on IQR.
So we replaced outliers with Q3 value(75% of max value) of each feature. 

(1. Normalization should be preceed after outliers are deleted, but if we preprocess the data in this order, we could not find out optimal K for kmeans clustering due to underperforming result of silhoutte coefficient.
2. If normalization is preceeded without replacing outliers, we can get appropriate optimal K=6 for kmeans clustering.
3. If we do preprosessing with replacing outliers after normalization, we still can get optimal K=6.)
괄호친 내용으로 이상치 내용 정당화 

As there was no missing value(null, NaN), skipped this step. 

For PCA, we already could get optimal K without doing this step, so skipped this step, too. 

#Finding Optimal K
- Elbow Method
- Silhoutte Coefficient
to find our optimal K, we used 2 methods mentioned above. For k in range 2 to 15, we drawed graph to check it visually.
Through these two method, we could get Optimal K -> 6 in common. 

#Clustering with k=6
Preceed clustering with k=6.
There are 2 nominal features, Region and Channel, and we can get 6 combinations from those features.
And we now can see that those 6 combinations corrrspond to 6 labels one-on-one.

