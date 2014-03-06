Detecting Newsworthy Topics in Twitter
======================================

In this project, you can find implementations of the different parts of our methodology described in our paper with title 'Detecting Newsworthy Topics in Twitter'.

### Step 1 - News Publisher Detection
For this step, we used this freely available WEKA implementation: 
http://weka.sourceforge.net/doc.stable/weka/classifiers/bayes/BayesNet.html

with parameters
* -Q weka.classifiers.bayes.net.search.local.K2
* -E weka.classifiers.bayes.net.estimate.SimpleEstimator


### Step 3 - Topic Ranking
For this step, we used this freely available WEKA implementation: 
http://weka.sourceforge.net/doc.stable/weka/classifiers/functions/SMO.html

wit parameters
* -C 2

Questions
-------------

In case you have any questions, feel free to contact me. My contact information can be found at http://www.linkedcubes.com/.