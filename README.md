# Project1_Wikipedia
##### By Vaibhav kant mishra
## INTRODUCTION
    This analysis consists of using big data tools to answer questions about datasets from Wikipedia. 
    There are a series of analysis questions, answered using Hive and MapReduce. 
    The tools used are determined based on the context for each question. 
    The output of the analysis includes MapReduce jarfiles and .hql files so that the analysis is a repeatable process that works on a larger dataset.
    
## TECHNOLOGY USED
    . HDFS
    . HIVE
    . MAP REDUCE
    . PYTHON
    . TEZ
    . HADOOP
## FEATURES
    1.  Process the downloaded data analyze the datasets.
    2.  Find, organize, and format pageviews on any given day.
    3.  Follow clickstreams to find relative frequencies of different pages.
    4.  Find the different way to analyze the most internal search link fraction of hotel california.

## GETTING STARTED

Most of the code was done using HQL in a Hive GUI interface via Data Analysis studio

    1. Download Hortonworks community Edition -https://www.cloudera.com/downloads/hortonworks-sandbox/hdp.html
    2. Install Hortonworks on your machine or virtual machine - https://www.virtualbox.org/wiki/Downloads
    3. Download Git Bash on your computer - https://git-scm.com/downloads
    4. Clone my code - git clone https://github.com/vaibhavkantmishra/Project1_Wikipedia.git
    5. Setup a Hortonworks in virtual machine, import pageview and clickstream data in hdfs, and start queryin the with hive.


## PROBLEM STATEMENTS-
### QUESTION 1.
    Which English wikipedia article got the most traffic on January 20, 2021?
### QUESTION 2.
    What English wikipedia article has the largest fraction of its readers follow an internal link to another wikipedia article?
### QUESTION 3.
    What series of wikipedia articles, starting with Hotel California, keeps the largest fraction of its readers clicking on internal links? 
### QUESTION 4.
    Find an example of an English wikipedia article that is relatively more popular in the Americas than elsewhere.
              
## USAGE

    1. The HQL commands can be used on similar large datasets, specifically those found in Wikipedia dumps - https://dumps.wikimedia.org/
    2. This script was designed to answer all sorts of questions pertaining to big data.      

      
##  REFERENCE
      https://dumps.wikimedia.org/other/pageviews/2021/2021-01/
