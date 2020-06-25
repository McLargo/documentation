## MONGO DB

few samples to conver main mongo db funcionalities:

show databases -> `show dbs`

to create/use a new database -> `use <db-name>`

show collections inside a db -> `show collections`

find items -> `db.collection.find({"_id" : <key>)})`

find one item -> `db.collection.findOne()`

insert one item into a collection -> `db.collection.insert({"name":"tutorial"})`

update item -> `db.collection.replaceOne({name: "sue" },{name: "amy", age: 25, score: "enrolled"})`

delete item in collection -> `db.collection.remove({"_id": ObjectId("5694db974267b99946531030")} )`

many other funcionalities are in mongo db. like update, findAndModify, insertMany, count, aggregate....