# A/B Test Analysis Project
This project involves analyzing the results of an A/B test conducted by an e-commerce website. The goal is to help the company make a decision regarding the implementation of a new page or the retention of the old page. The analysis involves various statistical techniques and regression modeling.

## Table of Contents
## Introduction
### Part I - Probability
### Part II - A/B Test
### Part III - Regression
##Introduction
A/B tests are commonly used by data analysts and data scientists to compare the performance of different versions of a webpage or application. In this project, we will explore the results of an A/B test conducted by an e-commerce website. The aim is to determine if the new page leads to more conversions, if the old page should be retained, or if the experiment should be extended for further analysis.

## Part I - Probability
In this section, we examine the basic statistics and probabilities associated with the dataset.

We start by importing the necessary libraries and reading the dataset (ab_data.csv). We explore the top few rows of the dataset and answer questions related to the dataset, such as the number of rows, unique users, proportion of users converted, and the number of times the new page and treatment group don't align.

Next, we handle the rows where the treatment group is not aligned with the new page or the control group is not aligned with the old page. We create a new dataset (df2) by removing these mismatched rows and verify that the correct rows have been removed.

Using df2, we answer questions about the number of unique user IDs, identify the duplicated user ID, provide information about the duplicate row, and remove one of the duplicate rows.

We calculate the probability of an individual converting regardless of the page they receive, as well as the conversion probability for the control and treatment groups separately. We also calculate the observed difference in conversion rates between the two groups.

## Part II - A/B Test
In this section, we simulate the null hypothesis and perform hypothesis testing based on the provided dataset.

We define the null and alternative hypotheses based on the assumption that the old page is better unless the new page proves to be definitely better at a Type I error rate of 5%.

We simulate a sampling distribution under the null hypothesis and calculate the conversion rates for both the old and new pages. We also determine the sample sizes for each page.

Using the simulated values, we calculate the observed difference in conversion rates and simulate 10,000 differences to create a sampling distribution. We plot a histogram of the sampling distribution and compare it to the observed difference.

We calculate the p-value, which represents the proportion of simulated differences greater than the observed difference. Based on the p-value and the significance level, we evaluate whether there is sufficient evidence to reject the null hypothesis.

Lastly, we use built-in functions to calculate the number of conversions and the number of individuals for each page. We then use the stats.proportions_ztest function to compute the test statistic and p-value. We compare the results with the previous findings.

## Part III - Regression
In the final part, we perform regression analysis to determine if there is a significant difference in conversion based on the page a customer receives.

We identify that logistic regression is appropriate for this case since the outcome variable is binary (conversion or no conversion).

We add an intercept column and a dummy variable column for the page received by each user. This allows us to fit a logistic regression model.

Using statsmodels, we import and instantiate the logistic regression model. We fit the model using the intercept and the ab_page column.

We examine the summary



