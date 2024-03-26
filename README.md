# Assignment-3-MongoDB-Setup-and-Queries

Kevin O'Connell

CS:3980

03/26/2024

## Show MongoDB is Downloaded 

<img width="1422" alt="Screen Shot 2024-03-26 at 12 43 38 PM" src="https://github.com/KevinOConnell7/Assignment-3-MongoDB-Setup-and-Queries/assets/45603150/fd252a91-3696-4950-9deb-7b35170dcc4c">

## Query 1

Here is query I ran:

db.movies.find(
  { year: 1983, runtime: { $gt: 200 } },
  { _id: 0, runtime: 1, title: 1, year: 1 }
).sort({ runtime: 1 })


Here is the output after I ran the first query.

<img width="358" alt="Screen Shot 2024-03-26 at 12 45 23 PM" src="https://github.com/KevinOConnell7/Assignment-3-MongoDB-Setup-and-Queries/assets/45603150/a0675052-05d1-4ae6-90cc-df7d6f43c337">


## Query 2

Here is query I ran:

db.movies.find(
  {
    "year": { $gt: 2014 },
    "imdb.rating": { $gt: 9 }
  },
  {
    "_id": 0,
    "title": 1,
    "year": 1,
    "imdb.rating": 1
  }
).sort({ "imdb.rating": -1 })

Here is the output after I ran the Second query.

<img width="541" alt="Screen Shot 2024-03-26 at 12 44 47 PM" src="https://github.com/KevinOConnell7/Assignment-3-MongoDB-Setup-and-Queries/assets/45603150/dd42de19-63ad-4f88-8e62-1e90e264168b">

