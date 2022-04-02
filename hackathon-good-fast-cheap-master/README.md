# Project 4 Hackathon: Features Constraints
# Molovi Shuba, Kevin Peng, Kehinde Ajayi

## Table of Contents

- [Executive Summary](#Executive-Summary:)
- [Problem Statement](#Problem-Statement:)
- [Goals](#Goals:)
- [Features](#Features:)
- [Metrics/Evaluation](#Metrics/Evaluation:)
- [Recommendations](#Recommendations:)
- [Citation List](#Citation-List:)

## Executive Summary
As a group of Data Scientists, Molovi Shuba, Kevin Peng, Kehinde Ajayi was tasked to create a predictive model for salary classification above \\$50,000 and less than or equal to \\$50,000 based on numerous different features. The goal is to make the most accurate prediction given the constraint of 20 features or less. To accomplish this task different data science models and procedures will be utilized and tested to create the best model to deploy. The four chosen models were Multinomial Naive Bayes, Logistic Regression, Random Forest, and Decision Tree Classifier. After training and optimizing our parameters, the model that performed the best was the Decision Tree Classifier.

## Problem Statement: 
Create the best machine learning model to predict if someone is making less than or greater( and equal to) than 50k. The goal is to optimize as much as possible by taking the best features to put into our models.  The features will be chosen and be discussed on what we see in our EDA. We will also transform data to meet our constraint of fewer than 20 features so that we do not over dummify a column. We will also optimize by having as much data as we can to be used for our models. This means we do not want to remove missing/questionable data but rather predict what it is through model imputation.

## Goals:
Which one is the best machine learning model when you have constraints?
How well did the models do?
What was done to optimize our dataset under constraints?

## Features

| feature                      	| Data type  	| description                                                                                     	|
|------------------------------	|------------	|-------------------------------------------------------------------------------------------------	|
| capital-gain                 	| continuous 	| capital gains for an individual                                                                 	|
| hours-per-week               	| continuous 	| the hours an individual has reported to work per week                                           	|
| age                          	| discrete   	| age of an individual                                                                            	|
| capital-loss                 	| continuous 	| capital loss for an individual                                                                  	|
| education-num                	| discrete   	| the highest level of education achieved in numerical form                                       	|
| sex_Male                     	| discrete   	| biological sex of the individual is Male                                                        	|
| marital-status_group_Married 	| discrete   	| marital status of an individual is Married-civ-spouse, Married-spouse-absent, Married-AF-spouse 	|
| occupation_Exec-managerial   	| binary     	| the general type of occupation of an individual is Exec-managerial                              	|
| occupation_Prof-specialty    	| binary     	| the general type of occupation of an individual is Prof-specialty                               	|
| occupation_Other-service     	| binary     	| the general type of occupation of an individual is Other-service                                	|
| relationship_Husband         	| binary     	| this individual is someone's Husband                                                            	|
| relationship_Own-child       	| binary     	| this individual is "Own-child" (?)                                                              	|
| relationship_Not-in-family   	| binary     	| this individual is not in anyone's family                                                       	|
| relationship_Unmarried       	| binary     	| this individual is Unmarried                                                                    	|

## Metrics/Evaluation: Baseline Score: 75%  

|Model|Train Score|Test Score
|---|---|---|
Multinomial Naive Bayes|0.82|0.82|
Logistic Regression|0.84|0.84|
Random Forest|0.85|0.85|
Decision Tree Classifier|0.86|0.85|

## Recommendations:

With a training accuracy score of 86% and testing accuracy score of 85, the model that performed the best is the Decision Tree Classifier and would make the best predictions. Something to note was that 
