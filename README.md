
# Facebook Page Classifier

The [facebook_large dataset](https://github.com/TimKong21/Facebook-page-classifier/tree/main/facebook_large) contains page-page graph of verified Facebook sites. 
This graph was collected through the Facebook Graph API in November 2017 
and restricted to pages from four categories which are defined by Facebook. 
Multi-class node classification on the Facebook sites is performed in this repository.

## Dataset
There are nodes and edges in the dataset. They are:

[musae_facebook_target.csv](https://raw.githubusercontent.com/TimKong21/Facebook-page-classifier/main/facebook_large/musae_facebook_target.csv)
- Nodes are the oficial Facebook pages with unique ids.
- Each page is labelled with the page type - **tvshow**, **government**, **company**, **politician**.

[musae_facebook_edges.csv](https://raw.githubusercontent.com/TimKong21/Facebook-page-classifier/main/facebook_large/musae_facebook_edges.csv)
- Edges are the mutual likes between the Facebook pages
- There could be no relarionships, one-to-one or one-to-many relationships.

## Notebook
[Facebook page classifier.ipynb](https://github.com/TimKong21/Facebook-page-classifier/blob/main/Facebook%20page%20classifier.ipynb)
contains the step for node classification. Through the process, every node is assigned a specific label. A predefined percentage of random nodes is used to train the classifier, while the rest serves as test data for evaluating the embedding method and specific classifier.
The implementation can be divided into four main steps:

    1. Calculate and save node embeddings for the whole graph.
    2. Split the node embeddings into training and testing sets.
    3. Train the classifier.
    4. Evaluate the classifier on the test data.
## Acknowledgements

 - [Node embeddings visualization reference](https://stellargraph.readthedocs.io/en/stable/demos/node-classification/node2vec-node-classification.html)
 - [Node classification algorithms reference](https://github.com/memgraph/graph-analytics-course/blob/master/lecture-5/node-classification/classifier.py)
  