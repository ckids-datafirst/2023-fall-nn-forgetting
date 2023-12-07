---
title: Problem and Requirements
summary: Problem and Requirements document that will drive the work to be done in the project
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

## Introduction

Federated Learning originates from the rising concerns about data privacy and the constraints of conventional centralized machine learning approaches. It emerged as a solution to safeguard user privacy while leveraging the wealth of knowledge found in dispersed data sources.

Industries increasingly embraced this concept upon realizing its potential for cooperative learning within the bounds of data privacy regulations. Its rapid evolution owes much to progress in encryption methods, communication protocols, and decentralized optimization algorithms. Presently, Federated Learning represents an encouraging framework that facilitates collaboration among diverse entities, prioritizing the protection of confidential user information and driving advancements in privacy-focused machine learning.

## Motivation

The overall motivation for the project is to address and fix the issue of client drift in case of non-IID distributions being used to train different clients.  

## Problem for the Semester

For the semester, we had two simple goals : To establish a working federated learning network - a problem statement rooted in Engineering and the second one was to visualized how the clients drifted - to answer the question : how does one quantify this drift?

## State of the Art

We initially sought to reproduce and test the network proposed in <a href = "https://iopscience.iop.org/article/10.1088/1361-6501/acf7da/meta">FedSiM</a>. We shall report the findings in the subsequent sections. We were also fascinated by the amazing math based proof for fixing client drifts in <a href = "https://proceedings.mlr.press/v119/karimireddy20a.html">SCAFFOLD: Stochastic Controlled Averaging
for Federated Learning</a> and wanted to implement the paper's proposed system.

## Design and Approach

Though initially framed as an engineering problem, at its essence, this constituted a research project aimed at exploring and executing various academic papers to evaluate their effectiveness. Consequently, we implemented two noteworthy papers over the semester to analyze and observe their outcomes.
<br>
(1) For FedSiM paper : We built a network of Convolution Neural Networks(clients) and a Community model. Like it is proposed in the paper, we manipulated each neuron in every layer of the network with a small value to observe its overall impact on the output of the network.
<br>
(2) For the SCAFFOLD paper : We built a Federated network of convolutional neural networks and a community model. Each model was equipped with a client control variate as proposed in the paper to account and adjust for the client drift.
<br>
<img src = "scaffold_algorithm.png"/>
<br>
Like mentioned in the data section, we split each class in the following fashion to simulate non-IID dataset:

    client_a : (labels == 'T-Shirt/top') | (labels == 'Trouser') | (labels == 'Pullover')
    client_b : (labels == 'Dress') | (labels == 'Coat')
    client_c : (labels == 'Sandal') | (labels == 'Shirt')
    client_d : (labels == 'Sneaker') | (labels == 'Bag') | (labels == 'Ankle Boot')


