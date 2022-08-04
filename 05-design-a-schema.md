### While creating Schema in MongoDB what are the points need to be taken in consideration?
Points need to be taken in consideration are

- Design your schema according to user requirements
- Combine objects into one document if you use them together. Otherwise, separate them
- -Do joins while write, and not when it is on read
- For most frequent use cases optimize your schema
- Do complex aggregation in the schema