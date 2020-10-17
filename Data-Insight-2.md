# Principle Component Analysis

Principle Component Analysis (PCA) is a data science method used to "reduce the dimsension of your feature space." In simpler terms, data scientists often have to work with so many variables in order to analyze the data properly. It's impossible for them to understand the intricate complexities of the relationship between each and every variable. Additionally, many variables increase the risk of overfitting a model or violating certain assumptions of the modeling tactic. Matt Brems, in his Toward Data Science article, states that one may ask the question, "How do I rake all of the variables I've collected and focus on only a few of them?" This is where PCA comes in and reduces the dimension of the feature space, meaning it allows for fewer relationships to be considered at a time.

### Dimensionality Reduction

Although there are many ways to reduce dimensionality of the data, the two most commonly used techniques are feature elimination and feature extraction.

- Feature elimination: In order to reduce dimensionality, we can eliminate features of the data. For example, if GDP data, you could drop the variable, "unemployment rate." Dropping variables would allow for greater simplicity and being able to fully comprehend more variables. However, a downside is that eliminating some features means eliminating some benefits those features would have brought. For example, the unemployment rate could have helped predict GDP since it contibutes to it in a significant way. However, we have dropped that variable. 

- Feature extraction: Instead of eliminating features, feature extraction almost "adds" new features to the dataset. Fo example, if we are analyzing GDP data and have 5 independent variables, we can create five "new" independent variables that essentially is a combinaytion of the previous 5 variables. These new variables are constructed in a specific way and are ordered by their significance and contribution to the dependent variable. For simplicity, we can drop some of these new variables created. However, this won't skip out on important information in the same way that feature elimination does, as we will keep most of the old variables. And since the newly constructed variables were created based on the new variables, we still have these valuable parts of the dataset in our analysis. 

### How PCA works

One thing to note before we dive into how PCA works, is that you should only use PCA if you are comfortabel with making some of your variables less interpretable. The new variables created won't be as easy to understand since they are a combination of all the other independent variables. The main break down of the PCA process is as follows:

1. calculate a matrix that summarizes how all the variables relate to one another
2. break matrix down into direction and magnitude
3. transform original data to align with directions

The process is a bit complicated and involves comprehension of upper-level mathematics. Luckily, in many languages such as R, there are functions that will conduct PCA for you. Here's a little snippet of the code in R:

![Screen Shot 2020-10-17 at 10 59 29 AM](https://user-images.githubusercontent.com/60228374/96343281-db308c80-1067-11eb-86c3-1acbf643a454.png)

### Applications

One really cool application I found of PCA was in making inferences of genetic ancestry differences among individuals from different populations. PCA is applied to genotype data to calculate principle components that explain the differences among these sample individuals in the genetic data. When PCAs were applied to European genetic data, it revealed that for Europeans whose all 4 grandparents originated in the same country, the first two principal components could map their country of origin quite accruately in the plane. These two principle components were computed using 200,000 SNPs. For referenced, SNPs are single nucleotide polymorphisms, or basically a single base-pai in the DNA. 



