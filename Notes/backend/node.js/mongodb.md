

## What is a Database?

A database is a collection of organized data that can be stored, managed, and retrieved efficiently.

Examples of data stored in a database:

- Users
- Products
- Orders
- Employees
- Student Records

Without a database, applications would lose all data when they restart.



## What is MongoDB?

MongoDB is a **NoSQL** database that stores data in **documents** instead of tables.

Unlike traditional SQL databases, MongoDB stores data in a flexible JSON-like format called **BSON (Binary JSON)**.

Example:

```json
{
    "name": "Deepthi",
    "age": 22,
    "city": "Bangalore"
}
```

MongoDB is fast, scalable, and widely used in modern web applications.



## Why MongoDB?

MongoDB is popular because it offers:

- Flexible schema
- High performance
- Easy scalability
- JSON-like document storage
- Easy integration with Node.js
- Suitable for large applications



## SQL vs NoSQL

| SQL | NoSQL |
|------|--------|
| Stores data in tables | Stores data in documents |
| Fixed schema | Flexible schema |
| Uses rows and columns | Uses JSON-like documents |
| Example: MySQL, PostgreSQL | Example: MongoDB |

Example SQL Table:

| id | name | age |
|----|------|-----|
| 1 | Deepthi | 22 |

MongoDB Document:

```json
{
    "_id": "...",
    "name": "Deepthi",
    "age": 22
}
```



## Database, Collection and Document

MongoDB organizes data into three levels.

```
Database
   │
   ▼
Collection
   │
   ▼
Documents
```

Example:

```
Database
    CollegeDB

Collections
    Students
    Teachers
    Courses

Documents
    {
        "name":"Deepthi",
        "age":22
    }
```

Think of it like this:

| SQL | MongoDB |
|------|----------|
| Database | Database |
| Table | Collection |
| Row | Document |



## What is a Document?

A document is a single record stored in MongoDB.

Example:

```json
{
    "name": "Deepthi",
    "email": "deepthi@gmail.com",
    "age": 22,
    "skills": ["Node.js", "Express"]
}
```

Each document is stored as BSON internally.



## What is a Collection?

A collection is a group of related documents.

Example:

```
Users Collection

User 1

User 2

User 3
```

Collections are similar to tables in SQL.



## What is BSON?

MongoDB stores data internally as **BSON (Binary JSON)**.

BSON supports additional data types such as:

- Date
- ObjectId
- Boolean
- Array
- Decimal
- Binary Data

Developers usually work with JSON, while MongoDB stores BSON behind the scenes.



## ObjectId (_id)

Every MongoDB document automatically gets a unique identifier.

Example:

```json
{
    "_id": "687dabc12ef456...",
    "name": "Deepthi"
}
```

The `_id` field uniquely identifies every document in a collection.



## Installing MongoDB

There are three common ways to use MongoDB:

- MongoDB Community Server (Local)
- MongoDB Compass (GUI)
- MongoDB Atlas (Cloud Database)

For most projects, developers use **MongoDB Atlas**.



## MongoDB Compass

MongoDB Compass is the official graphical interface for MongoDB.

It allows you to:

- View databases
- Create collections
- Insert documents
- Update documents
- Delete documents
- Run queries



## MongoDB Atlas

MongoDB Atlas is MongoDB's cloud database service.

Benefits:

- Free cluster available
- Accessible from anywhere
- Automatic backups
- High availability
- Easy connection with Node.js applications



## MongoDB Shell

MongoDB provides an interactive shell called **mongosh**.

Example:

```bash
mongosh
```

This allows you to execute MongoDB commands directly.



# Basic MongoDB Commands

## Show Databases

```javascript
show dbs
```

Displays all available databases.



## Create or Switch Database

```javascript
use CollegeDB
```

If the database does not exist, MongoDB creates it automatically when data is inserted.



## Show Current Database

```javascript
db
```



## Show Collections

```javascript
show collections
```



## Create Collection

```javascript
db.createCollection("students")
```



## Insert One Document

