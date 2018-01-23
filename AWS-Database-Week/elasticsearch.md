# Elasticsearch

## characteristics
- open source
- works with structured JSON, no schema
- *facets* and *nested facets*

## building blocks
- documents
  - core entity of search: file, db, log line, data structure
  - represented with JSON
  - referened by idx
  - field:value pairs
  - distributed across shards and replicas
- index
  - collection of docs that has fields that can be searched
  - access and index through any participating instance
- replica
  - copy of shard
  - used for availability or scale
  - scale because searches can leverage replicas in parallel
  - number of replicas can be changed dynamically
- shards
  - instance of Lucene
  - using compute, storage, other system resources
  - Elasticsearch deploys shards elastically, dynamically to the instances in the cluster
- instance
  - for Amazon ElasticSearch (AES)

## Amazon ElasticSearch (AES)
- distributed index
- fully managed
- scalable, available, reliable
-
