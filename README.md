# Applying words representations in embeddings (Bert, w2v) to automatic categorization of posts problem.
This is my bachelor thesis and consists of algorithm I developed for myself. However, it is not hard and rocket since things — I've done only aggregation of well-known algos for different tasks. Probably it could be helpful to someone (I hope).

So, the main problem in Hyppr (company I did this for) was in lack of recommender system. I was student at that moment so decided to kill two rabbits with one bullets: dive into Bert and text representation in general and make some simple recommender. 

Posts in this SN either an image or the video (which could be represented as discrete set of images). Using Google API, we got some simple objects set for the image. This is crucial moment — getting a set of **words** instead of pictures. And then we could play as we want — in my work I used [RoBERTa](https://arxiv.org/abs/1907.11692) model, [BERTopic](https://github.com/MaartenGr/BERTopic) and classic w2v + tf-idf. 

In the end model with w2v+tf-idf showed best quality. There is a simple reason for it: in each set for each image objects, or _words_ were not connected to each other, hereby causing bad quality for sequence2sequence models (as for the Bert)
