# Graph and Amazon Neptune

## presenter
Richard Elberger
elberger@amazon.com
Solutions Architect

## what is a property graph
- *vertex* or *node*: represents entities/domains
- *edge*:
  - directional relationship between vertices
  - each edge has a label that denotes the type of relationship
- each vertex and edge has a *unique identifier*
- *property*: each vertex or edge has properties

## what is an RDF graph
- RDF graphs are collections of *triples*:
  - *subject*: internationalized resource identifier (IRI)
  - *object*
  - *predicate*

## tinkerpop

## graph db applications
- recommendations based on relationships
  - ex. P1 and P2 follow Sport, P1 bought Product, recommend Product to P2
- knowledge graph applications
  - too many relationships
  - e.g. Google can solve 'who painted the mona lisa',
         but not 'what museums should friend Alice visit while in Paris'
         or 'what artists have paintings in the Louvre'
- navigate tax policies
  - Thomson Reuters use Neptune to create links with data for flobal tax solutions

## existing graph DBs

- hard to scale
- hard to maintain availability
- expensive

## amazon neptune

- fully managed graph database
- uses Apache Tinkerpop/Gremlin and RDF/SPARKQL
