- [X] We will use tv-show.json data in all excercise


#### Example 1. Count number of collection in the document
count() returns the total of all documents, which means duplicate documents will be counted.
##### query
```db.movie.count()``` or ```db.movie.find().count()```
##### result
```240```

#### Example 2. count all collection where 'Thriller' in genres
##### query
```db.movie.count({'genres':'Thriller'})```
##### result
```41```

#### Example 3. count all collection where name is 'Arrow'
##### query
```db.movie.count({name:'Arrow'})```
##### result
```1```

#### Example 4. count all collection where schedule day is 'Monday'
##### query
```db.movie.count({"schedule.days":'Monday'})```
##### result
```36```

#### Example 5. count distict rating collection
##### query
```db.movie.distinct('rating').length```
##### result
```39```

#### Example 6. Find all collection where name is 'Arrow'
Let's chain the ```pretty()``` method to the ```find()``` method for a prettier print of the output where each new field is written on a new line.
##### query
```db.movie.find({name:'Arrow'}).pretty()```
##### result

 ```
 { "_id" : ObjectId("608008a38ba139604add0828"),
        "id" : 4,
        "url" : "http://www.tvmaze.com/shows/4/arrow",
        "name" : "Arrow",
        "type" : "Scripted",
        "language" : "English",
        "genres" : [
                "Drama",
                "Action",
                "Science-Fiction"
        ],
        "status" : "Running",
        "runtime" : 60,
        "premiered" : "2012-10-10",
        "officialSite" : "http://www.cwtv.com/shows/arrow",
        "schedule" : {
                "time" : "20:00",
                "days" : [
                        "Monday"
                ]
        },
        "rating" : {
                "average" : 7.6
        },
        "weight" : 99,
        "network" : {
                "id" : 5,
                "name" : "The CW",
                "country" : {
                        "name" : "United States",
                        "code" : "US",
                        "timezone" : "America/New_York"
                }
        },
        "webChannel" : null,
        "externals" : {
                "tvrage" : 30715,
                "thetvdb" : 257655,
                "imdb" : "tt2193021"
        },
        "image" : {
                "medium" : "http://static.tvmaze.com/uploads/images/medium_portrait/165/414895.jpg",
                "original" : "http://static.tvmaze.com/uploads/images/original_untouched/165/414895.jpg"
        },
        "summary" : "<p>After a violent shipwreck, billionaire playboy Oliver Queen was missing and presumed dead for five years before being discovered alive on a remote island in the Pacific. He returned home to Starling City, welcomed by his devoted mother Moira, beloved sister Thea and former flame Laurel Lance. With the aid of his trusted chauffeur/bodyguard John Diggle, the computer-hacking skills of Felicity Smoak and the occasional, reluctant assistance of former police detective, now beat cop, Quentin Lance, Oliver has been waging a one-man war on crime.</p>",
        "updated" : 1536062117,
        "_links" : {
                "self" : {
                        "href" : "http://api.tvmaze.com/shows/4"
                },
                "previousepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1426875"
                },
                "nextepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1473817"
                }
        }
}
```

