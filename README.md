# Entity-Resolution-using-Machine-Learning-techniques-on-Massive-Datasets
This project aims to develop a competitive solution to be submitted to a programming contest of a database conference (SIGMOD: http://www.inf.uniroma3.it/db/sigmod2020contest/index.html). The contest consists of solving a real-world entity resolution challenge using a dataset of camera product descriptions from various e-commerce sites. The winning team will be the one who achieves the highest f1 score by producing a machine learning pipeline that discerns accurately between matching and non-matching product pairs. This task is especially challenging because of the following reasons:
a) Data is presented in a semi-structured format (JSON files), with different schemas even within a site.
b) Data is noisy, with marketing text introduced by some sites.
c) The dataset contains a large number of entries for products that, although related to cameras, are not cameras (e.g. accessories).
d) The dataset is large (30k products), making it impractical to compare each item to all the others.
e) The attributes have different characteristics (e.g. model names which are short and seem like serial numbers, vs. descriptions which are long and free-text)
f) The ground truth is only partially made available.
As a result, the task requires solutions for schema alignment, data cleaning, filtering for non-products, specialized blocking, attribute-specific similarity metrics and propagation of the known ground truth is of importance.

In the project we seek to solve all these challenges by building a pipeline consisting of the following steps:
1) Weakly supervised label assignation to distinguish products from non-products, filtering-out the latter from the pipeline.
2) Data cleaning for products and convergence to a single schema.
3) Blocking of products based on similarity metrics and representations (including word embeddings) designed per attribute.
4) Classification using attribute features and block-level features that allow the propagation of the knowledge accumulated.

During the project we will iterate on approaches to the outlined steps, coming up with innovative solutions that aim to be competitive in the leaderboard for the programming contest."
