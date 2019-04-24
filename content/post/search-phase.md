
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
The First phase of the project “search” implementation has been successfully completed by
me. In this the user will be able to search with movie title and search engine will retrieve the
movie title, overview, rating and genres. Except deploying it in public server.
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
