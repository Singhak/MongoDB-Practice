## Import tv-show.json into your mongoDB
```mongoimport --db moviesData --collection movie --file tv-show.json --jsonArray```

  If there is any error while using mongoimport command check this [blog](https://singhak.in/mongoimport-is-not-recognized-as-an-internal-or-external-command)
  
  ## After importing data
  * Connected to mongo db server
    * ```mongo```
  * List all dbs ( If data imported successfully then moviesData db will show in list)
    * ```show dbs```
  * Now use movies Data db
    * ```use moviesData```
  * Now list down the collection of db
    * ```show collections```
* Now check number of documents in collection
  * ```db.movie.count()```
