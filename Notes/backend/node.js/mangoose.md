

## What is Mongoose?

Mongoose is an **Object Data Modeling (ODM)** library for Node.js and MongoDB.

It provides a simple way to interact with MongoDB by allowing developers to define schemas, validate data, and perform database operations using JavaScript.

Instead of writing MongoDB queries directly, developers use Mongoose methods.



## Why Mongoose?

Mongoose is widely used because it provides:

- Schema-based data modeling
- Built-in validation
- Easy CRUD operations
- Better error handling
- Middleware support
- Easy integration with Express.js
- Cleaner and more maintainable code



## MongoDB vs Mongoose

| MongoDB | Mongoose |
|----------|-----------|
| Database | ODM Library |
| Stores data | Interacts with MongoDB |
| Uses BSON documents | Uses JavaScript objects |
| Can work without Mongoose | Requires MongoDB |

Think of it like this:

```
Node.js
   │
   ▼
Mongoose
   │
   ▼
MongoDB
```



## Installing Mongoose

Install Mongoose using npm.

```bash
npm install mongoose
```



## Importing Mongoose

CommonJS

```javascript
const mongoose = require("mongoose");
```

ES Modules

```javascript
import mongoose from "mongoose";
```



## Connecting to MongoDB

Local MongoDB

```javascript
const mongoose = require("mongoose");

mongoose.connect("mongodb://127.0.0.1:27017/CollegeDB")
.then(() => console.log("Database Connected"))
.catch(err => console.log(err));
```

MongoDB Atlas

```javascript
mongoose.connect(process.env.MONGO_URI)
.then(() => console.log("Connected"))
.catch(err => console.log(err));
```



## Environment Variables

Install dotenv

```bash
npm install dotenv
```

Create a `.env` file

```env
PORT=5000

MONGO_URI=your_mongodb_connection_string
```

Load environment variables

```javascript
require("dotenv").config();
```



## What is a Schema?

A Schema defines the structure of a MongoDB document.

It tells MongoDB:

- Which fields exist
- What data type they have
- Validation rules
- Default values

Example

```javascript
const mongoose = require("mongoose");

const studentSchema = new mongoose.Schema({

    name: String,

    age: Number,

    city: String

});
```

Think of a Schema as a blueprint for documents.



## Schema with Data Types

```javascript
const studentSchema = new mongoose.Schema({

    name: String,

    age: Number,

    email: String,

    isActive: Boolean,

    skills: [String],

    createdAt: Date

});
```

Common Data Types

| Data Type | Description |
|-----------|-------------|
| String | Text values |
| Number | Numeric values |
| Boolean | True or False |
| Date | Date and Time |
| Array | List of values |
| ObjectId | Reference to another document |
| Mixed | Any type of value |



## What is a Model?

A Model is created from a Schema.

It allows us to perform CRUD operations on the database.

```javascript
const Student = mongoose.model("Student", studentSchema);
```



## Schema vs Model

| Schema | Model |
|---------|-------|
| Defines document structure | Performs database operations |
| Blueprint | Working object |
| No database interaction | Directly interacts with MongoDB |


## Folder Structure

```
project/

config/
    db.js

models/
    Student.js

controllers/

routes/

server.js

.env
```

## Creating a Model

Student.js

```javascript
const mongoose = require("mongoose");

const studentSchema = new mongoose.Schema({

    name: String,

    age: Number,

    city: String

});

module.exports = mongoose.model("Student", studentSchema);
```


# CRUD Operations Using Mongoose

CRUD stands for:

| Operation | Mongoose Method |
|------------|-----------------|
| Create | create(), save() |
| Read | find(), findOne(), findById() |
| Update | updateOne(), findByIdAndUpdate() |
| Delete | deleteOne(), findByIdAndDelete() |



## Create a Document

Method 1

```javascript
const student = new Student({

    name: "Deepthi",

    age: 22,

    city: "Bangalore"

});

await student.save();
```



Method 2

```javascript
await Student.create({

    name: "Rahul",

    age: 21,

    city: "Mysore"

});
```



## Read All Documents

```javascript
const students = await Student.find();
```

Returns all documents inside the collection.


## Read One Document

```javascript
const student = await Student.findOne({

    name: "Deepthi"

});
```

Returns the first matching document.



## Find Document by ID

```javascript
const student = await Student.findById(id);
```

Searches using the MongoDB ObjectId.



## Find Using Conditions

```javascript
const students = await Student.find({

    age: 22

});
```

Returns all students whose age is 22.



## Find Multiple Conditions

```javascript
const students = await Student.find({

    age: 22,

    city: "Bangalore"

});
```

Returns documents matching both conditions.



## Query Operators

Greater Than

```javascript
Student.find({

    age: {

        $gt: 20

    }

});
```

Less Than

```javascript
Student.find({

    age: {

        $lt: 25

    }

});
```

Greater Than or Equal

```javascript
Student.find({

    age: {

        $gte: 22

    }

});
```

Less Than or Equal

```javascript
Student.find({

    age: {

        $lte: 22

    }

});
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
Student.find({

    age: {

        $gt: 20

    },

    city: "Bangalore"

});
```

OR

```javascript
Student.find({

    $or: [

        {

            city: "Bangalore"

        },

        {

            age: 25

        }

    ]

});
```