```javascript
db.students.insertOne({
    name: "Deepthi",
    age: 22
})
```



## Insert Multiple Documents

```javascript
db.students.insertMany([
    {
        name: "Rahul",
        age: 21
    },
    {
        name: "Anjali",
        age: 23
    }
])
```



## Find All Documents

```javascript
db.students.find()
```



## Find One Document

```javascript
db.students.findOne()
```



## Find Using Condition

```javascript
db.students.find({
    age: 22
})
```



## Update One Document

```javascript
db.students.updateOne(
    {
        name: "Deepthi"
    },
    {
        $set: {
            age: 23
        }
    }
)
```



## Delete One Document

```javascript
db.students.deleteOne({
    name: "Rahul"
})
```



## Delete Many Documents

```javascript
db.students.deleteMany({})
```

Deletes all documents inside the collection.



## Drop Collection

```javascript
db.students.drop()
```



## Drop Database

```javascript
db.dropDatabase()
```



# CRUD Operations

CRUD stands for:

| Operation | MongoDB Command |
|------------|-----------------|
| Create | insertOne(), insertMany() |
| Read | find(), findOne() |
| Update | updateOne(), updateMany() |
| Delete | deleteOne(), deleteMany() |



## Query Operators

MongoDB provides operators for filtering data.

Greater Than

```javascript
db.students.find({
    age: {
        $gt: 20
    }
})
```

Less Than

```javascript
db.students.find({
    age: {
        $lt: 25
    }
})
```

Greater Than or Equal

```javascript
db.students.find({
    age: {
        $gte: 22
    }
})
```

Less Than or Equal

```javascript
db.students.find({
    age: {
        $lte: 22
    }
})
```



## Comparison Operators

| Operator | Meaning |
|-----------|---------|
| $gt | Greater Than |
| $lt | Less Than |
| $gte | Greater Than or Equal |
| $lte | Less Than or Equal |
| $eq | Equal |
| $ne | Not Equal |



## Logical Operators

AND

```javascript
db.students.find({
    age: {
        $gt: 20
    },
    city: "Bangalore"
})
```

OR

```javascript
db.students.find({
    $or: [
        {
            city: "Bangalore"
        },
        {
            age: 25
        }
    ]
})
```



## Sorting

Ascending Order

```javascript
db.students.find().sort({
    age: 1
})
```

Descending Order

```javascript
db.students.find().sort({
    age: -1
})
```



## Limiting Results

```javascript
db.students.find().limit(5)
```



## Skipping Results

```javascript
db.students.find().skip(5)
```



## Count Documents

```javascript
db.students.countDocuments()
```



## Best Practices

- Use meaningful collection names.
- Store related data together.
- Avoid duplicate data whenever possible.
- Use MongoDB Atlas for production applications.
- Always validate user input.
- Keep backups of important data.
- Learn CRUD operations before using Mongoose.



## Common Interview Questions

### What is MongoDB?

MongoDB is a NoSQL document-oriented database that stores data in BSON documents instead of tables.



### What is the difference between SQL and MongoDB?

SQL stores data in tables with a fixed schema, while MongoDB stores data in flexible JSON-like documents.



### What is BSON?

BSON stands for Binary JSON. It is the internal format MongoDB uses to store documents.



### What is a Collection?

A collection is a group of related documents, similar to a table in SQL.



### What is ObjectId?

ObjectId is the unique identifier automatically generated for every MongoDB document.



### What does CRUD stand for?

- Create
- Read
- Update
- Delete



## Quick Revision

- MongoDB is a NoSQL database.
- Data is stored as BSON documents.
- Database → Collection → Document.
- Every document has a unique `_id`.
- MongoDB Atlas is the cloud version of MongoDB.
- MongoDB Compass is the GUI tool.
- CRUD operations are Create, Read, Update and Delete.
- `find()` retrieves documents.
- `insertOne()` inserts a document.
- `updateOne()` updates a document.
- `deleteOne()` deletes a document.
- MongoDB uses flexible schemas, making it suitable for modern web applications.