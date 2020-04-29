Recommendations in News Industry
--------------------------------

Challanges
----------

* The system must perform well on fresh content (Item Cold Start Problem)

Content-based filtering
-----------------------

1. Based on article tags & user's interaction data build user profile
2. Match user profile with article profile

Less diversity/hard to show recs out of user intrests

Collaborative Filtering
-----------------------

1. Learn user item embeddings
2. Match users withe items

Item Cold Start Problem

Hybrid Method
-------------

[Collaborative Topic Modeling
for Recommending Scientific Articles KDD 2011](http://www.cs.columbia.edu/~blei/papers/WangBlei2011.pdf)
1. Model articles using LDA
2. Adjust the LDA via behavioural data of user-article interaction (Contribution of the paper)
3. Model user by avaraging article Topics
4. Use cosine similarity between aeticle and user
