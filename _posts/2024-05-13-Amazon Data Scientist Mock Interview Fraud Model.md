---
layout: post
title: Amazon Data Scientist Mock Interview Note
date: 2024-05-13 10:00:00 -0000
categories: blog
---

## What is the variance and bias trade-off?

### Bias 
- Deviation of a model prediction from the training data

 ### Variance
 - Deviation of a model prediction from the test data

## Does a flexibility model have anything to do with the variance and bias trade-off?
[參考資料](https://towardsdatascience.com/understanding-bias-variance-trade-offs-101-ff8f44533731)

## What the difference between boosting and bagging?
> Both Ensemble model

### Bagging
- Decreases the variance and helps to avoid overfitting
- Decision tree
- **Aim to decrease variance, not bias.**

**Implementation Steps of Bagging**
- **Step 1:** Multiple subsets are created from the original data set with equal tuples, selecting observations with replacement.
- **Step 2:** A base model is created on each of these subsets.
- **Step 3:** Each model is learned in parallel with each training set and independent of each other.
- **Step 4:** The final predictions are determined by combining the predictions from all the models.
![[bagging.png]]
### Boosting
- An ensemble modeling technique that attempts to build a strong classifier from the number of weak classifiers. It is done by building a model by using weak models in series.
- **Aim to decrease bias, not variance.**
**Algorithm:**

1. _Initialise the dataset and assign equal weight to each of the data point._
2. _Provide this as input to the model and identify the wrongly classified data points._
3. _Increase the weight of the wrongly classified data points and decrease the weights of correctly classified data points. And then normalize the weights of all data points._
4. _if (got required results)_  
      _Goto step 5_  
    _else_  
      _Goto step 2_
5. _End_
![[boosting.png]]
