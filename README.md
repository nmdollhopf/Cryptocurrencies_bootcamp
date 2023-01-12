# Cryptocurrencies_bootcamp

This is the module 19 challenge for the unc data analytics bootcamp.

Given a dataset of cryptocurrency information, we aimed to use unsupervised learning methods to group like cryptocurrencies. 

Dataset, included as crypto_data.csv, includes cryptocurrency names and nicknames (e.g. BitCoin and BTC), algorithm used, the type of proof used, whether the coin is trading, the total number of coins mined so far, and the current supply of each coin.

Work was completed in the notebook crypto_clustering.ipynb.  

First, we dropped all coins not actively trading and all coins that have not been mined yet. We then one-hot encoded categorical columns via `pandas`' `get_dummies()` method. `Sklearn`'s `StandardScaler` was used to standardize the dataset.

Principal Component Analysis was performed as a teaching aid and to make the analysis easier. Included in the notebook is discussion on a better choice for the number of components to use. In the end, 3 components were used for visualization purposes.

`Sklearn`'s `KMeans` was utilized for the unsupervised clustering. Included is an elbow curve of `inertia vs k` to find an "ideal" number of clusters to use for the categorization. Choosing 4 clusters, we perform the unsupervised clustering and plot the assigned class of each cryptocurrency by the 3 principal components. 

We also create summary tables with the assigned classes to each cryptocurrency and plot the assigned classes on a 'total coin supply' vs 'total coins mined' graph. The first of these graphs have these values scaled between 0 and 1. The second graph is instead plotted on a log scale to prevent clumping and better visualize the outcomes.

No further analysis or interpretation is done on the assigned classes.