## Update One Document

```javascript
await Student.updateOne(

    {
        name: "Deepthi"
    },

    {
        $set: {
            age: 23
        }
    }

);
```

Updates the first matching document.

---

## Update Multiple Documents

```javascript
await Student.updateMany(

    {
        city: "Bangalore"
    },

    {
        $set: {
            city: "Bengaluru"
        }
    }

);
```

Updates all matching documents.



## Find By Id And Update

```javascript
await Student.findByIdAndUpdate(

    id,

    {
        age: 24
    },

    {
        new: true
    }

);
```

The `new: true` option returns the updated document.



## Delete One Document

```javascript
await Student.deleteOne({

    name: "Rahul"

});
```

Deletes the first matching document.



## Delete Multiple Documents

```javascript
await Student.deleteMany({

    city: "Mysore"

});
```

Deletes all matching documents.



## Find By Id And Delete

```javascript
await Student.findByIdAndDelete(id);
```

Deletes a document using its ObjectId.


## Query Methods

Find All

```javascript
Student.find();
```

Find One

```javascript
Student.findOne();
```

Find By ID

```javascript
Student.findById(id);
```

Count Documents

```javascript
Student.countDocuments();
```

Sort

```javascript
Student.find().sort({

    age: 1

});
```

Descending Order

```javascript
Student.find().sort({

    age: -1

});
```

Limit Results

```javascript
Student.find().limit(5);
```

Skip Results

```javascript
Student.find().skip(5);
```



## Validation

Mongoose allows validation before saving data into MongoDB.

Example

```javascript
const studentSchema = new mongoose.Schema({

    name:{

        type:String,

        required:true

    },

    age:{

        type:Number,

        required:true

    }

});
```

If a required field is missing, Mongoose throws an error.



## Validation Rules

Required

```javascript
required: true
```

Minimum Length

```javascript
minlength: 6
```

Maximum Length

```javascript
maxlength: 30
```

Minimum Number

```javascript
min: 18
```

Maximum Number

```javascript
max: 60
```

Unique Value

```javascript
unique: true
```



## Default Values

Default values are automatically assigned when no value is provided.

```javascript
isActive:{

    type:Boolean,

    default:true

}
```



## Enum Validation

Restricts a field to predefined values.

```javascript
role:{

    type:String,

    enum:["Student","Teacher","Admin"]

}
```

Only these values are allowed.



## Timestamps

```javascript
const studentSchema = new mongoose.Schema(

{

    name:String

},

{

    timestamps:true

}

);
```

Automatically creates:

- createdAt
- updatedAt



## Error Handling

Always use `try...catch` while performing database operations.

```javascript
try{

    const student = await Student.create(req.body);

    res.status(201).json(student);

}

catch(err){

    res.status(500).json({

        message: err.message

    });

}
```



## Database Connection File

Create a separate file for the database connection.

config/db.js

```javascript
const mongoose = require("mongoose");

const connectDB = async () => {

    try{

        await mongoose.connect(process.env.MONGO_URI);

        console.log("MongoDB Connected");

    }

    catch(err){

        console.log(err);

        process.exit(1);

    }

};

module.exports = connectDB;
```

server.js

```javascript
require("dotenv").config();

const connectDB = require("./config/db");

connectDB();
```



## MVC Folder Structure

```
project/

config/
    db.js

models/
    Student.js

controllers/
    studentController.js

routes/
    studentRoutes.js

server.js

.env
```



## Best Practices

- Create separate models for each collection.
- Always validate user input.
- Store the MongoDB connection string in the `.env` file.
- Use `try...catch` for database operations.
- Keep database logic inside controllers.
- Use meaningful collection names.
- Avoid duplicate data.
- Use async/await instead of callbacks.



## Common Interview Questions

### What is Mongoose?

Mongoose is an ODM library that helps Node.js applications interact with MongoDB.



### What is ODM?

ODM (Object Data Modeling) maps JavaScript objects to MongoDB documents.



### Difference between MongoDB and Mongoose?

MongoDB is the database.

Mongoose is a library used to interact with MongoDB.



### What is a Schema?

A Schema defines the structure and validation rules of a MongoDB document.



### What is a Model?

A Model is created from a Schema and is used to perform CRUD operations.



### Difference between Schema and Model?

Schema defines the structure of data.

Model performs database operations.



### Difference between `create()` and `save()`?

`create()` creates and saves a document in one step.

`save()` first creates a document object and then saves it.



### What does `new: true` do?

It returns the updated document after an update operation instead of the old document.



### Why use timestamps?

They automatically maintain the `createdAt` and `updatedAt` fields.



## Quick Revision

- Mongoose is an ODM library for MongoDB.
- It simplifies database operations in Node.js.
- A Schema defines the structure of documents.
- A Model performs CRUD operations.
- `create()` and `save()` insert documents.
- `find()`, `findOne()`, and `findById()` retrieve documents.
- `updateOne()` and `findByIdAndUpdate()` update documents.
- `deleteOne()` and `findByIdAndDelete()` remove documents.
- Validation ensures only valid data is stored.
- `timestamps: true` automatically creates `createdAt` and `updatedAt`.
- Store database credentials in the `.env` file.
- Always use `try...catch` while working with the database.