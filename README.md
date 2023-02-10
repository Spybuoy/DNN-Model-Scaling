# ABSTRACT
Convolutional neural networks (CNNs) are a type of artificial neural network that are commonly used for image and video recognition
tasks. They are designed to process data with a grid-like topology, such as an image, by applying a series of filters to the input data to
extract features and make predictions. In order to improve the accuracy of CNNs, it is often necessary to scale them up by increasing
the number of filters (i.e., the width), the number of layers (i.e., the depth), or the resolution of the input images. This process is known
as compound scaling. In this project, I am investigating the implementation of compound scaling to improve the performance of
various neural networks.

# INTRODUCTION
The scaling of neural networks is a critical aspect of machine learning that has garnered a great deal of attention in
the field. In this project, I aimed to delve deeper into this complex problem by exploring the use of the compound
scaling approach to scale various networks in terms of depth, width, and image resolution. By treating the compound
coefficient ø as distinct hyperparameters for each dimension, rather than a single parameter, I sought to gain a greater
understanding of which dimension is most effective for a particular model, based on its size. Additionally, I sought
to compare the performance of scaling with other techniques for model compression, such as pruning and deep
compression, in order to determine the most effective method for improving model performance. Through my work on
this project, I hope to contribute to the broader knowledge base on the topic of model scaling and its impact on model
performance, and to further our understanding of this complex problem.
Taking inspiration from the paper, I sought to further explore the intuitive appeal of the compound scaling method.
Specifically, I recognized that as the size of the input image increases, the network may require more layers to increase
its receptive field and more channels to capture finer-grained patterns in the larger image. Previous theoretical research
has suggested that there may be a relationship between network width and depth, and we sought to empirically quantify
this relationship, as well as the relationship between all three dimensions of network width, depth, and resolution.
Through this work, we hope to gain a greater understanding of how these different dimensions interact and influence
model performance.

# METHODOLOGY
One of the primary challenges presented in the paper is the interconnectedness of the optimal scaling values for depth,
width, and resolution, which are also prone to fluctuation under various resource constraints. As a result, traditional
approaches to scaling ConvNets typically focus on a single dimension, whether it be the depth, width, or resolution

The paper introduces the concept of a "Compound Scaling Coefficient" referred to as 𝜙, which is subject to constraints
imposed by the right-hand side (RHS) value. This RHS value determines the extent to which depth, width, and
resolution can be scaled. Through analysis, it appears that the scaling of these dimensions is approximately equal to
the one-third power of the RHS value in the equation. This was mentioned in my presentation, however upon further
investigation, it has been determined that this relationship is merely a coincidence and not a precise correlation. It does
not hold true for every model. This will further be discussed in the Conclusion/Discussion section.
In order to assess the similarity between various Neural Network models that have been processed, I have employed
various data science techniques, specifically similarity metrics. Two such metrics that I have utilized are Central Kernel
Alignment (CKA) and Canonical Correlation Analysis (CCA).
The CKA method is a measure of similarity between two different distributions, typically used in the context of
comparing the representations of neural networks. It involves calculating the alignment between the kernels of the
distributions, with a higher CKA score indicating a greater degree of similarity. This method has been shown to be
effective in comparing the performance of different neural network architectures and identifying relationships between
their internal representations.
CCA, on the other hand, is a statistical technique used to identify the underlying relationships between two sets
of variables. It involves finding the linear combination of variables that maximizes the correlation between the two
sets. In the context of comparing neural network models, CCA can be used to identify similarities in their internal
representations and relationships between their outputs.
Overall, the use of similarity metrics such as CKA and CCA allows for a more thorough and nuanced understanding of
the similarities and differences between various neural network models, and can inform the selection and design of
models for specific tasks.

# Files

This repository contains the following Jupyter notebooks:

mobilenet.ipynb: a notebook that evaluates scaling of mobilenet model.
resnet.ipynb:a notebook that evaluates scaling of resnet18 model.
scalingresults.ipynb: a notebook that executes previously trained and scaled efficient nets to compare to the results int the previous notebooks.

Setup
To use these notebooks, you will need a access to files on my personal drive. 

Outputs
The outputs of the notebooks are organized in the output folder according to the notebooks they're obtained from.
of the input image. This inter dependency and variable nature of the optimal values make finding the most effective
solution a complex task.
