
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
For the Phase I, Game Finder used two references. 

1. https://github.com/AdnanOquaish/Cosine-similarity-Tf-Idf-/blob/master/DocumentParser.java

2. https://stackoverflow.com/questions/27685839/removing-stopwords-from-a-string-in-java

3. https://github.com/BhaskarTrivedi/QuerySearch_Recommentation_Classification.

The first recommendation is used for how to use application programming interface for term frequency and inverse document frequency on a dataset and also for cosine similarity, i just used this reference as a model to understand how tf-idf and cosine similarity works for the dataset.

The second recommendation is used to remove stop words from query as well as in the description column in the dataset. I used the similar API in my project.

The third recommendation i used is from bhaskar trivedi, to see how to connect from android application to flask in python anywhere server and also i reused his code for the android application user interface(as i am beginner to android).


Implementation & Challenges :
I had implemented my project in java using android studio. I had title column and plot
column where detailed description of movie is found. As am beginner in developing a
android application I faced lot of difficulties in choosing application design, deciding the
programming language to implement in, after deciding the programming language faced lot
of difficulties in starting with android studio and its environment and I referred some of the
websites like stack overflow, you tube videos on how to create basic hello world application
and launching it. After all these hurdles i faced challenges in converting the csv file to json
file , retrieving the data from json file and performing search on json and displaying the
search results back on to new activity in android is one of the most difficult part in
implementation.
When considering the column title I had removed the white spaces in the value of title
column and searched by ignoring the uppercase of the words. Next after successful
implementation it took lot of time to build the .apk file and deploying it in the android
mobile using usb debugger.
Till now I had implemented the application by storing the dataset locally instead in an
different server but if given some time am confident of meeting this requirement and I
learned a lot in this process of developing android application using the real time dataset