#### Example 7. Find all collection where genres is 'Drama'
Let's chain the ```pretty()``` method to the ```find()``` method for a prettier print of the output where each new field is written on a new line.
##### query
```db.movie.find({genres:'Drama'}).pretty()```
##### result
Total result count will be ```153```. Here we are showing one result
```
{
        "_id" : ObjectId("608008a38ba139604add0828"),
        "id" : 4,
        "url" : "http://www.tvmaze.com/shows/4/arrow",
        "name" : "Arrow",
        "type" : "Scripted",
        "language" : "English",
        "genres" : [
                "Drama",
                "Action",
                "Science-Fiction"
        ],
        "status" : "Running",
        "runtime" : 60,
        "premiered" : "2012-10-10",
        "officialSite" : "http://www.cwtv.com/shows/arrow",
        "schedule" : {
                "time" : "20:00",
                "days" : [
                        "Monday"
                ]
        },
        "rating" : {
                "average" : 7.6
        },
        "weight" : 99,
        "network" : {
                "id" : 5,
                "name" : "The CW",
                "country" : {
                        "name" : "United States",
                        "code" : "US",
                        "timezone" : "America/New_York"
                }
        },
        "webChannel" : null,
        "externals" : {
                "tvrage" : 30715,
                "thetvdb" : 257655,
                "imdb" : "tt2193021"
        },
        "image" : {
                "medium" : "http://static.tvmaze.com/uploads/images/medium_portrait/165/414895.jpg",
                "original" : "http://static.tvmaze.com/uploads/images/original_untouched/165/414895.jpg"
        },
        "summary" : "<p>After a violent shipwreck, billionaire playboy Oliver Queen was missing and presumed dead for five years before being discovered alive on a remote island in the Pacific. He returned home to Starling City, welcomed by his devoted mother Moira, beloved sister Thea and former flame Laurel Lance. With the aid of his trusted chauffeur/bodyguard John Diggle, the computer-hacking skills of Felicity Smoak and the occasional, reluctant assistance of former police detective, now beat cop, Quentin Lance, Oliver has been waging a one-man war on crime.</p>",
        "updated" : 1536062117,
        "_links" : {
                "self" : {
                        "href" : "http://api.tvmaze.com/shows/4"
                },
                "previousepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1426875"
                },
                "nextepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1473817"
                }
        }
}
```
#### Example 8. Find all collection where schedule day is 'Monday'
Let's chain the ```pretty()``` method to the ```find()``` method for a prettier print of the output where each new field is written on a new line.
##### query
```db.movie.find({schedule.days:'Monday'}).pretty()```
##### result
Total result count will be ```36```. Here we are showing one result
```
{ 
        "_id" : ObjectId("608008a38ba139604add0828"),
        "id" : 4,
        "url" : "http://www.tvmaze.com/shows/4/arrow",
        "name" : "Arrow",
        "type" : "Scripted",
        "language" : "English",
        "genres" : [
                "Drama",
                "Action",
                "Science-Fiction"
        ],
        "status" : "Running",
        "runtime" : 60,
        "premiered" : "2012-10-10",
        "officialSite" : "http://www.cwtv.com/shows/arrow",
        "schedule" : {
                "time" : "20:00",
                "days" : [
                        "Monday"
                ]
        },
        "rating" : {
                "average" : 7.6
        },
        "weight" : 99,
        "network" : {
                "id" : 5,
                "name" : "The CW",
                "country" : {
                        "name" : "United States",
                        "code" : "US",
                        "timezone" : "America/New_York"
                }
        },
        "webChannel" : null,
        "externals" : {
                "tvrage" : 30715,
                "thetvdb" : 257655,
                "imdb" : "tt2193021"
        },
        "image" : {
                "medium" : "http://static.tvmaze.com/uploads/images/medium_portrait/165/414895.jpg",
                "original" : "http://static.tvmaze.com/uploads/images/original_untouched/165/414895.jpg"
        },
        "summary" : "<p>After a violent shipwreck, billionaire playboy Oliver Queen was missing and presumed dead for five years before being discovered alive on a remote island in the Pacific. He returned home to Starling City, welcomed by his devoted mother Moira, beloved sister Thea and former flame Laurel Lance. With the aid of his trusted chauffeur/bodyguard John Diggle, the computer-hacking skills of Felicity Smoak and the occasional, reluctant assistance of former police detective, now beat cop, Quentin Lance, Oliver has been waging a one-man war on crime.</p>",
        "updated" : 1536062117,
        "_links" : {
                "self" : {
                        "href" : "http://api.tvmaze.com/shows/4"
                },
                "previousepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1426875"
                },
                "nextepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1473817"
                }
        }
}
```
#### Example 9. Find all collection whose genres is 'Thriller' and rating is 8
Let's chain the ```pretty()``` method to the ```find()``` method for a prettier print of the output where each new field is written on a new line.
##### query
```db.movie.find({'rating.average':8, 'genres':'Thriller'}).pretty()```
##### result
```
{
        "_id" : ObjectId("608008a38ba139604add082f"),
        "id" : 9,
        "url" : "http://www.tvmaze.com/shows/9/revenge",
        "name" : "Revenge",
        "type" : "Scripted",
        "language" : "English",
        "genres" : [
                "Drama",
                "Thriller",
                "Mystery"
        ],
        "status" : "Ended",
        "runtime" : 60,
        "premiered" : "2011-09-21",
        "officialSite" : null,
        "schedule" : {
                "time" : "22:00",
                "days" : [
                        "Sunday"
                ]
        },
        "rating" : {
                "average" : 8
        },
        "weight" : 87,
        "network" : {
                "id" : 3,
                "name" : "ABC",
                "country" : {
                        "name" : "United States",
                        "code" : "US",
                        "timezone" : "America/New_York"
                }
        },
        "webChannel" : null,
        "externals" : {
                "tvrage" : 28387,
                "thetvdb" : 248837,
                "imdb" : "tt1837642"
        },
        "image" : {
                "medium" : "http://static.tvmaze.com/uploads/images/medium_portrait/82/206879.jpg",
                "original" : "http://static.tvmaze.com/uploads/images/original_untouched/82/206879.jpg"
        },
        "summary" : "<p>This is not a story about forgiveness; <b>Revenge</b> is a show about retribution. Meet Emily Thorne, the newest resident of The Hamptons. When she was a little girl (and known as Amanda Clarke) her father, David Clarke, was framed for a horrific crime and subsequently sent to prison. While serving his time, the conspirators plotted and murdered David in order to prevent the truth from coming out. Emily is now back with a new identity and ready to take vengeance on the people that murdered her father and stole her childhood.</p>",
        "updated" : 1535975199,
        "_links" : {
                "self" : {
                        "href" : "http://api.tvmaze.com/shows/9"
                },
                "previousepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/154117"
                }
        }
}
```
#### Example 10. Find all collection where 'Thriller' in genres at 2nd position
Let's chain the ```pretty()``` method to the ```find()``` method for a prettier print of the output where each new field is written on a new line.
##### query
```db.movie.find({'genres.1':'Thriller'}).pretty()```
💡 Don't forget that arrays use 0-indexing here!
##### result
Total result count will be ```13```. Here we are showing one result
```
{

        "_id" : ObjectId("608008a38ba139604add082f"),
        "id" : 9,
        "url" : "http://www.tvmaze.com/shows/9/revenge",
        "name" : "Revenge",
        "type" : "Scripted",
        "language" : "English",
        "genres" : [
                "Drama",
                "Thriller",
                "Mystery"
        ],
        "status" : "Ended",
        "runtime" : 60,
        "premiered" : "2011-09-21",
        "officialSite" : null,
        "schedule" : {
                "time" : "22:00",
                "days" : [
                        "Sunday"
                ]
        },
        "rating" : {
                "average" : 8
        },
        "weight" : 87,
        "network" : {
                "id" : 3,
                "name" : "ABC",
                "country" : {
                        "name" : "United States",
                        "code" : "US",
                        "timezone" : "America/New_York"
                }
        },
        "webChannel" : null,
        "externals" : {
                "tvrage" : 28387,
                "thetvdb" : 248837,
                "imdb" : "tt1837642"
        },
        "image" : {
                "medium" : "http://static.tvmaze.com/uploads/images/medium_portrait/82/206879.jpg",
                "original" : "http://static.tvmaze.com/uploads/images/original_untouched/82/206879.jpg"
        },
        "summary" : "<p>This is not a story about forgiveness; <b>Revenge</b> is a show about retribution. Meet Emily Thorne, the newest resident of The Hamptons. When she was a little girl (and known as Amanda Clarke) her father, David Clarke, was framed for a horrific crime and subsequently sent to prison. While serving his time, the conspirators plotted and murdered David in order to prevent the truth from coming out. Emily is now back with a new identity and ready to take vengeance on the people that murdered her father and stole her childhood.</p>",
        "updated" : 1535975199,
        "_links" : {
                "self" : {
                        "href" : "http://api.tvmaze.com/shows/9"
                },
                "previousepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/154117"
                }
        }
}
```
#### Example 11. Find all collection where there is only two genres 'Thriller' and 'Drama'
Let's chain the ```pretty()``` method to the ```find()``` method for a prettier print of the output where each new field is written on a new line.
##### query
```db.movie.find({'genres':['Thriller', 'Drama']}).pretty()```
##### result
Total result count will be ```0```.
Let change oreder of Drama and Thriller

