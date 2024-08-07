# CryptoClustering - Module 19 homework for Data Analysis bootcamp

# Used sk learn library for clustering and pca (unsupervised learning) to perform historical crypto price change analysis.

**Analysis:**

PC1 (explains the most variance):

Strongly positively correlated with long-term price changes (200d, 1y)
Negatively correlated with short-term changes (24h)
So PC1 might represent the contrast between long-term and short-term price trends.

PC2:

Positively correlated with medium-term price changes (30d, 14d, 60d)
Also has some positive correlation with short-term changes (24h, 7d)
PC2 might represent overall medium-term price trends.

PC3:

Strongly positively correlated with 7d price change
Mix of positive and negative correlations with other timeframes
PC3 might capture specific weekly price dynamics that differ from longer-term trends.

**Inference:**

Long-term vs. Short-term: There's a clear distinction between long-term and short-term price changes, primarily captured in PC1.
Medium-term Trends: PC2 seems to capture medium-term price trends.
Weekly Dynamics: PC3 gives special importance to weekly (7d) price changes.

----------------------------------------------------------------------------------

**from Claude AI when prompted with:
"So how would I use this information to predict future prices?"**

**Here's how you might use this information:**

**Pattern Recognition:**

The PCs identify key patterns in price changes across different timeframes.
You could monitor how new price data aligns with these patterns to get a sense of overall market trends.


**Cryptocurrency Grouping:**

The clusters group cryptocurrencies with similar behavior patterns.
You might expect cryptocurrencies in the same cluster to respond similarly to market conditions.


**Feature Selection for Predictive Models:**

The PCA results highlight which timeframes are most important in capturing price variability.
You could use this to select or weight features in a predictive model (e.g., giving more importance to 200d and 1y changes for long-term predictions).


**Market Segmentation:**

Different clusters might represent different market segments (e.g., stable coins, volatile coins, etc.).
You could develop separate prediction strategies for each segment.


**Trend Analysis:**

PC1 contrasts long-term and short-term trends. You could use this to identify cryptocurrencies where short-term trends are diverging from long-term trends, which might indicate potential price corrections.


**Anomaly Detection:**

Cryptocurrencies that don't fit well into any cluster or suddenly change clusters might be undergoing significant changes, which could precede price movements.


**Dimensionality Reduction for Other Models:**

You could use the PCA-transformed data as input for other machine learning models (e.g., regression, neural networks) that are more directly suited for price prediction.


**Correlation with External Factors:**

You could investigate how external factors (news, regulations, etc.) affect cryptocurrencies in different clusters, potentially helping predict reactions to future events.


**Risk Assessment:**

Clusters with high variability in PC3 (weekly changes) might be considered more risky or volatile in the short term.


**Portfolio Diversification:**

For investment purposes, you might choose cryptocurrencies from different clusters to diversify a portfolio.

**This analysis should be just one part of a comprehensive approach that might include:**

More advanced time series analysis techniques
Fundamental analysis of the cryptocurrencies and their underlying technologies
Sentiment analysis of news and social media
Consideration of broader economic factors and market conditions
