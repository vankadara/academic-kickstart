
+++
title = "Recommendation systems Report Phase 2" 
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
The Moto in doing this project is to develop a movie recommendation android applicaton, as part of this project, second phase is to develop a classifier in which user enters the sentence and based on training dataset using niave bayes classifier it will classify in to one of the generes.

Dataset Link:
https://drive.google.com/open?id=1wSPSLCX8AJ35P1ssgPPe1gwsTmZL-3mO

References
For the Phase II, used three references. 

https://stackoverflow.com/questions/27685839/removing-stopwords-from-a-string-in-java

https://github.com/BhaskarTrivedi/QuerySearch_Recommentation_Classification.

https://machinelearningmastery.com/


Implementation :

For implementing the classification i used naive bayes algorithm. Naive Bayes model is easy to build and particularly useful for very large data sets. Along with simplicity, Naive Bayes is known to outperform even highly sophisticated classification methods.

Bayes theorem provides a way of calculating posterior probability P(c|x) from P(c), P(x) and P(x|c). 

                    P(c/x) = (P(x/c) * p(c) ) / p(x)

P(c|x) is the posterior probability of class (c, target) given predictor (x, attributes).
P(c) is the prior probability of class.
P(x|c) is the likelihood which is the probability of predictor given class.
P(x) is the prior probability of predictor.

TO read the movie dataset file i used following code 
                    
                    data = pd.read_csv("../input/movie_metadata.csv")
                   
To split the movie dataset into training and test i used below code

                    def splitDataset(dataset, splitRatio):
	trainSize = int(len(dataset) * splitRatio)
	trainSet = []
	copy = list(dataset)
	while len(trainSet) < trainSize:
		index = random.randrange(len(copy))
		trainSet.append(copy.pop(index))
	return [trainSet, copy]
          
 For calculating the class probabilities
 
                    def calculateClassProbabilities(summaries, inputVector):
	probabilities = {}
	for classValue, classSummaries in summaries.iteritems():
		probabilities[classValue] = 1
		for i in range(len(classSummaries)):
			mean, stdev = classSummaries[i]
			x = inputVector[i]
			probabilities[classValue] *= calculateProbability(x, mean, stdev)
	return probabilities
          
And after calculating class probabilities for the code, i used top 1 result to show the genre, the given query belongs to.

#Challenges:
	
The challenging part in building the classifier is to knowing the algorithm and implementing the algorithm and especially in stage of calculating the class probablities and computing the class to which the query belongs to. But i used the materials given by professor and those were very helpful and handy while designing the entire project.


