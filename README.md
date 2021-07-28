# Project1_Wikipedia
##### By Vaibhav kant mishra
## INTRODUCTION
    This analysis consists of using big data tools to answer questions about datasets from Wikipedia. 
    There are a series of analysis questions, answered using Hive and MapReduce. 
    The tools used are determined based on the context for each question. 
    
## TECHNOLOGY USED
    . HDFS
    . HIVE
    . MAP REDUCE
    . PYTHON
    . TEZ
    . HADOOP
## PROBLEM STATEMENTS-
### QUESTION 1.
    Which English wikipedia article got the most traffic on January 20, 2021?
### QUESTION 2.
    What English wikipedia article has the largest fraction of its readers follow an internal link to another wikipedia article?
### QUESTION 3.
    What series of wikipedia articles, starting with Hotel California, keeps the largest fraction of its readers clicking on internal links? 
### QUESTION 4.
    Find an example of an English wikipedia article that is relatively more popular in the Americas than elsewhere.
              
## QUERY FOR THE ABOVE PROBLEMS ->
### QUERY FOR PROBLEM STATEMENT 1 : 
      Create external table target (lang string, search string, visit int, deli int)
      row format delimited
      fields terminated by ' '
      location "/tmp/project1_info";
      ==========================================================================================
      LOAD DATA INPATH '/tmp/formated_00.txt' INTO TABLE target;
      (Here the above query for loading data file in the directory will be executed for 24 times 
        as we have 24 data files for all the 24 hours data which is divided hourly)
      ===========================================================================================
      CREATE TABLE IF NOT EXISTS total_en_pageviews
      AS SELECT DISTINCT(search), SUM(visit) OVER (PARTITION BY search ORDER BY search) 
      AS total_views FROM target
      WHERE search != 'Main_Page' AND search != 'Special:Search' AND search != '-';
      ===========================================================================================
      SELECT * FROM total_en_pageviews
      WHERE total_views > 10000
      ORDER BY total_views DESC;
      ===========================================================================================
##  REFERENCE
      https://dumps.wikimedia.org/other/pageviews/2021/2021-01/