```db.movie.find({'genres':['Drama', 'Thriller']}).pretty()```

result:

Total result count will be ```4```.
THis is because it do equality check in equality order is matter. There are the way to ignore the order of array element we will see in advance queries.

```
{

        "_id" : ObjectId("608008a38ba139604add0885"),
        "id" : 98,
        "url" : "http://www.tvmaze.com/shows/98/scandal",
        "name" : "Scandal",
        "type" : "Scripted",
        "language" : "English",
        "genres" : [
                "Drama",
                "Thriller"
        ],
        "status" : "Ended",
        "runtime" : 60,
        "premiered" : "2012-04-05",
        "officialSite" : "http://abc.go.com/shows/scandal",
        "schedule" : {
                "time" : "22:00",
                "days" : [
                        "Thursday"
                ]
        },
        "rating" : {
                "average" : 7.7
        },
        "weight" : 95,
        "network" : {
                "id" : 3,
                "name" : "ABC",
                "country" : {
                        "name" : "United States",
                        "code" : "US",
                        "timezone" : "America/New_York"
                }
        },
        "webChannel" : null,
        "externals" : {
                "tvrage" : 28398,
                "thetvdb" : 248841,
                "imdb" : "tt1837576"
        },
        "image" : {
                "medium" : "http://static.tvmaze.com/uploads/images/medium_portrait/124/310268.jpg",
                "original" : "http://static.tvmaze.com/uploads/images/original_untouched/124/310268.jpg"
        },
        "summary" : "<p>Everyone has secrets… and Olivia Pope has dedicated her life to protecting and defending the public images of the nation's elite by keeping those secrets under wraps. Pope's team are at the top of their game when it comes to getting the job done for their clients, but it becomes apparent that these \"gladiators in suits\", who specialize in fixing the lives of other people, have trouble fixing those closest at hand -- their own.</p>",

        "updated" : 1535456926,
        "_links" : {
                "self" : {
                        "href" : "http://api.tvmaze.com/shows/98"
                },
                "previousepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1387071"
                }
        }
}
```
#### Example 12. Find all collection where genres is only 'Drama' and runtime is '60'
Let's chain the ```pretty()``` method to the ```find()``` method for a prettier print of the output where each new field is written on a new line.
##### query
```db.movie.find({'genres':['Drama'], runtime:60}).pretty()```
##### result
Total result count will be ```8```. Here we are showing one result
```
{
        "_id" : ObjectId("608008a38ba139604add0853"),
        "id" : 48,
        "url" : "http://www.tvmaze.com/shows/48/madam-secretary",
        "name" : "Madam Secretary",
        "type" : "Scripted",
        "language" : "English",
        "genres" : [
                "Drama"
        ],
        "status" : "Running",
        "runtime" : 60,
        "premiered" : "2014-09-21",
        "officialSite" : "http://www.cbs.com/shows/madam-secretary/",
        "schedule" : {
                "time" : "22:00",
                "days" : [
                        "Sunday"
                ]
        },
        "rating" : {
                "average" : 7.9
        },
        "weight" : 97,
        "network" : {
                "id" : 2,
                "name" : "CBS",
                "country" : {
                        "name" : "United States",
                        "code" : "US",
                        "timezone" : "America/New_York"
                }
        },
        "webChannel" : null,
        "externals" : {
                "tvrage" : 37247,
                "thetvdb" : 281623,
                "imdb" : "tt3501074"
        },
        "image" : {
                "medium" : "http://static.tvmaze.com/uploads/images/medium_portrait/0/399.jpg",
                "original" : "http://static.tvmaze.com/uploads/images/original_untouched/0/399.jpg"
        },
        "summary" : "<p><b>Madam Secretary</b> follows Elizabeth McCord, the shrewd, determined, newly appointed Secretary of State who drives international diplomacy, battles office politics and circumvents protocol as she negotiates global and domestic issues, both at the White House and at home. A college professor and a brilliant former CIA analyst who left for ethical reasons, Elizabeth returns to public life at the request of the President following the suspicious death of her predecessor. The President values her apolitical leanings, her deep knowledge of the Middle East, her flair for languages and her ability to not just think outside the box, but to not even acknowledge there is a box.</p>",
        "updated" : 1535111282,
        "_links" : {
                "self" : {
                        "href" : "http://api.tvmaze.com/shows/48"
                },
                "previousepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1431764"
                },
                "nextepisode" : {
                        "href" : "http://api.tvmaze.com/episodes/1489850"
                }
        }
}
```
### Projections
By default, MongoDB returns all fields for all matching documents as seen in all the results above. Projections reduce network overhead and processing requirements by limiting the fields that are returned in the results documents. Projections are passed as the second argument to the ```find()``` method.

