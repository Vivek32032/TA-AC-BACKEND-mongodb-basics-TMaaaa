writeCode

Write code to:-

- create a database named `mountains`
- a collection inside that database named `himalayas`
- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`

- insert multiple document using insertMany command
- find all documents from mountains
- find a single document using name

use mountains
db.createCollection('himalayas')
db.himalayas.insert({name:'Dhauldhar range, height: '4000 meter'})
show collection

let mountains = [
    {
        name: 'Himalaya range',
        height: '5500 meter'
    },
    {
        name: 'Shivalik range',
        height: '6000 meter'
    }
  ]

  db.himalayas.insertMany(mountains;

  db.himalayas.find()
  db.himalayas.find({name: 'Shivalik range'})
