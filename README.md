# The Aggregation Pipeline: Demo Activity

## Problem:

Noa began to create the following query on the movies collection in the sample_mflix database with MQL, but quickly realized that they will need to build an aggregation pipeline for the task that they wish to complete:

```txt
db.movies.find(
    {"imdb.rating": { $gt: 8}, "year": { $gt: 2000}},
    {"title": 1, "year": 1, "imdb.rating": 1, "genres": 1, "_id": 0}).pretty()
```