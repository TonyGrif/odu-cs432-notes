Web searching requires [[#Web Crawling | web crawling]], [[#Indexing | indexing]], and [[#Ranking | ranking]].
# Web Crawling
A web crawler is a program used to fetch a page, place all links found in that page in a queue, run some function, and continue for each URL in queue.

The largest web crawlers are called *broad crawlers*. There are also *vertical crawlers* that focus on a subset of [[The Web and Internet#The Web | the Web]] and *focused crawlers* that focus on specific content.
## Evaluation
* Precision: How much extra stuff was acquired?
* Recall: How much was missed?
# Indexing
After [[#Web Crawling | crawling]], content is indexed and links stored in a link database for later analysis. Text found in files are converted to tokens, which could use stemming & lower case. The *inverted index* can then be created to display tokens and which pages they are located in.
## Document-Based Partitioning
A type of index where each document only appears in a single partition. To do this, the words are replicated over partitions. This makes it easier to add a document, but harder to add terms. Each partition can be searched in parallel, aiding speed and efficiency.
## Term-Based Partitioning
A type of index where each term has its own space in a partition and not split across multiple. Querying in this partitioning is much less trivial than [[#Document-Based Partitioning | document-based partitioning]]. A single machine will also have to fetch the result for each term. Finally, indexing a new document will require the entire index to be rebuilt.
# Ranking
Ranking a web page refers to analyzing the content found to determine how relevant a document is to the query.
## Content Analysis
These methods involve ranking based on the documents returned from a query.
### Term Frequency (TF)
This involves counting the number of times the query term appears in the document. Pages with higher term frequencies get a higher rank. To normalize and not punish short documents, simply divide the TF by the number of total words in the document.

This method is very susceptible to spamming. Search engines flag pages with an abnormally high TF score as potential spam. 
### Inverse Document Frequency (IDF)
Some terms are used frequently enough that they are not useful when discerning documents from one another. In this case, less frequently used terms are more helpful. This is IDF and it is calculated as the total docs in the corpus (search engine) divided by the number of documents with the term returned from a query.

The IDF will grow with the size of the corpus. To prevent this, the formula changes to $log_2($ total docs in corpus / docs with the term $)$.
### TF-IDF
This is the terms [[#Term Frequency (TF) | TF]] $\times$ the terms [[#Inverse Document Frequency (IDF) | IDF]]. For a document with $n$ terms, simply take the sum of their TF-IDF scores.
## Link Based Metrics
These methods provide a more successful method to rank pages.
### PageRank
Links are viewed as a recommendation system. The more [[Web Architecture#Web Structure | in-links]] to a page, the more important that the page is. The more [[Web Architecture#Web Structure | out-links]] a page has, the less weight the page's links carry.
### Hyperlink-Induced Topic Search (HITS)
This method is made up as hubs (pages with out-links to informative web pages) and authority (informative page with many in-links).