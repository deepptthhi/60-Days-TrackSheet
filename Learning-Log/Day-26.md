# Day 26 - Learning MongoDB Fundamentals

## What did I learn?

Today I took my first step into databases by learning **MongoDB**, and it helped me understand where all the data in a backend application is actually stored. Until now, my Express applications could receive requests and send responses, but they couldn't permanently save any information. Learning MongoDB showed me how backend applications persist data even after the server restarts.

One of the biggest things I learned was the difference between **SQL and NoSQL databases**. I had heard these terms many times before, but today I finally understood why MongoDB stores data as flexible documents instead of tables and rows. Seeing data represented in JSON-like documents made it feel much more natural, especially since JavaScript also works with objects.

I also learned how MongoDB organizes data into **databases, collections, and documents**. Understanding this hierarchy made it much easier to visualize how information is stored inside a database.

Another interesting concept was **BSON** and the automatically generated **ObjectId**. I learned that although we work with JSON like data, MongoDB stores it internally as BSON and automatically gives every document a unique identifier.

Towards the end, I practiced basic **CRUD operations** using MongoDB commands. I learned how to create databases, insert documents, retrieve data, update existing records, and delete documents. It felt like I was finally interacting with a real database instead of just writing backend logic.

By the end of today's learning, I understood that a backend application isn't complete without a database, and MongoDB provides a simple yet powerful way to manage application data.

## What challenges did I face?

The biggest challenge today was understanding the relationship between **databases, collections, and documents**. Initially, they all seemed similar, but after comparing them with SQL tables and rows, the structure became much clearer.

I also found BSON slightly confusing because the data I wrote looked like JSON. After reading more about it, I realized that developers usually work with JSON-like syntax, while MongoDB stores everything internally as BSON for better performance and additional data type support.

Another small challenge was remembering the MongoDB shell commands. There were several commands like `insertOne()`, `find()`, `updateOne()`, and `deleteOne()`, and I had to practice them a few times before I became comfortable using them.

## What new concepts did I understand?

### MongoDB

I learned that MongoDB is a NoSQL database that stores data in flexible JSON like documents instead of tables.

### SQL vs NoSQL

I understood the differences between relational databases and document databases, and why MongoDB is often chosen for modern web applications.

### Database, Collection and Document

I learned how MongoDB organizes information using databases, collections, and documents, making it easier to store related data together.

### BSON

I understood that MongoDB stores documents internally as BSON, which extends JSON by supporting additional data types.

### ObjectId

I learned that every MongoDB document automatically receives a unique `_id` field, allowing each document to be uniquely identified.

### CRUD Operations

I practiced the four basic database operations:

- Create
- Read
- Update
- Delete

These operations form the foundation of almost every backend application.

## What computer/software engineering fundamentals did I learn today?

Today's learning helped me understand that databases are one of the core building blocks of software engineering. A backend application isn't useful if it cannot store and retrieve information reliably.

I also learned why choosing the right type of database matters. SQL databases provide structured relationships, while NoSQL databases like MongoDB offer flexibility when working with changing or unstructured data.

Another important realization was that CRUD operations are universal concepts. Regardless of the programming language or database technology, most applications perform these same four operations to manage data.

## What changed in my thinking?

Before today, I thought a database was simply a place where applications stored information.

After learning MongoDB, I realized that databases have their own structure, design principles, and ways of organizing data efficiently. Understanding how data is modeled is just as important as writing backend code.

The biggest realization for me was that building a backend isn't only about creating APIs it's also about designing how information is stored, managed, and retrieved efficiently. That completely changed the way I think about backend development.

## Today's One Line Summary

> **"Today I learned that a backend becomes truly useful when it can store and manage data, and MongoDB makes this possible through flexible document based storage and powerful CRUD operations."**