# Machine Learning Clustering Project

This project implements **unsupervised clustering algorithms** on a dataset containing species measurements. Both custom implementations and Scikit-Learn models are used to compare performance.

## Project Overview

The dataset (`hw4 dataset`) contains two features: **length** and **width** of several species. The species themselves are unknown, making this an **unsupervised learning task**. The main goal of this project is to classify the data points into clusters that can represent different species.

Two clustering algorithms were implemented:

1. **K-Means Clustering**
2. **Gaussian Mixture Model (GMM) Clustering**

Both algorithms are implemented from scratch in Python using NumPy.

## Project Structure

```
Machine-Learning-Projects/
│
├─ KMeansCluster.py        # Custom K-Means implementation
├─ GMMCluster.py           # Custom GMM implementation
├─ hw4_dataset.csv         # Input dataset
├─ K-mean.png              # K-Means clustering results
├─ SKM.png                 # Scikit-Learn K-Means results
├─ gmm.png                 # GMM clustering results
├─ sgmm.png                # Scikit-Learn GMM results
├─ report.tex              # LaTeX report
└─ README.md
```

## Implementation Details

### K-Means

* Randomly initializes `k` centroids from the dataset.
* Iteratively assigns each point to the nearest centroid (Euclidean distance).
* Updates centroids as the mean of points assigned to each cluster.
* Stops if centroids converge or after a maximum number of iterations.

### Gaussian Mixture Model (GMM)

* Implements the **Expectation-Maximization (EM)** algorithm.
* Initializes `n_components` Gaussian distributions with random means, identity covariances, and uniform weights.
* **E-Step:** Computes the probability (`responsibility`) of each point belonging to each component.
* **M-Step:** Updates the means, covariances, and weights based on responsibilities.
* Iterates until convergence or maximum iterations reached.

### Comparison to Scikit-Learn

Both custom implementations were compared visually with Scikit-Learn’s implementations:

* `sklearn.cluster.KMeans`
* `sklearn.mixture.GaussianMixture`

The results were consistent, demonstrating that the custom implementations are correct.

## Usage

1. Install dependencies:

```bash
pip install numpy matplotlib pandas scikit-learn
```

2. Load the dataset and run clustering scripts:

```python
from KMeansCluster import KMeanscluster
from GMMCluster import GMMcluster
import pandas as pd
import numpy as np

# Example for K-Means
X = pd.read_csv('hw4_dataset.csv').values
kmeans = KMeanscluster(k=3, max_iter=100)
kmeans.fit(X)
clusters = kmeans.predict(X)
```

3. Generate and save cluster plots:

```python
import matplotlib.pyplot as plt
plt.scatter(X[:,0], X[:,1], c=clusters)
plt.savefig('K-mean.png')
```

4. Repeat similarly for GMM.

## Results

* Clustering results were saved as images (`K-mean.png`, `SKM.png`, `gmm.png`, `sgmm.png`)
* Different values of `k` or `n_components` and iteration limits were tested to analyze convergence and cluster stability.
* Visual inspection shows that custom implementations closely match Scikit-Learn results.

## Conclusion

* Custom K-Means and GMM implementations successfully clustered the dataset.
* Increasing `k` or `n_components` produces more granular clusters.
* Both algorithms converge well for moderate iteration limits.
* Comparison with Scikit-Learn confirms correctness of the implementations.

---

## Author

**Anushka Hada**
Email: [[your_email@example.com](mailto:your_email@example.com)]
