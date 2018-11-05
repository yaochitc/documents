### Facets

###### Create
    uid_node1 <edge> uid_node2 (facet1=xxx, facet2=xxx)
    
###### Query
    edge @facets 
    edge @facets(facet1)       # query facet1 only
    edge @facets(facet1: f1)   # query facet1 with alias f1
    
