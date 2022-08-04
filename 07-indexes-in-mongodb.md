### What are Indexes in MongoDB?

In MondoDB, Indexes are used to execute query efficiently. Without indexes, MongoDB must scan every document in a collection. MongoDB can use the index to limit the number of documents it must inspect.

Indexes are special data structures that store a small portion of the collection's data set in an easy to traverse form. The index stores the value of a specific field or set of fields, ordered by the value of the field. The ordering of the index entries supports efficient equality matches and range-based query operations. In addition, MongoDB can return sorted results by using the ordering in the index.


#### Indexes Types

- **Single Field**

- **Compound Index**: MongoDB supports user-defined indexes on multiple fields, 

- **Hashed Index**

- **Clustered Index**

- **Partial Index**

- **Sparse Index**