Use ```<field name>: 1``` to include that field in the results document and/or use ```<field name>: 0``` to exclude that field. Note that the values ```1``` and ```0``` stand for inclusion and exclusion in the resulting document respectively.

#### Example 13. Find all collection where status is 'Running'
##### query
```db.movie.find({status:'Running'},{status:1})```
##### result
Total result count will be ```62```. Here we are showing few result

```
{ "_id" : ObjectId("608008a38ba139604add0828"), "status" : "Running" }
{ "_id" : ObjectId("608008a38ba139604add082c"), "status" : "Running" }
{ "_id" : ObjectId("608008a38ba139604add082d"), "status" : "Running" }
{ "_id" : ObjectId("608008a38ba139604add0830"), "status" : "Running" }
```
> We want only status as projection but ```_id``` is also comming. So to exclude ```_id``` we need mention it explicitly in query

#### Example 14. Find all collection where network name is 'CBS'
##### query
```db.movie.find({'network.name':'CBS'},{"network.name":1, _id:0})```
##### result
Total result count will be ```29```. Here we are showing few result

```
{ "network" : { "name" : "CBS" } }
{ "network" : { "name" : "CBS" } }
{ "network" : { "name" : "CBS" } }
{ "network" : { "name" : "CBS" } }
```

#### Example 15. Find all collection where schedule days is only 'Sunday'
##### query
```db.movie.find({'schedule.days':['Sunday']},{"schedule":1, _id:0})```
##### result
Total result count will be ```62```. Here we are showing few result

```
{ "schedule" : { "time" : "21:00", "days" : [ "Sunday" ] } }
{ "schedule" : { "time" : "22:00", "days" : [ "Sunday" ] } }
{ "schedule" : { "time" : "21:00", "days" : [ "Sunday" ] } }
```
