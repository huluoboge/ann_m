# ann_m
ANN: A Library for Approximate Nearest Neighbor Searching for multi-threaded version

The original code is here: : https://www.cs.umd.edu/~mount/ANN/

**The original version does not support multi-threaded searching, while this version supports multi-threaded searching.**

----
ANN is a library written in C++, which supports data structures and algorithms for both exact and approximate nearest neighbor searching in arbitrarily high dimensions.
In the nearest neighbor problem a set of data points in d-dimensional space is given. These points are preprocessed into a data structure, so that given any query point q, 
the nearest or generally k nearest points of P to q can be reported efficiently. 
The distance between two points can be defined in many ways. 
ANN assumes that distances are measured using any class of distance functions called Minkowski metrics. 
These include the well known Euclidean distance, Manhattan distance, and max distance.

Based on our own experience, ANN performs quite efficiently for point sets ranging in size from thousands to hundreds of thousands, and in dimensions as high as 20. 
(For applications in significantly higher dimensions, the results are rather spotty, but you might try it anyway.)

The library implements a number of different data structures, based on kd-trees and box-decomposition trees, and employs a couple of different search strategies.

The library also comes with test programs for measuring the quality of performance of ANN on any particular data sets, as well as programs for visualizing the structure of the geometric data structures.

Why approximate nearest neighbors?
Computing exact nearest neighbors in dimensions much higher than 8 seems to be a very difficult task.
Few methods seem to be significantly better than a brute-force computation of all distances. 
However, it has been shown that by computing nearest neighbors approximately, it is possible to achieve significantly faster running times (on the order of 10's to 100's) often with a relatively small actual errors.
ANN allows the user to specify a maximum approximation error bound, thus allowing the user to control the tradeoff between accuracy and running time.
