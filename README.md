# wholesale-clustering

## Purpose

- Clasifying sales data with given 8 features and giving appropriate sales idea with the result.
- Use unsupervised learning – Hierarchical Clustering, DBSCAN, K-Means Clustering.

 ## File Directory ## 
 
 ```shell
wholesale-clustering
├── data
│   └── Wholesale customers data.csv               # 연간 고객 판매량 데이터 csv
├── wholesale-kmeans.ipynb                         # 반소희, 이서린 : K-Means Clustering
├── wholesale_hierarchical.ipynb                       # 장아연 :  Hierarchical Clusterin
└── DBSCAN                        # DBSCAN
```

## Methods

1. load data
2. check missing value
    - As there was no missing value, skipped this step. 
3. preprosessing 
    - numeric feature
        - normalization
            - For numeric features, there are some well known data preprosessing, standardlization and normalization.
            - Our numeric features need to be normalized so we used minmax scaler for min-max normalization. 
        - outliers
            - After normalization, we check byplot of each features and we can find out there are some outliers-based on IQR.
            - So we replaced outliers with Q3 value(75% of max value) of each feature. 

    - categorical feature
        - Use one-hot encoding to train machine learning model.

4. Finding Optimal k
    - Elbow Method
    - Silhoutte Coefficient
        - To find our optimal K, we used 2 methods mentioned above. 
        - For k in range 2 to 15, we drawed graph to check it visually.
        - Through these two method, we could get Optimal K = 6 in common. 

5. Clustering with 6 clusters
    - Use Kmeans, DBSCAN, Hierarchical clustering to clustering data.
    - Preceed clustering with k = 6.
    - There are 2 nominal features, Region and Channel, and we can get 6 combinations from those features.
    - And we now can see that those 6 combinations corrrspond to 6 labels one-on-one.

## Analysis Clusters

- 6 clusters are created.
     |KMeans||Hierarchical|
     |:--:|:--:|:--:|
     |<img width="458" alt="image" src="https://user-images.githubusercontent.com/67853616/208429251-594212a2-06e6-4822-9e7c-7610af16d59a.png">|<img width="725" alt="image" src="https://user-images.githubusercontent.com/67853616/208429373-e6de6c0a-72ed-427b-9ce6-7f2430101c5f.png">|<img width="252" alt="image" src="https://user-images.githubusercontent.com/67853616/208429939-e8ddbba3-6d49-4aa9-89c2-50f959723990.png">|
     
     
     <img width="1027" alt="image" src="https://user-images.githubusercontent.com/67853616/208430130-70fb25dc-66e1-4e71-95f2-23711fc4003e.png">

     
- explain each cluster here.
<img width="1167" alt="image" src="https://user-images.githubusercontent.com/67853616/208428487-156ecac1-4067-4cfb-b38a-4dd7b246dd40.png">
<img width="1078" alt="image" src="https://user-images.githubusercontent.com/67853616/208428539-98875e56-4977-43e6-b515-08b40dba1cf3.png">


