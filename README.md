# Factorization Machine Algorithm with Explicit Feedback #
---
[AWS Docs](https://docs.aws.amazon.com/sagemaker/latest/dg/fact-machines.html)

This example shows how to perform training and inference with SageMaker's built-in Recomendation Machine algorithm.

The method we will use is a Factorization Machine regression. Factorization Machine is a general-purpose supervised learning algorithm that you can use for classification and regression tasks. It is an extension of a linear model that is designed to parsimoniously capture interactions between features in high-dimensional sparse data sets. For example, in a click prediction system, the Factorization Machine model can capture observed click rate patterns. Factoring machines are a good choice for tasks related to high-dimensional sparse data sets, such as click prediction and item recommendation.

The Amazon SageMaker Factorization Machine algorithm provides a robust and highly scalable implementation of this algorithm, which has become extremely popular in ad click prediction and recommendation systems.

![FM](https://cdn-images-1.medium.com/max/1200/1*LIUoxYjroygCiS5UhrMk4w.png)

## Data
---

[F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19.](https://dl.acm.org/doi/10.1145/2827872)

MovieLens data sets were collected by the GroupLens Research Project at the University of Minnesota.
 
This data set consists of:
* 100,000 ratings (1-5) from 943 users on 1682 movies. 
* Each user has rated at least 20 movies. 
* Simple demographic info for the users (age, gender, occupation, zip)

The data was collected through the MovieLens web site (movielens.umn.edu) during the seven-month period from September 19th, 1997 through April 22nd, 1998. This data has been cleaned up - users who had less than 20 ratings or did not have complete demographic information were removed from this data set. Detailed descriptions of the data file can be found at [link](https://files.grouplens.org/datasets/movielens/ml-100k-README.txt).


Variables in the dataset [ua.base](./ml-100k/ua.base) and [ua.test](./ml-100k/ua.test): 
* **userId** = unique identifier of the user.
* **movieId** = unique identifier of the movie.
* **rating** = User rating of the movie (1-5).
* **timestamp** = date variable.

## Notebooks
---

1. [Recommendation-Machine-Explicit.ipynb](Recommendation-Machine-Explicit.ipynb)
    * Introduction
    * Prequisites and Preprocessing
    * Training the model
    * Perform Batch Inference
    * Perform Real-Time Inference
    
    
2. [Recommendation-Machine-tuning-Explicit.ipynb](Recommendation-Machine-tuning-Explicit.ipynb)
    * Prerequisites and Preprocessing
    * Perform Hyperparameter Tuning of the Model
    * Perform Batch Inference with the best Model
