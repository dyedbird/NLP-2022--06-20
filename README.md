# NLP-2022--06-20

REDDIT TOPIC TRENDS IN r/datascience

By: Burak Basogul

Abstract

The potential client(s) for the results of this analysis are Reddit or similar forum web sites. Reddit has a built-in filtering mechanism on its site but lack a section that shows trending topics. Addition of such a new section to the subreddits could draw new users who are more so interested in catching up on the latest trends in a domain of their interest with ease rather than turning on a couple of filters and fortunately coming across an engaging discussion.

Design
I have been a member of the r/datascience for several months now which motivated me to explore and identify trending topics for this subreddit. Having been following the channel long enough provided me with enough familiarity to be able to interpret the topic components especially for the components predicted by LSA and NMF models. 

Data
Using PushshiftAPI 8,715 submissions and a total of 86,212 comments made under those submissions were retrieved from r/datascience subreddit. The data was limited to the timeframe between 12/27/21 and 06/27/22. Subsequently, the data was converted to Data Frame and exported as .csv files for further EDA, clean-up and corpus building.

Algorithms 
•	Data Retrieval
  1.	Reddit’s own API does not allow for large amounts of data scraping, so PushshiftAPI was used to retrieve submission and comment data.
•	Dimensionality Reduction Models
  1.	Latent Semantic Analysis (LSA)
  2.	Non-Negative Matrix Factorization (NMF)
•	Probabilistic Model
  1.	Latent Dirichlet Allocation (LDA)

•	Model Evaluation and Selection
Once all models were tuned, fitted and visualized for 10 topic components each with 10 terms in them, it was clear that LDA was not accurate enough predicting insightful terms as LSA and NMF were capable of in this use case. However, both LSA and NMF performed similarly accurate in predicting the topic terms but the LSA had the edge for being faster in the end. It will be good practice though to employ both LSA and NMF for future iterations of this project or any other Reddit data analysis.

Tools
•	PushshiftAPI for data import
•	Numpy and Pandas for data manipulation
•	NLTK, Gensim, RegEx and Scikit-learn for text preprocessing and modeling
•	Matplotlib for plotting

Communication
•	Project presentation slides
