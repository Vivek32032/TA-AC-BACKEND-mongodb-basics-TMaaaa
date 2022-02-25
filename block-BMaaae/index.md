writeCode

Write code to:-

- create a database named `sports`.
- list all databases present in local mongod server.
- create 3 collections named `cricket`, `football`, `TT` in sports databse.
- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.
- list all collections in sports database.
- rename `TT` collection to `tennis`.
- create a capped collection called `khokho` which should have max 3 documents.
  Try inserting more than 3 and see what happens?
- check whether a collection is capped or not?
- drop all documents from `football` collection.
- delete cricket collection completely.
- delete sports database.
- check which database you are connected to ?
- connect to test database


use sports
show dbs
db.createCollection('cricket')

```data.js

var players = [
  {
    name : 'player 1',
    email : 'p1@gmail.com',
    age : 22,
    bid_price : '$20k'
  },
   {
    name : 'player 2',
    email : 'p2@gmail.com',
    age : 25,
    bid_price : '$30k'
  },
   {
    name : 'player 3',
    email : 'p3@gmail.com',
    age : 27,
    bid_price : '$25k'
  },
   {
    name : 'player 4',
    email : 'p4@gmail.com',
    age : 20,
    bid_price : '$18k'
  }

]
```
db.cricket.insertMany(players);
db.cricket.find().pretty();
show collection


db.football.insertMany(players);
db.TT.insertMany(players);

show collections
db.TT.renameCollection('tennis');
db.createCollection('khokho',{capped:true,size:2048,max:3})

db.khokho.insertMany(players);kho
show collections
db.khokho.isCapped()
db.tennis.isCapped();
db.football.find();
db.football.remove({});

db.cricket.drop();
db.dropDatabase();

db
show collections
use test
db