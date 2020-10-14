# Clustering
In this project, I have made with some age (measured in years) and height (measured in fractional feet. So, for instance, 5 feet 6 inches would be 5.5 since there are 12 inches in a foot). In the data, there is a feature called true_cluster. Usually, this column would never be available (after all, clustering is a form of unsupervised learning). I have not used this column in my clustering either. This column has been included for the sole purpose of comparing clustering methods to ground truth.

**Part 1:**

I load the age_height_data.csv data into a pandas dataframe. I plot a scatterplot of the two variables and colour the dots according to their true_cluster_label value for reference.

**Part 2:**

There are 4 true clusters in the data. I create a K-means pipeline using sklearn's KMeans with n_clusters=4. Then I predict on the data and plot the data according to the predicted cluster label.

**Part 3:**

You can see that the left most blob is clustered in a way that the decision line between two clusters is nearly vertical. 
Here is a question:

- Does this look like the true cluster labels? If not, what might explain this? Hint: How is age measured? How is height measured? Are they comparable scales?

You can find the answer to this question in the Jupyter Notebook I provided: "Clustering.ipynb"

**Part 4:**

I add a StandardScaler to the pipeline and create the plot again. You can see my comment on if the scaling helped the clustering in so far as the predicted clusters look more like the true clusters.

**Part 5:**

In applied clustering, we never know how many clusters exist in the data. That is something we have to decide. One method used to determine the number of clusters is to use an elbow plot.

An elbow plot is made by fitting the clustering algorithm for a variety of cluster sizes (usually between 2 and  𝑁⎯⎯⎯⎯√  clusters, where  𝑁  is the number of rows in the data. Each time we fit the clustering algorithm with a different number of clusters, we record the value of the objective function for the algorithm (in sklearn's KMeans, this can be done by calling Kmeans.score). The number of clusters is determined by looking for an "elbow" in the data; a point where the algorithm's objective function stops decreasing quickly with additional numbers of clusters.

Here I create an elbow plot for this data.

**Part 6:**

Where is the "elbow" for this data?

You can check out my answer to this question in the Jupyter Notebook provided: "Clustering.ipynb"


**Part 7:**

Check out the accompanying paper entitled Clustering - What Both Theoreticians and Practitioners are Doing Wrong, then think about the following short answer questions.

1) Why does the author think the two requirements of clustering conflict with one another?

2) Summarize the author's criticisms of the theoretician's approach to clustering.

3) Summarize the author's criticisms of the practitioner's approach to clustering.

4) As a practitioner, how might you go about thinking about which algorithm to use for clustering from now on?

You can check out my answers to these questions in the Jupyter Notebook provided: "Clustering.ipynb"
