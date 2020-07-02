# GraphTheory

Given the project of building a recommendation system for MovieLens100K it was implemented a neural network based on graph features.

The aim was to enhance the model with features related to the data of movies but in the context of graph properties.

## Collaborative filtering: Graph-based

Graph theory has a variety of techniques to find neighbours, and similarities. Besides, there are methods like Link Prediction which can enhance Machine Learning (ML) providing contextual information that only is able to obtain through graphs.

The pipeline is to extract graph features and convert those into features that a ML model can use.

In this project, we used Link Prediction to determine the closeness of a pair of nodes. The computed scores can then be used to predict new relationships between them (Needham etl.al. 2019).
There were used the following Link Prediction algorithms:

**• Common neighbors:** in this scenario it can be applied to find a possible connection between a user that has not watched a movie through a neighbour that already watched it. “The idea is that two strangers who have a friend (Movie) in common are more likely to be introduced than those who don’t have any friends in common” (NEO4J).

**• Preferential attachment:** movies which have a huge amount of links are more likely to receive new RATED link. “The more connected a node is, the more likely it is to receive new links. This algorithm was used by Albert-László Barabási and Réka Albert through their work on scale-free networks” (NEO4J).

**• Total neighbors:** the aim is to find the total number of movies that each user has watched. “computes the closeness of nodes, based on the number of unique neighbors that they have.” (NEO4J).

## References

Needham, M., Hodler, 2019. A. Graph Algorithms, Published by O'Reilly Media, Inc.

NEO4J, 5 Algorithms 5.6. Link Prediction algorithms, viewed on 30 May 2020, https://neo4j.com/docs/graph-data-science/current/algorithms/linkprediction/
