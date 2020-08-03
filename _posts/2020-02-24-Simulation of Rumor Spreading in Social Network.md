---
layout: post
title: Simulation of rumor spread in social network
remark: Simulation of rumor spread in social network
author: Haomin Lin
date: 2020-02-24
tags: [course project]
---

This project is from course CSE 6730 at Gerogia Tech. In this project, me and my teammates built a software to run the simulation on rumor spreading in social networks. The rumor spreading machnism is based on [Discrete-Event Simluation](https://en.wikipedia.org/wiki/Discrete-event_simulation).

In the software, three types of roles in the social network are generated: Ignorant (I) who isn't aware of the rumor, Spreader (S) who believes in the rumor and spreads the rumor with others, Truther (T) who is aware of the rumor and talks to others to defend the truth. Anyone aware of the rumor would be a Truther or Spreader, but not necessarily someone who wants to communicate with others, therefore, a Stifler (R), which is divided into RS and RT. Those nodes not stiflers would keep communicating with others and keep the rumor spreading until they are stifled.

In the simulation, each one is seen as a queue where people wanting to talk to him waiting in queue, only after the former conversation finishes can someone waiting in the queue to initiate a new conversation with the person of interest. Therefore, this constructs a discrete event simulation.

<p align="center">
  <img  src="/img/sna/system.png"
  alt="DES system plot" style="border:1px solid black" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">An image of how a queue works in Discrete Event Simulation in our project</p>

With this machnism, we built a software consisting of modules computing combination of both sides of conversations, one's nearest friends, transformation of nodes in the graph, and introducing new nodes into the graph.

<p align="center">
  <img  src="/img/sna/software.png"
  alt="software modules" style="border:1px solid black" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">Software modules of rumor spreading simulation</p>

In the results, the Truthers and Spreaders will greatly affect people around them, and the increasing trend of the number of stiflers in the network also fits the trend in related research work. The rumor spreading will automatically stop as active people in the network are all tired of sharing rumor of truth.

<p align="center">
  <img  src="/img/sna/stifler.jpg"
  alt="software modules" style="border:1px solid black" width="700">
</p>

<p style="text-align:center;font-family:'Courier New';font-size:14px">Results of how the number of stiflers increases</p>


