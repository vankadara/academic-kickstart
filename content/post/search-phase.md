
+++
title = "Recommendation systems Report Phase 1" 
date = 2018-12-21T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Vishnu Vardhan Vankadara"]

#List format.
#0 = Simple
#1 = Detailed
#2 = Stream
list_format = 2

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Server","Installation"]

# Step to follow.


#Optional featured image (relative to static/img/ folder).
[header] 
image = "" 
caption = "" 
+++
The Moto in doing this project is to develop a movie recommendation android applicaton, as part of this project, first phase is to develop a search engine in which user enters the query or description text and based on that the search engine displays top 3 results that matches the description of the movie in the movie dataset.

Dataset Link:
https://drive.google.com/open?id=1wSPSLCX8AJ35P1ssgPPe1gwsTmZL-3mO

References
For the Phase I, used three references. 

1. https://github.com/AdnanOquaish/Cosine-similarity-Tf-Idf-/blob/master/DocumentParser.java

2. https://stackoverflow.com/questions/27685839/removing-stopwords-from-a-string-in-java

3. https://github.com/BhaskarTrivedi/QuerySearch_Recommentation_Classification.

The first recommendation is used for how to use application programming interface for term frequency and inverse document frequency on a dataset and also for cosine similarity, i just used this reference as a model to understand how tf-idf and cosine similarity works for the dataset.

The second recommendation is used to remove stop words from query as well as in the description column in the dataset. I used the similar API in my project.

The third recommendation i used is from bhaskar trivedi, to see how to connect from android application to flask in python anywhere server and also i reused his code for the android application user interface(as i am beginner to android).

Implementation :

TF: Term Frequency, which measures how frequently a term occurs in a document. Since every document is different in length, it is possible that a term would appear much more times in long documents than shorter ones. Thus, the term frequency is often divided by the document length (aka. the total number of terms in the document) as a way of normalization: 

TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document).

IDF: Inverse Document Frequency, which measures how important a term is. While computing TF, all terms are considered equally important. However it is known that certain terms, such as "is", "of", and "that", may appear a lot of times but have little importance. Thus we need to weigh down the frequent terms while scale up the rare ones, by computing the following: 

IDF(t) = log_e(Total number of documents / Number of documents with term t in it).

Then i generated the document vector by using the above tf and idf and converted the user search query as query vector.

In the next step i found the cosine similarity between two vectors(query and document)

                          Similarity  = cosθ = (a.b) / (||a||||b||)
Here, a -> query vector and b -> document vector.

