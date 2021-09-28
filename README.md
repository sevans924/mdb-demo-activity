# The Aggregation Pipeline: Demo Activity

## Problem:

Noa began to create the following query on the movies collection in the sample_mflix database with MQL, but quickly realized that they will need to build an aggregation pipeline for the task that they wish to complete:

```txt
db.movies.find(
    {"imdb.rating": { $gt: 8}, "year": { $gt: 2000}},
    {"title": 1, "year": 1, "imdb.rating": 1, "genres": 1, "_id": 0}).pretty()
```

## Activity

1. Help Noa by converting their MQL query into an aggregation pipeline.

* **Hint:** Your pipeline should include 2 stages: **$match** and **$project**

2. Once you've converted the MQL query into an aggregation pipeline, add a final stage that **groups** the documents by genres.

* **Hint:** Visit the [$group docs](https://docs.mongodb.com/manual/reference/operator/aggregation/group/#mongodb-pipeline-pipe.-group) to learn more about syntax 
* **Hint:** The final result should be an array of 20 objects

### Remember:

* Test out your pipeline using the movies collection in the sample_mflix database in the cluster that you set up in MongoDB Atlas.
* Once you are finished, you can compare your solution at each stage of the activity to solutions in [the 'Solved' directory](./Solved).

### Optional Extension:

1. Change the **$group** stage to the **$sort** stage.

2. Use the **$sort** stage to sort the movie documents by rating in **descending** order.

## Resources

* [Aggregation](https://docs.mongodb.com/manual/aggregation/)
* [Aggregation Pipeline Stages](https://docs.mongodb.com/manual/reference/operator/aggregation-pipeline/)
* [Query and Projection Operators](https://docs.mongodb.com/manual/reference/operator/query/)
