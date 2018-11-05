### Schema

#### Definition

###### Types
Dgraph Type | Go type           
------------|---------
default     | string            
int         | int64
float       | float            
string      | string
bool        | bool         
dateTime    | time.Time         
geo         | go-geom
password    | string (encrypted)
uid         | uint64

###### Indexes
Dgraph Type | Index
------------|---------
int         | int             
float       | float             
bool        | bool
dateTime    | year(default), month, day, hour
geo         | geo
string      | hash, exact, term, fulltext
uid         | reverse, count


#### Examples

###### Define a schema
    director.film: uid @reverse .
    genre: uid @reverse .
    initial_release_date: dateTime @index(year) .
    name: string @index(term) @lang .
   
###### Define predicates with list type
    occupations: [string] .
    score: [int] .
