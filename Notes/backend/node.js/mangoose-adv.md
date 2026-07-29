

## What is Relationships in MongoDB?

Unlike SQL databases, MongoDB does **not use JOINs** to connect tables.
Instead, documents are related using **ObjectIds**.

Mongoose makes handling these relationships simple through the
**populate()** method.

Example

``` text
Student
---------
_id
name
department

Course
---------
_id
courseName
studentId ---> Student ObjectId
```

Here, `studentId` stores the ObjectId of the Student document instead of
storing the complete student information.



# Why Relationships?

Relationships help us:

-   Avoid duplicate data
-   Keep databases normalized
-   Easily fetch related documents
-   Reduce storage usage
-   Improve maintainability

Example:

Instead of storing customer information in every order,

``` text
Order
Customer Name
Customer Email
Customer Phone
```

Store only:

``` text
customerId
```

Later, Mongoose can retrieve the complete customer document using
`populate()`.



# Types of Relationships

## 1. One-to-One

One user has one profile.

``` text
User
{
  _id:1,
  name:"Deepthi"
}

Profile
{
  userId:1,
  bio:"Backend Developer"
}
```

## 2. One-to-Many

One author writes many books.

``` text
Author
{
  _id:10,
  name:"John"
}

Books
{
  title:"Node.js",
  author:10
}

{
  title:"MongoDB",
  author:10
}
```

## 3. Many-to-Many

Students enroll in multiple courses.

``` text
Student
courses:[
 ObjectId(),
 ObjectId()
]

Course
students:[
 ObjectId(),
 ObjectId()
]
```


# Embedding vs Referencing

## Embedding

Stores related data inside another document.

``` javascript
const user = {
  name: "Deepthi",
  address: {
    city: "Bangalore",
    state: "Karnataka"
  }
}
```

### Advantages

-   Faster reads
-   Simple queries
-   Less database calls

### Disadvantages

-   Data duplication
-   Harder to update large datasets


## Referencing

Stores only ObjectIds.

``` javascript
const order = {
  customer: ObjectId("65af...")
}
```

### Advantages

-   No duplication
-   Better scalability
-   Easier maintenance

### Disadvantages

-   Extra query required
-   Uses `populate()`

  Embedding             Referencing
  --------------------- ----------------------
  Stores full data      Stores ObjectId
  Faster reads          Better normalization
  More duplication      Less duplication
  Best for small data   Best for large data



# What is populate()?

`populate()` automatically replaces an ObjectId with the actual
referenced document.

Without populate:

``` text
{
  customer:"65afbc238fd..."
}
```

After populate:

``` text
{
  customer:{
    name:"Deepthi",
    email:"abc@gmail.com"
  }
}
```

# Creating Relationships

## User Schema

``` javascript
const mongoose = require("mongoose");

const userSchema = new mongoose.Schema({
  name: String,
  email: String
});

module.exports = mongoose.model("User", userSchema);
```

## Post Schema

``` javascript
const mongoose = require("mongoose");

const postSchema = new mongoose.Schema({
  title: String,
  content: String,
  author: {
    type: mongoose.Schema.Types.ObjectId,
    ref: "User"
  }
});

module.exports = mongoose.model("Post", postSchema);
```



# Inserting Related Data

``` javascript
const user = await User.create({
  name: "Deepthi",
  email: "abc@gmail.com"
});

await Post.create({
  title: "Learning Node",
  content: "Today's topic",
  author: user._id
});
```


# Using populate()

``` javascript
const posts = await Post.find().populate("author");
```

Retrieve selected fields:

``` javascript
.populate("author", "name email")
```

Populate multiple fields:

``` javascript
Post.find()
.populate("author")
.populate("comments");
```

Nested populate:

``` javascript
Post.find().populate({
  path:"comments",
  populate:{
    path:"user"
  }
});
```


# Virtual Populate

``` javascript
userSchema.virtual("posts",{
  ref:"Post",
  localField:"_id",
  foreignField:"author"
});
```

Benefits:

-   Cleaner database
-   Less duplication
-   Automatic relationship



# Common Errors

## Missing `ref`

Wrong

``` javascript
author: mongoose.Schema.Types.ObjectId
```

Correct

``` javascript
author:{
  type: mongoose.Schema.Types.ObjectId,
  ref:"User"
}
```



## Wrong populate field

Wrong

``` javascript
.populate("users")
```

Correct

``` javascript
.populate("author")
```


## Validate ObjectId

``` javascript
mongoose.Types.ObjectId.isValid(id)
```



# Best Practices

-   Prefer referencing for large datasets.
-   Embed only small related data.
-   Populate only required fields.
-   Avoid deep nested populates.
-   Validate ObjectIds.
-   Use indexes on referenced fields.



# Common Interview Questions

## What is populate()?

It replaces referenced ObjectIds with complete documents.

## Why do we use `ref`?

It tells Mongoose which model should be populated.

## Difference between Embedding and Referencing?

Embedding stores complete data inside the document.

Referencing stores ObjectIds and retrieves related data using
`populate()`.

## Can MongoDB perform JOINs?

Not directly. MongoDB uses `$lookup`, while Mongoose provides
`populate()`.



# Quick Revision

-   MongoDB uses ObjectIds for relationships.
-   `populate()` fetches related documents.
-   `ref` specifies the referenced model.
-   Three relationship types: One-to-One, One-to-Many, Many-to-Many.
-   Embedding stores complete data.
-   Referencing stores ObjectIds.
-   Virtual Populate creates relationships without storing ObjectIds.

