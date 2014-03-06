Detecting Newsworthy Topics in Twitter
======================================

In this project, you can find implementations of the different parts of our methodology described in our paper with title 'Detecting Newsworthy Topics in Twitter'.

### Step 1 - News Publisher Detection
For this step, we used this freely available WEKA implementation: 
http://weka.sourceforge.net/doc.stable/weka/classifiers/bayes/BayesNet.html

with parameters
* -Q weka.classifiers.bayes.net.search.local.K2
* -E weka.classifiers.bayes.net.estimate.SimpleEstimator


### Step 2 - Topic Detection

Java application cluster.jar contains the implementation of this step. You can run the jar file using this command:

java -jar cluster.jar 'tweetfile_news_publishers' 'tweetfile_all' 'dirname' 'minPts' 'epsilon' '#minutes in block'

with

* 'tweetfile_news_publishers' the name of the file which contains the tweets posted by the news publishers
* 'tweetfile_all' the name of the file which contains all tweets
* 'dirname' the name of the folder in which the output will come
* 'minPts' the minimum points parameter of the DBSCAN algorithm
* 'epsilon' the epsilon parameter of the DBSCAN algorithm
* '#minutes in block' the length of the time intervals of interest, in minutes


### Step 3 - Topic Ranking
For this step, we used this freely available WEKA implementation: 
http://weka.sourceforge.net/doc.stable/weka/classifiers/functions/SMO.html

wit parameters
* -C 2


### Step 4 - Topic Enrichment

Java application summarize.jar contains the implementation of this step. You can run the jar file using this command:

java -jar summarize.jar 'tweetfile_all' 'dirname_topics'

with

* 'tweetfile_all' the name of the file which contains all tweets
* 'dirname_topics' the name of the folder which contains the obtained topics


Questions
-------------

In case you have any questions, feel free to contact me. My contact information can be found at http://www.linkedcubes.com/.