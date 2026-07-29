# Day 28 - Learning Advanced Mongoose Relationships & Population

## What did I learn?

Today I learned how Mongoose helps connect different collections in MongoDB using relationships. Until now, I had only worked with individual collections and performed CRUD operations on them. Today I understood how real-world backend applications connect related data instead of storing everything in a single collection.

One of the biggest things I learned was the difference between **embedding** and **referencing**. At first, I thought storing all related information inside one document was always the easiest approach. But after learning both methods, I realized that embedding is useful for small data that is always accessed together, while referencing is better when data is large, shared across multiple documents, or changes frequently.

I also learned about the different types of relationships that can exist in MongoDB, such as **one-to-one**, **one-to-many**, and **many-to-many**. Understanding these relationships helped me see how applications like e-commerce websites, social media platforms, and blogging applications organize their data efficiently.

Another concept that I found really interesting was **populate()**. Before today, I thought I would need to manually write multiple queries to retrieve related information. After learning populate(), I understood that Mongoose can automatically replace an ObjectId with the complete referenced document, making the code much cleaner and easier to read.

I also explored **Virtual Populate**, which allows related data to be fetched without storing arrays of ObjectIds inside the document. It showed me another way to create relationships while keeping the database organized and avoiding unnecessary duplication.

By the end of today's learning, I realized that designing relationships is an important part of backend development. A well-designed database not only keeps data organized but also makes applications easier to maintain, faster to develop, and more scalable as they grow.


## What challenges did I face?

The biggest challenge today was understanding when to use **embedding** and when to use **referencing**. Initially, both approaches looked very similar, so it was difficult to decide which one would be the better choice. After going through a few examples, I understood that the decision depends on how the data is used and how often it changes.

Another challenge was understanding how **populate()** works. At first, I expected it to behave exactly like SQL joins, but I learned that Mongoose handles the process differently by fetching the referenced documents and combining them automatically.

I also found **Virtual Populate** a little confusing in the beginning because the relationship exists without storing ObjectIds directly inside the document. After practicing with examples, the concept became much easier to understand.



## What new concepts did I understand?

### Relationships

I learned how MongoDB connects documents using **ObjectIds** instead of traditional SQL joins.

### Embedding vs Referencing

I understood when to store related data inside the same document and when to store only a reference to another document.

### Relationship Types

I learned how one-to-one, one-to-many, and many-to-many relationships are implemented in MongoDB.

### populate()

I learned that `populate()` automatically replaces ObjectIds with the complete referenced documents, making it much easier to retrieve related information.

### Virtual Populate

I understood how Virtual Populate creates relationships dynamically without storing arrays of ObjectIds inside the database.

### ObjectId Validation

I learned why validating ObjectIds before querying the database helps prevent runtime errors.



## What computer/software engineering fundamentals did I learn today?

Today's learning helped me understand that backend development is not only about creating APIs but also about designing databases properly.

I learned that choosing the right relationship strategy helps reduce duplicate data, improves maintainability, and allows applications to scale more efficiently. I also realized that good database design makes backend applications cleaner, easier to understand, and simpler to maintain as they become larger.



## What changed in my thinking?

Before today, I thought storing all related information inside a single document was always the easiest solution.

After learning about relationships in MongoDB, I realized that storing too much data together can lead to duplication and make applications harder to maintain. I now understand why developers carefully choose between embedding and referencing depending on the application's requirements.

The biggest realization for me today was that designing relationships is just as important as writing backend code. The way data is connected plays a huge role in building scalable and well-structured applications.



## Today's One Line Summary

> **"Today I learned how Mongoose uses relationships and populate() to connect different collections, helping build cleaner, more organized, and scalable backend applications."**