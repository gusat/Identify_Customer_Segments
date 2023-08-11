# Identify_Customer_Segments
P3 in Udacity T3

The Jupyter notebook is self-contained; it runs on any basic PC w/ the proper python libs installed.

let's abuse this README to replicate our conclusions

Analysis and Discussion:

Aggregating these preliminary insights from a limited range of analyses (5 runs; non-SME student, single clustering, rash decisions in feat. eng. etc.), an early understanding of customer segmentation and preferences for the mail-order company comes into focus. We attempt a first perspective on the segments that are relatively popular or unpopular with the company, offering our arguable guidance for targeted marketing strategies.

Relatively Popular Customer Segments:

Distinct Cluster Attributes: Clusters that are overrepresented in customer data exhibit common traits. These individuals are often wealthier, residing in larger households, and leaning towards conservative financial habits. They tend to be rational, materialistic, and dutiful, with characteristics that are more aligned with traditional values.

Affluent Older Demographics: An evident pattern emerges among segments that consist of older, more affluent individuals. This demographic is characterized by higher financial status, a penchant for wealth accumulation, and a preference for larger residences.

Psychological Traits: Overrepresented segments often encompass individuals who demonstrate rational financial behaviors, are less dreamful and socially-minded, and live in less densely populated areas.

Relatively Unpopular Customer Segments:

Diverse Cluster Attributes: Clusters underrepresented in customer data share varying characteristics. This includes environmentally conscious individuals living in densely populated regions with higher unemployment rates and segments comprised of younger individuals with lower financial awareness and status.

Challenges with Younger Audiences: Younger individuals, particularly females, stand out as being relatively unpopular among the customer base. These segments often lack financial involvement, exhibit less conservative attitudes, and reside in densely populated areas.

Psychological Traits: Unpopular segments also tend to possess attributes such as high financial interest, rationality, combative attitudes, or being male. These traits align with segments that do not resonate well with the company's offerings.

Potential Guidance for Marketing Strategy:

Targeting Older and Wealthier: Given the prevalence of overrepresented segments that are older and wealthier, it's advisable to direct marketing efforts towards this demographic. Crafting campaigns that emphasize affluence and financial stability could be effective.

Tailoring Psychological Messaging: Understanding the psychological traits associated with both popular and unpopular segments provides an opportunity to craft messaging that resonates with each group's values and aspirations.

Leveraging Environmental and Economic Trends: The environmentally conscious segments can be tapped into by aligning marketing efforts with green initiatives. On the other hand, addressing financial awareness among younger demographics is crucial for engagement.

Balancing Contradictory Traits: Considering contradictory traits collectively, marketers should aim to identify potential customers based on combinations of attributes. This can provide a nuanced approach to reaching diverse audiences.

In conclusion, this preliminary analysis draws from a range of k-mean cluster&PCA investigations, enabling the mail-order company to shape a sophisticated marketing strategy. By focusing on identified segments and crafting messaging that addresses the above mentioned attributes and traits, the company can position itself for success in attracting and engaging a wide-ranging customer base.

Limitations of our ML Analysis:

Limited Number of Clusters: The K-means clustering utilized only 16 clusters due to the absence of a clear elbow point in the sum of squared errors (SSE) curve. This limited granularity might not capture the intricate patterns within the data, leading to oversimplification of customer segments.

Lack of Ground Truth: The absence of ground truth labels makes it challenging to objectively evaluate the clustering results. While domain expertise was employed, subjective interpretation can introduce bias into the segmentation process.

Cluster Interpretability: Interpreting the meaning behind the clusters can be complex, as they are composed of high-dimensional principal components. Connecting these components to actionable insights can be challenging and might require further domain-specific knowledge.

Data Transformation Impact: The reduction of features through PCA (from 284 to 128) introduces the risk of information loss. While it aids in dimensionality reduction, it might mask subtle nuances that play a crucial role in customer segmentation. We also dropped ca. 10% of the samples (93K rows), despite the KS tests advising to the contrary; hence we may have introduced a bias distorting our conclusions...?

Sensitive to Initialization: The performance of K-means clustering can vary based on the initial placement of centroids. Different random initializations can lead to slightly different cluster assignments, impacting the stability of the results.

Future Work:

Alternative Clustering Algorithms: Exploring other clustering methods such as hierarchical clustering, DBSCAN, or Gaussian Mixture Models and EM could provide different perspectives on the data structure, potentially revealing more meaningful clusters.

Feature Engineering: Careful selection and engineering of features can improve the quality of the clusters. Exploring new features or transformations might highlight more pronounced patterns.

Dimensionality Reduction Techniques: Experimenting with other dimensionality reduction methods beyond PCA, such as t-SNE or UMAP, might help retain more of the original data's characteristics while reducing dimensionality.

Evaluation Metrics: Introducing evaluation metrics like silhouette scores, Davies-Bouldin index, or silhouette plots could provide more objective means to assess the quality of the clustering results.

Hyperparameter Tuning: Fine-tuning the parameters of the clustering algorithm, including the number of clusters, initialization methods, and convergence criteria, could lead to more stable and accurate segmentation.

Domain Expertise: Collaborating closely with domain experts and incorporating their insights during both the preprocessing and clustering stages can enhance the accuracy and interpretability of the segmentation.

Ensemble Methods: Combining results from multiple clustering algorithms through ensemble techniques can provide a more robust and reliable segmentation outcome.

External Validation: Gathering external data, such as customer demographics or behavioral data, could be used to validate the generated clusters against real-world characteristics.

Iterative Approach: Segmentation is not a one-time task. Regularly revisiting and updating the analysis based on new data and insights is important to ensure the strategy remains relevant.

In conclusion, while our initial ML analysis provided valuable insights, it's important to acknowledge its limitations. Expanding the analysis through the mentioned future work avenues can enhance the accuracy, stability, and applicability of the customer segmentation process for the mail-order company.

Intangible / remark: After 5 runs with different PCA and K-means, this student could not obtain the resemblance of an elbow in the SSE scores plots. This suggests the need for alternative clustering models and metrics.
