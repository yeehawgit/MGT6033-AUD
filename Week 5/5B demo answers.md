# Answer Key

## Section 1: Data Preparation and Feature Engineering

1. Correct Answer: B  
Explanation: TfidfVectorizer is used for the DTM in Demo 5B.  
Verbatim Quote: “I'm going to use TFIDF to extract features.” (5B-Clustering-Dimension-Reduction.pdf)

2. Correct Answers: A, B, C, D  
Explanation: All listed parameters are set for the vectorizer except E (use_idf is not mentioned).  
Verbatim Quote: “vec = TfidfVectorizer(token_pattern = r'\b[a-zA-Z]{3,}\b', stop_words = list(stops), ngram_range = (1,2), max_features = 1000)” (5B-Clustering-Dimension-Reduction.pdf)

3. Correct Answer: D  
Explanation: Clustering algorithms do not require integer counts, so TF-IDF can be used.  
Verbatim Quote: “Clustering algorithms we're looking at, they don't require simple word counts.” (5_DemoB1-The-Data.txt)

4. Correct Answers: B, C, D
Explanation: Curse of dimensionality, sparsity, and scale differences are main challenges.  
Verbatim Quote: “Recall that clustering algorithms like K-means can be negatively impacted by features with varying scales and by the curse of high dimensionality.” (5_DemoB4-Dimension-Reduction-Standardizing-and-Tuning-K-means.txt)

5. Correct Answer: C  
Explanation: Standardization centers each feature at zero and scales to unit variance.  
Verbatim Quote: “By shifting it, we move the mean to be zero... we divide everything by the standard deviation... going to have a standard deviation of one.” (5_DemoB4-Dimension-Reduction-Standardizing-and-Tuning-K-means.txt)

## Section 2: K-means Clustering and Cluster Evaluation

6. Correct Answer: B  
Explanation: n_clusters is the primary parameter for K-means.  
Verbatim Quote: “n_clusters : the number of clusters (recall that k-means requires us to set this)” (5B-Clustering-Dimension-Reduction.pdf)

7. Correct Answers: A, B, C  
Explanation: value_counts, reviewing cluster sizes, and examining extremes are all used.  
Verbatim Quote: “We can check this with value_counts() in pandas... how distributed clusters are within the data.” (5B-Clustering-Dimension-Reduction.pdf)

8. Correct Answer: D  
Explanation: Silhouette score measures how well a point fits in its cluster vs. others.  
Verbatim Quote: “Silhouette score... measures how well each point fits within its assigned cluster compared to others.” (5_DemoB5Tuning-the-K-Means-Model.txt)

9. Correct Answers: A, B, C  
Explanation: All three are used to interpret cluster meaning.  
Verbatim Quote: “We can evaluate which words appear with greatest prevalence... determine which cluster dimensions are most dissimilar... identify which reviews are closest to each cluster center.” (5_DemoB3-Evaluating-Individual-Clusters.txt)

10. Correct Answer: A  
Explanation: Standardizing cluster centers allows fair comparison of feature importance.  
Verbatim Quote: “If we standardize all of these features to have mean zero... tells you how far it is away from the mean.” (5_DemoB3-Evaluating-Individual-Clusters.txt)

## Section 3: Dimension Reduction and PCA

11. Correct Answer: C  
Explanation: PCA reduces feature count while retaining variance.  
Verbatim Quote: “principal component analysis... identifies a set of common factors... that explain the majority of the variation in the original data.” (5B-Clustering-Dimension-Reduction.pdf)

12. Correct Answers: A, B, D  
Explanation: Eigenvalues >1, explained variance threshold, or a fixed number are all common.  
Verbatim Quote: “Retain only those factors with eigenvalues greater than 1, or those factors that explain at least as much variation as an individual feature... or a target threshold of total variance.” (5B-Clustering-Dimension-Reduction.pdf)

13. Correct Answer: C  
Explanation: Standardization gives each component mean zero, std one.  
Verbatim Quote: “all I did was took dtm_pca, passed it to my standardizer, and created a final document term matrix.” (5_DemoB4-Dimension-Reduction-Standardizing-and-Tuning-K-means.txt)

14. Correct Answers: A, B, C  
Explanation: explained_variance_ratio_ provides all these except the number of clusters.  
Verbatim Quote: “explained_variance_ratio_... tells me what proportion of the overall variance is explained by each individual component.” (5B-Clustering-Dimension-Reduction.pdf)

15. Correct Answer: B  
Explanation: Retaining up to 75% balances dimension reduction and information retention.  
Verbatim Quote: “keep components such that 75% of that variance in the data is explained.” (5_DemoB4-Dimension-Reduction-Standardizing-and-Tuning-K-means.txt)

## Section 4: HDBSCAN, UMAP, and Advanced Clustering

16. Correct Answer: D  
Explanation: “-1” is used for noise points in HDBSCAN.  
Verbatim Quote: “I have one very populous cluster, minus 1. Any guess what minus 1 is? It's actually noise.” (5_DemoB6-EHDBSCAN-and-UMAP.txt)

17. Correct Answers: A, B, C, D  
Explanation: All except n_init are key HDBSCAN parameters.  
Verbatim Quote: “cluster selection method... min cluster size... min samples... cluster selection epsilon...” (5_DemoB7-Tuning-HBSCAN.txt)

18. Correct Answer: B  
Explanation: High-dimensionality makes points appear unique, so many are labeled noise.  
Verbatim Quote: “high-dimensional data... Everything looks sparse. If every observation looks unique, you end up with lots of observations categorized as noise.” (5_DemoB6-EHDBSCAN-and-UMAP.txt)

19. Correct Answers: A, B, C, D  
Explanation: All four are recommended for evaluating HDBSCAN results.  
Verbatim Quote: “number of points that are classified as noise, the number of clusters... maximum cluster size and the standard deviation of cluster size... how many clusters are in that minimum size cluster bracket.” (5_DemoB7-Tuning-HBSCAN.txt)

20. Correct Answer: A  
Explanation: UMAP preserves local structure, which is better for density-based clustering.  
Verbatim Quote: “UMAP... tends to retain that local relationships which just tends to work a little bit better with HDBSCAN than a linear projection that you get from PCA.” (5_DemoB6-EHDBSCAN-and-UMAP.txt)
