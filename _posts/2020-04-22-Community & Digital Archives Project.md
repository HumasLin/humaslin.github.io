---
layout: post
title: Community & Digital Archives Project
remark: Community & Digital Archives Project
author: Haomin Lin
date: 2020-04-22
tags: [course project]
---

In this project, I worked with a [Vertically Integrated Project team](https://www.vip.gatech.edu/teams/community-digital-archives-project) working on an online archive project to add image classification and sentiment scoring functions of allenarchive website.

<h1>Image classification</h1>

In Image classfication part, I located a transfer learning model online from a [Youtube video](https://www.youtube.com/watch?v=QfNvhPx5Px8), which simply asks for similar image samples to train the model. After collecting similar pictures from google and working with Docker to train the model, I connected the model with a Python notebook to execute the classification. To include cases where the map image is hidden in a small part of the whole page, I also used openCV to take out each subpage of the page for classification. The model has accuracy score over 90%.

*More details and source code can be found at [Haomin's GitHub](https://github.com/HumasLin/Allenarchive-Imageclassifier)

<h1>Sentiment scoring</h1>

In scoring comment's sentiment, I used the library from [VADER sentiment in PHP](https://github.com/abusby/php-vadersentiment), which I can use for giving each comment a sentiment score to identify whether the comment is positive or negative. It is successfully incorporated into the website, admins of the website can access the score and identify negative comments.

<p align="center">
  <img  src="/img/allen/score.png"
  alt="allenarchive sentiment score" style="border:1px solid black" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">Admins viewing sentiment scores of comments on the website</p>

*More details and source code can be found at [Haomin's GitHub](https://github.com/HumasLin/Allenarchive-commenting)