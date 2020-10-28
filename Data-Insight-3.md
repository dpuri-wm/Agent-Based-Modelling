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
  
![1*VUw6Pfe7qcuiGtxSZenxiw](https://user-images.githubusercontent.com/60228374/97474998-157d1200-1923-11eb-903a-e8e212530b3c.png)
  
  To calculate distance between clusters, there are a variety of approaches. These include calculating the maximum distance between clusters before merging, calculating average distance between clusters, finding the centroid of cluster 1 and cluster 2 and calculating the distance between them before merging. 
  
  ### Application
  
  There are a variety of different applications of hierarchical clustering. Oftentimes, biologists utilize the data science method to construct phylogenetic trees that reveal evolutionary information about different species. Another application includes utilizing hierarchical clustering to analyze population health and labour market regulations in lower-middle income countries. In the article, published in BMC Public Health, "Hierarchical cluster analysis of labour market regulations and population health: a taxonomy of low- and middle-income countries," 113 Lower middle income countries were clustered together accroding to their labour market taxonomy. These clusters were analyzed for their association with adult mortality, healthy life expectancy, infant mortality, nenonatal mortatlity, and more health factors. Thus, this method would rellay allow to see the correlation between labour market regulations and health factors, as countries with similar markets are clustered together and compared. Without clustering, it would be difficult to hone in on whether market regulations actually have an association with health - there may be confounding variables. However, across many countries, if a relationship is shown, then it would be more accurate. 
  
  The result was interesting; it was determined that labor market regulations are a social determinant of health. In the end, 6 market clusters were created. These include: residual, emerging, informal, post-communist, less-successful informal, insecure. Next, boxplots were created to see the relationship with the different health factors. I included the boxplot of the 6 market clusters with maternal mortality rate below:
  
  ![Screen Shot 2020-10-28 at 1 37 23 PM](https://user-images.githubusercontent.com/60228374/97474885-f7afad00-1922-11eb-8363-095f0fe03687.png)

