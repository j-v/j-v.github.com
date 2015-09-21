---
layout: media
title: Content-Based Image Retrieval Using the Earth Mover's Distance Algorithm
categories: portfolio
image:
  teaser: emd/mdsvis-teaser-400x400.png
---

 As a course project during my time at Freie Universität Berlin, my teammate Martí Griera Jorba and I experimented with various algorithms relating to shape matching and feature extraction in images. The project was coded in C++, making extensive use of the [OpenCV](http://opencv.org/) library for computer vision. The image below illustrates some of the algorithms we used to extract features from input images, resulting in a representation of the image as a weighted point set. 

![ Feature extraction algorithms ](/images/emd/pointset-method.png)

*Data from edge detection done using the Canny algorithm, corner detection using the MinEigenVal algorithm, and the intensity gradient computed using the Sobel operator were combined to generate the resultant point set. We used OpenCV implementations of all three algorithms.*

To compare the weighted point sets, we used the [Earth Mover's Distance](https://en.wikipedia.org/wiki/Earth_mover%27s_distance) (EMD) algorithm, as implemented by [Yossi Rubner](http://ai.stanford.edu/~rubner/emd/default.htm). 

![ Images of a ray compared using EMD ](/images/emd/ray-emd-vis.png)

*Visualization of EMD computed on two images of simple shapes. Larger points indicated larger weights, and thicker lines indicate higher flow between points*

With the feature extraction and comparison algorithms in place, we can query a database of images, and retrieve the closest matches.

![ Simple shape matches ](/images/emd/simple-shapes-queries.png)

*Closest matches to the query image, as reported by our EMD comparison engine. Dataset: [Brown Shape Indexing of Images Database (SIID)](http://www.lems.brown.edu/vision/researchAreas/SIID/)*

The EMD image retrieval engine effectively returns matches for a database of simple images, such as the dataset of silhouettes shown above. For more complex datasets, the results are... mixed.

![ Matches from the Caltec 101 Categories Dataset ](/images/emd/categories-queries.png)

*Image retrieval results of a larger, more complex dataset. Dataset: 500 image subset of the [Caltec 101 Categories Dataset](http://www.vision.caltech.edu/Image_Datasets/Caltech101/)*

It can be interesting to visualize an image database globally to examine the computed similarities of the images. We did this using a [multidimensional scaling](https://en.wikipedia.org/wiki/Multidimensional_scaling) algorithm, which plots each image into 3D space. Images which are computed to be most similar to each other wind up closest to each other in the 3D space. We used the freely available [MDSJ - Multidimensional Scaling for Java](http://algo.uni-konstanz.de/software/mdsj/) library, and created a 3D visualization using [Processing](https://processing.org/).

![ Visualizing image similarities using multidimensional scaling ](/images/emd/mdsvis1.png)

*The SIID image dataset visualized in 3D space. Each image class is given a different color. Images nearest to eachother in 3D space are most similar as computed by EMD.* 