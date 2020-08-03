---
layout: post
title: Uber Saver
remark: Uber Saver
author: Haomin Lin
date: 2019-12-03
tags: [course project]
---

This project is from course CSE 6242 at Georgia Tech. In this project, me and my teammate developed a tool to predict [Uber surge value](https://www.uber.com/us/en/drive/driver-app/how-surge-works/) for Uber/Lyft passengers. The tool is able to predict certain surge multiplier with conditions like weather, time, source, destination, and distance set. The dataset we used to train the model is from [Kaggle](https://www.kaggle.com/brllrb/uber-and-lyft-dataset-boston-ma).

In the beginning of the project, our team found out the data is from different kinds of services in Uber/Lyft, which makes our original plan to calculate the surge multiplier with all the data impractical. So we run a program to calculate the average price of orders in each service and calculate the surge multiplier seperately. This helps to get the distribution of surge multiplier against differnt variables, like the weather, temperature, or distance. This helps us to identify some variables that are valuable to be selected as features.

<p align="center">
  <img title="D3 visualization of prediction results" src="/img/uber/temperature.png"
  alt="D3 visualization" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">Surge multiplier distribution against temperature of the trip</p>

Then, to implement classification method, we classify the surge multipliers into 3 levels as `[1, 2, 3]`, and we also redistributed surge multiplier levels to balance the proportion of each level, so that the data won't be too biased.

With data processing done, we trained a Random Forest classifier model to predict the surge multiplier using the Python package Scikit-learn. We picked `['source', 'destination', 'hour', 'weekday', 'avg_distance', 'weather']` as features to train our model as their feature importance stands out among all other features. The model reached accuracy of 74%. Then we used the model to create prediction results by creating combinations for different cases of Uber/Lyft trips for visualization. So that we can view what the predicted surge multiplier is on different conditions.

To establish visualization, we used D3.js to create the interactive heatmap. In this heatmap, we integrated data with different destinations and sources to show predicted surge multipliers in different time slots. Apart from that, the detailed predicted value in differnt weather can also be checked when the mouse is over certain cell.

<p align="center">
  <img title="D3 visualization of prediction results" src="/img/uber/visual.png"
  alt="D3 visualization" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">D3 visualization of prediction results</p>

Although we managed to build a model at last, the limited size and range of data still stop us from getting a more general and accurate model. With the privacy policy changing, it will still get harder to make  