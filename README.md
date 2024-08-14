# Project Documentation

## Introduction

This is a Practical Application Assignment for the Professional Certification in Machine Learning and Artificial Intelligence program at UC Berkeley Executive Education

A dataset from [UCI Machine Learning repository](https://archive.ics.uci.edu/ml/datasets/bank+marketing) was used. The data is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns

----

## Business Objective


**Identify the best Machine Learning Classification model that can be used to apply the CRISP-DM methodology to determine the factors that drive the success of tele-marketing campaigns for a Banking Institution**

The evaluation of the best model will be based on the data available from the Bank's previous marketing campaigns, which highlights the acceptance or rejection of the product offered and includes personal characteristics of the customer as well as a few specifics about how the product was offered to that individual

----

## Procedure

Following the CRISP-DM methodology:

1. Business Understanding

* After reviewing the documentation and instructions provided a clear **Business Objective** was established, as stated above

2. Data Understanding

* **Exploratory Data Analysis** was performed on all features (columns) in the dataset
* Identified categorical and numerical features
* Features were deemed: necessary, appropriate, insufficient, inadequate or irrelevant
* Based on that designation, a subset of features was selected for use in modeling
 
3. Data Preparation

* Removed unselected features
* Converted and aggregated value options for some features
* Filled in missing data
* Transformed categorical features accordingly using:
  * OneHotEncoding
* Training and Testing datasets were created using **stratification** given the unbalanced classes for the target variable

4. Modeling

* Established **baseline** performance
* Compared **accuracy** and **fitting time** for the following Classification models with default configuration:


  * Logistic Regression
  * K Nearest Neighbors
  * Decision Tree
  * Support Vector Machine


* Evaluated the initial results and reassessed the data engineering process, performance metric used, and hyper-parameter options for each model
* Performed Grid Search for hyper-parameter tuning using **f1 scoring**

5. Evaluation

* Model performance was evaluated and compared between modules using:

  * **F1 score**
  * **Accuracy**
  * **Precision**
  * **Recall**
  * **ROC AUC**

* Identified best performing model and corresponding hyper-parameters
* Reviewed findings from best model to elaborate final recommendations

6. Deployment

* Established the conclusions reached from the evaluation process
* Provided recommendations base on the results

----

## Conclusions


* Based on these results, which target F1 scoring as a measure of adequacy for the model to classify the tele-marketing data, the recommendation is to use **K Nearest Neighbors** as a first option


* Considering some of the drawbacks of **KNN**, the second best option would be to use a **Decision Tree** model


* Both of these models seem to strike an acceptable balance between performance scoring, simplicity when it comes to configuring hyper-parameters, and similar fitting times that do not appear resource intensive

----

## Recommendations


* Given the challenges with such an unbalanced data set, the main recommendation is to further improve the data engineering process and apply more elaborate techniques to reduce that condition
* Cycle through the tuning process with that new set of engineered data and assess any improvement in performance, which may yield a different outcome for the best model to use
* Priority should be put on working with the two best models identified in this initial assessment

----
