---
layout: post
title: Revealing Gendered Language in Job Descriptions
remark: Revealing Gendered Language in Job Descriptions
author: Haomin Lin
date: 2020-05-02
tags: [course project]
---

This project is from course CSE 6240 at Gerogia Tech. In this project, I worked with two teammates to study the relationship between gendered language usage in job descriptions and salary level, industry, company, location. My part is to analyze how gender scores vary in different salary levels and industries.

I scraped data from Indeed.com to collect job descriptions from 100 cities in United States and integrate all the data into a dataset of 300 thousand job descriptions. But a number of job description doesn't have salary information. Therefore, I implemented [Ensemble Learning](https://en.wikipedia.org/wiki/Ensemble_learning) to make predictions on the salary level of each job description and achieved an accuracy score of 87.1%. This method helps to supplement over 100 thousand salary information entries for the dataset.

<p align="center">
  <img  src="/img/jd/ensemble.jpg"
  alt="Ensemble learning" style="border:1px solid black" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">Ensemble learning structure</p>

To categorize the job description into 16 industries, I scraped typical descirptions of jobs in 16 industries from [https://www.recruiter.com/careers/](https://www.recruiter.com/careers/), and then extract the keywords of each industry. By counting the frequency of keywords from each industry in a job description, I label the job as one in the industry that has the most keywords in the job description.

With the features ready and gender score calculated beforehand, I plotted the confidence intervals of gender scores in each industry to show the gender score of each industry and salary level. Results show that IT and Finance industry are the most masculine, while Human Services and Hospitality and Tourism are most feminine industries. As for salaries, low salary level jobs are most feminine.

<p align="center">
  <img  src="/img/jd/ind_sal.jpg"
  alt="Results" style="border:1px solid black" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">Gender scores in different industries and salary levels</p>


