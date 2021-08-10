# **Technical Paper on Full-Text Search**

Written by **Gopal Pal**

## **Table of Content**

    * What is Full-Text Search
    * Why do we need it?
    * Example of Full-Text Search
    * Elasticsearch
    * Solr
    * Lucene
    * References

## **What is Full-Text Search?**

Full-text search is the technique used by search engines to find data from the database. The Full-Text Search helps to guess what the user wants and return them the best matching data. Suppose inputs have more than a single word Full-Text Search can returns result in different order separated by words. Database Management systems like MySQL allow partial text lookups using "LIKE" clauses. However, these requests are not suitable in a large database and are also limited to matching the searched input exactly, sometimes it may not produce results even when data is relevant. The Full-Text Search can build a more powerful text search engine without using any advanced tools. Here is an example, In a small Database we try to search data by using the Full 

## **Why do we need it?**

The full-text search may be useful when one needs to search for:

    1. a name of the person in a list or a database;
    2. a word or a phrase in a document;
    3. a web page on the internet;
    1. products in an online store, etc.
    2. a regular expression.
Full-text search results can be used as an input for a replacement of phrases and in the process of related word forms search, etc.

## **Example**

    Employee Table Contains four columns, 
    1. EmpId, 
    2. EmpName,
    3. Department,
    4. Location.
    
Now, We will make an index for using Full-Text Search. To do this, we will use MySQL query "FULLTEXT"

***mysql> ALTER TABLE Employee ADD FULLTEXT (EmpName, Department, Location);***

This query works by combining all the text columns and sanitizing them (for example removing the punctuation and making uppercase letters lowercase). Now, this index is created, it will be updated by any SQL query that changes the content of the source table.

## **Elasticsearch**

Elasticsearch is a distributed, Full, open search and analytics engine for all types of data, including textual, numerical, geospatial, structured, and unstructured. It provides a distributed, multitenant-capable Full-text search engine with an HTTP web interface and schema-Full JSON documents. It is certainly possible to use Elasticsearch as a primary store when the limitations described are not showstoppers. One good example is when using Logstash. Logstash is a fantastic tool for managing logs and shoving them into Elasticsearch, perhaps also archiving them somewhere else just in case. Logs are written once, read many. No updating, no need for transactions, integrity constraints, etc.

## **Solr**

Solr is an open-source enterprise-search platform. Its major features include Full-Text Search, hit highlighting, faceted search, real-time indexing, dynamic clustering, database integration, NoSQL features, and rich document handling. For every value of a numeric field, Lucene stores several values with different precisions. This allows Lucene to run range queries very efficiently. Since your use-case seems to leverage numeric range queries a lot, this may explain why Solr is so much faster.

## **Lucene**

Lucene is a Java library providing powerful indexing and search features, as well as spellchecking, hit highlighting, and advanced analysis/tokenization capabilities. One of the main reasons that Apache Lucene is considered in such high regard is that it can return search responses quickly.

## **References**

- https://en.wikipedia.org/wiki/Full-text_search
- https://blog.issart.com/Full-text-search-how-it-works/
- https://www.digitalocean.com/community/tutorials/how-to-improve-database-searches-with-Full-text-search-in-mysql-5-6-on-ubuntu-16-04
