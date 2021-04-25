- [X] We will use tv-show.json data in all excercise

#### Example 1. Count number of collection in the document
##### query
```db.movie.count()``` or ```db.movie.find().count()```
##### result
```240```
#### Example 2. Find all collection where name is 'Arrow'
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

#### Example 2. Find all collection where name is 'Arrow'
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
#### Example 2. Find all collection where schedule day is 'Monday'
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
#### Example 3. Find all collection whose genres is 'Thriller' and rating is 8
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
#### Example 4. Find all collection where 'Thriller' in genres at 2nd position
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
