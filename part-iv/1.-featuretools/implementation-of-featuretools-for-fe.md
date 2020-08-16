# Implementation of FeatureTools for FE:

You can find lots of examples of featuretools implementation at ‘[**featuretools demos**](https://www.featuretools.com/demos/)**’.** I will be using one of the mock datasets to explain this tool in brief.

**Install featuretools:**

![](https://cdn-images-1.medium.com/max/1600/1*GSE2I1N_7J-qUdymx2Em2Q.png)

![](https://cdn-images-1.medium.com/max/1600/1*OG7NLpD_fdKqXGJDA2p0WQ.png)

**Load Mock data:**

This toy data has 3 entities:  
customers: list of customers with unique customer\_id and other relevant attributes  
sessions: unique sessions, joined to customer entity using customer\_id  
transactions: list of events

![](https://cdn-images-1.medium.com/max/1600/1*wuFH3dZi8uhkRprcfFl6uQ.png)



**Running Deep Feature Synthesis:**

As already stated in the description of DFS, **the minimal input to DFS is a set of entities, a list of relationships, and the “target\_entity” to calculate features for**.  
The output of DFS is a feature matrix and the corresponding list of feature definitions for the given target entity.  
So, we need to perform 2 tasks:

1. define a dictionary of all the entities
2. relationship between them When 2 entities have a many-to-one relationship then one entity is called ‘parent’ and the other is called the ‘child’ entity. And the relationship is defined as:  **\(parent\_entity, parent\_variable, child\_entity, child\_variable\)**

![](https://cdn-images-1.medium.com/max/1600/1*a5XeW8v93_gMF8YPOPznDw.png)

Similar feature matrices can be created for other entities by changing the ‘target\_entity’ value in the ft.dfs\(\).

**Using EntitySets:**

Featuretools take ‘entities’ and ‘relationships’ as separate entities, but it is advisable to use **EntitySets**. EntitySet is a collection of entities and the relationships between them. They are useful for preparing raw, structured datasets easily for feature engineering.  
While creating **EntitySet**, we add each entity one by one.

In **entity\_from\_dataframe\(entity\_id,dataframe,index,time\_index,variable\_type\)**:  
**entity\_id** : entity name,  
**index**: a column that acts as a unique identifier  
**time\_index**: tells featuretools when the data was created  
**variable\_type**: allows user to indicate the type of column

![](https://cdn-images-1.medium.com/max/1600/1*nhn_Ni2yJfTsV5hmqcBm6w.png)

![](https://cdn-images-1.medium.com/max/1600/1*o6VHKYFcrupBLlOaBaVqvg.png)

I believe it is a great and the easiest tool to quickly generate large amount features but like any other feature generation tool, it also leads to the [‘**curse of dimensionality**’](../../part-i/some-important-concepts.md#4-curse-of-dimensionality) for which feature selection is required. Also, it cannot be used for non-relational or unstructured data.

So, at a beginner level, it is a good tool to understand feature generation easily. To perform Feature Engineering for non-relational and unstructured data, [AutoFeat](../2.-autofeat/) can be used. AutoFeat is the only general-purpose library for automatic feature generation and selection. 

