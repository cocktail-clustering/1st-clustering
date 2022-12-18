# wholesale-clustering

## DBSCAN
Density-based spatial clustering of applications with noise

## Instructions 
1. open [`DBScan.ipynb` file in colab (link)](https://colab.research.google.com/github/ml-clustering-proj/wholesale-clustering/blob/dbscan/DBScan.ipynb)

2. run code
    * Runtime - Run all (ctrl/command+F9)

## Reasons for failure
* DBSCAN is sensitive to density of data
* Data in each column are gathered in short range of sales amount(7000-12000) <br/><img width="450" alt="image" src="https://user-images.githubusercontent.com/60884877/208306344-9905d562-0310-4032-952a-49e9f11216a7.png">
* Data are gathered in high and even density
* It is hard to find appropriate epsilon and MinPts
  * Because data are gathered in high density, slight change in hyperparameter occurs huge change in clustering result.
