---
layout: post
title: Information Extraction on Advisory Reports
remark: Information Extraction on Advisory Reports
author: Haomin Lin
date: 2020-07-06
tags: [research project]
---

In this project, I worked to extract information on advisory reports from [ICS-CERT Advisories](https://us-cert.cisa.gov/ics/advisories) with Professor [Xiaojing Liao](https://www.xiaojingliao.com) and Yue Qin at Indiana University. 

In this project, my work basically consists of three parts:

- Scrape text data from ICS-CERT website, each report as a pure text file.
- Process the text data to extract key information from each advisory report and use a dictionary to store the information of each report.
- For some cases, transform the detailed text data into more simple text value describing the feature of some vulneralbilities.

In the second step, the regular expressions or string matching methods are widely used to identify valuable information in the text data, and [POS tagging](https://spacy.io/usage/linguistic-features) is also implemented to remove certain sentences that are mistakenly identified as useful information.

The results are pushed to the next level analysis of advisory reports on network security to serve as word embeddings.

*Source code is available in [Haomin's Github](https://github.com/HumasLin/Information-Extraction)