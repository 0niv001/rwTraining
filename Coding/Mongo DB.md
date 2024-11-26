---
sticker: lucide//layers
---
NoSQL DB used by modern apps, they allow for more flexibility. 
Data format of JSON and BSON (Binary JSON)
Very commonly used with JS (MERN - Mongo, Express, React, Node). 

**MacOS Service
- `brew services start mongodb-community@8.0` to start MongoDB
- `brew services stop mongodb-community@8.0` to stop MongoDB
- `mongosh` to start the MongoDB Shell (JS Shell)

**CRUD**
- Database > Collections > Objects
- Object IDs are automatically generated if none are specified
- `show databases`
- `use {databaseName}` - Creates new DB
- `show collections` - Data needs to be stored in a collection. 
- `db.collName.insertOne({}) or Many([{},{}])`  
- `db.collName.find()` - Shows data in the collection
- `db.collName.find({key:value})` - Filters out the data `findOne()`for only first result
- `db.colName.updateOne({filter} {$set: {filed:value}})/updateMany()`  - Can also be used to add new Key:Value pair
- `db.colName.replaceOne()`
- `db.colName.deleteOne({filter})/deleteMany({})` - Deletes whole object. 

**Operators**
- $ and, or, not, nor
- $ gt ,gte > >=
- $ eq ==
- $lt, lte < <=
- $in : \[ ]
## Mongoose
- **ODM** - Object data mapper, connects node to Mongo turning data into JS Objects. 
- Allows to set schemas that data needs to follow. 
- Models are JS objects

**Creating Models**
- `.connect(/databaseName)`
- `const schemaName = new mongoose.Schema({name: Type});` to create new schema. 
- `const CollName = mongoose.model("Collection", schemaName);` create collectiotn. 
- `const "item" = new CollName({properties});` create new class / objec
- `item.save()` - Save to DB.


- `item.property = new` change values
- `Model.find({filter}).then(data => console.log(data))`
- `.load file.js` do this inside Node REPL

*Updating in Mongoose*
- updateOne({filter:}, {change:})
- updateMany({filter:}, {change:})

*Deleting:
- Model.remove()