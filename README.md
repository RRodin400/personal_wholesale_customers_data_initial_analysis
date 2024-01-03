# Background information
The dataset analyzed for this report is called Wholesale Customers, sourced from the UCI Machine Learning 
Repository [1]. This dataset contains vendor data from various customers of a wholesale distributer [1]. It 
contains a total of 440 records. Each record represents a single vendor and contains information related to 
their annual expenditure, in some unknown monetary unit, for various product domains. More specifically, 
there are 8 features to this dataset. The first two features (‘Channel’ and ‘Region’) store categorical 
information about the vendor (but were translated into numeric values): Channel describes the customer 
type, either Hotel/Resturant/Café, or Retail, whereas Region refers to the client’s location: Lisbon, Oporto, or 
other. The remaining features provide details about spending in the following product categories (each 
category is represented by its own feature): Fresh produce, Milk, Grocery, Frozen, Detergents_Paper, and 
Delicatessan. There is no missing data from the dataset [1].

# Methods
Clustering algorithms performed so far on the dataset: K-means, DBSCAN, and hierarical clustering. 

K-means:
I will use SSE (Sum of Squared Errors) to help determine a good value for k, the number of clusters to partition 
the dataset into. I will also use SSE to measure cluster cohesion and help evaluate cluster validity for the k-mean model.
To provide some significance to the SSE value obtained, it would be ideal to set up a statistical framework for evaluating 
the SEE value: I ideally would generated 200 datasets, each with the same shape (400 records by 8 features) as our 
Wholesale Customers dataset, with the same normalized range, ran 20 iterations of K-means on each, and calculate an
ANOVA p-value [5].

DBSCAN:
I will validate the clusters created by DBSCAN using Silhouette Scores.

Hierarchical Clustering:
 I ran this type of algorithm 3 
different ways: defining inter-clustering distance first via the min method, second via the group method, and lastly via 
the max method. Since SSE was designed for non-overlapping clusters [3], like with DBSCAN, cluster validity will be measured 
via the silhouette score. 



References
[1] = https://archive.ics.uci.edu/dataset/292/wholesale+customers
[2] = Dr. Elodie Lugez CPS803/8318 Machine Learning Fall 2023 Class Notes
[3] = https://shritam.medium.com/how-dbscan-algorithm-works-2b5bef80fb3
[4] = https://www.semanticscholar.org/paper/An-Efficient-Algorithm-for-Density-Based-Subspace-LakshmiMadhuri/f93298e163b368c2e77500f77cea260dbdff8629
[5] = https://www.reneshbedre.com/blog/anova.html

