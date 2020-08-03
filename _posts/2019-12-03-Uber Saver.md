---
layout: post
title: Uber Saver
remark: Uber Saver
author: Haomin Lin
date: 2019-12-03
tags: [course project]
---

This project is from course CSE 6242 at Georgia Tech.

In this project, me and my teammate developed a tool to predict [Uber surge value](https://www.uber.com/us/en/drive/driver-app/how-surge-works/) for Uber/Lyft passengers. The tool is able to predict certain surge multiplier with conditions like weather, time, source, destination, and distance set. The dataset we used to train the model is from [Kaggle](https://www.kaggle.com/brllrb/uber-and-lyft-dataset-boston-ma).

In the beginning of the project, our team found out the data is from different kinds of services in Uber/Lyft, which makes our original plan to calculate the surge multiplier with all the data impractical. So we run a program to calculate the average price of orders in each service and calculate the surge multiplier seperately. This helps to get the distribution of surge multiplier against differnt variables, like the weather.

<p align="center">
  <img src="/img/uber/Weather.png"
  alt="Distribution of surge multiplier in different weather" width="500" title="hover text">
</p>
