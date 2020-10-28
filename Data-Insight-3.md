## Data Science Method: Clustering

  In this data insight, I wanted to examine the data science method: Clustering. According to Toward Data Science, clustering a is a machine learning algorithm that involves the grouping of data points. This method is very useful, especially when analyzing data with multiple features/variables. Data points can be grouped together, revealing they are similar with respect to their features. One would expect data points in different groups to have different features/properties and be dissimilar to one another, while data points in the same group are similar to one another. Clustering is considered "unsupervised learning", meaning that it is a type of machine learnign that searches for previously undetected patterns in a dataset. There are many different clustering models: connectivity models based on connectivity distance, centroid models based on central individuals and distance, density models based on dense region in space, graph models based on cliques and their relaxations, and more. However, the model I would like to discuss in this insight is the hierarchical (graph) mode. 
  
  ### Hierarchical model
  
  There are two ways of clustering data points with the use of this model, agglomerative and divisive. Agglomerative involves single observations and merging clusters together until a stopping criterion is satisfied. A divisive method begins with a single cluster and performs a splitting until a stopping criterion is met. Divisive methods are much more popular, as we are used to seeing the divisive cluster representation much more often. [Agglomerative on left, Divisive on right]
  
  ![1*3JL_dSj4cGguByJM1-wz3A](https://user-images.githubusercontent.com/60228374/97467123-3ee57000-191a-11eb-8477-e2f136fa18de.png)
  
  The main operation that is repeated in hierarchical clustering is to combine the two nearest clusters into a larger cluster. This is done through the following steps:
  
  1. Distance is calculated between every pair of observation points and is stored in a distance matrix
  2. Every point is considered its own cluster
  3. the closest pairs of points are merged based on their distance matrix, amount of clusters decreases by 1
  4. distance is recomputed between the new cluster and all the other ones, and stored in a new distance matrix
  5. steps 2 and 3 are repeated until there is one single cluster
  
  The end result is a hierarchical, tree-like diagram - called a dendogram. The below plot is an example of one:
  
  
  
