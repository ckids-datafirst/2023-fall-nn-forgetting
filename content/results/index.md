---
title: Results
summary: The main results of the work done to date
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

## Visualization of the last layer of the model : 

So how does the softmax layer give out the classes to be predicted. It takes the activations from the last layer of the model. We took a specific class-balanced subset of the test dataset and pulled out the activations from the last layer of the model. After reducing the dimension of the activation for an instance to 2 using t-SNE, we plotted the each instance colored by its target label. If the classes are placed well apart, it visually shows that even in two dimensions, these class clusters can be separated. Not a very accurate way but makes up for a visual. After all, we are very visual beings. :)



## Discussion of Findings

Offer a discussion of the main findings using the system developed. Put the results in the context of the original problem statement and the questions that were posed.

Discuss any unexpected results, and potential explanations.

Enumerate (ideally in bullets) the most important findings, and their impact on your project goals.

## Limitations and Future Work

Discuss any limitations of the work to date, how these limitations could be addressed in future work.  Discuss what lines of work are most promising given the understanding of the problem and the data gained throughout the project.
