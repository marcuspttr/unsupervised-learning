# unsupervised-learning
Using unsupervised machine learning methods to help cluster cryptocurrencies.

## Some thoughts:
- This was an intense assignment bringing together almost a "best of" our unsupervised machine learning methods.
- The overall idea of the assignment was very interesting, with reports on cryptocurrencies being somewhere between "fad" and "the future".

### A picture of the initial data provided:
![Initial upload of data](https://github.com/marcuspttr/unsupervised-learning/blob/main/Assets/intialframe.PNG)

I started by removing unnecessary columns such as the coin names (at this point we are just interested in seeing if there are clusters of similar coins at a general level) and cleaning out null or duplicated values. Then converted key categorical data into binary settings with one hot encoding (which shifted the data from 5 columns to 97). The final in preparing the data was to standardize the numeric data to make trends easier to find, resulting in the following table:

### Preview of data after cleaning & preparing:
![Prepared dataframe](https://github.com/marcuspttr/unsupervised-learning/blob/main/Assets/scaledframe.PNG)

Running the indicated dimensionality reduction to maintain 90% of the explained variance, we limited the data to 12 principal components.
Created a new clean dataframe for reference in the future calculations.

### PCA dimensionality reduction, resulting frame with components:
![PCA dimensionality reduction](https://github.com/marcuspttr/unsupervised-learning/blob/main/Assets/datapca.PNG)

### TSNE graph with potential clusters within the data:
![TSNE graph](https://github.com/marcuspttr/unsupervised-learning/blob/main/Assets/tsnegraph.PNG)
The graph definitely seems to show some distinct clusters. I have some concerns of how tightly some of the data appears, but I would claim at this point there are around 5 clusters.

### Elbow graph showing clusters & inertia:
![K means eblow graph](https://github.com/marcuspttr/unsupervised-learning/blob/main/Assets/elbowgraph.PNG)
Finding the proper flattening of this curve I'd recommend to my clients that there may be 6 to 7 clusters within the data. Reflecting on the TSNE graph as well, I'd say it's safer to go with the additional clusters (6) rather than misgroup unrelated data. 
