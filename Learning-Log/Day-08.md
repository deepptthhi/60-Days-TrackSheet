# Day 8 – Completing SmartExpiry 

## What did I learn?

Today was a really satisfying day because I completed **SmartExpiry**, my first Python Object Oriented Programming (OOP) project.

Yesterday, I started building the project after learning the basics of OOP. Today, I focused on completing the remaining features, improving the code, testing everything, and preparing the project for GitHub.

SmartExpiry is a command line application that helps users keep track of the expiry dates of medicines, groceries, and important documents. It allows users to add, view, search, update, and delete items, while also checking whether an item has expired or is about to expire. The data is stored in a JSON file, so the inventory remains saved even after closing the application.

Once the application was working, I spent time making the project cleaner and more presentable. I improved the folder structure, added input validation, updated the README, added screenshots, created a `.gitignore` file, included an MIT License, and organized my Git commits properly.

Completing the project felt rewarding because it wasn't just another practice program, it was my first complete software project from planning to deployment on GitHub.


## What challenges did I face?

Although the project looks simple now, I faced quite a few challenges while building it.

The biggest challenge was understanding how different classes should interact with each other. Initially, I wasn't sure what should belong inside the `Item` class and what should be kept inside the individual classes like `Medicine`, `Grocery`, and `Document`.

Saving objects into a JSON file was another challenge. Since Python objects can't be stored directly, I had to understand how to convert them into dictionaries before saving and recreate them when loading the data.

I also spent time fixing import errors, organizing the project into multiple folders, and making sure everything worked together correctly.

Another challenge was handling invalid user input. At first, the application would crash if someone entered the wrong data type. Adding proper input validation using `try` and `except` made the application much more reliable.

Finally, writing a good README was harder than I expected. It took a few revisions before I was happy with the structure and the way I explained the project.


## How does this project solve a real world problem?

The idea behind SmartExpiry came from something I've noticed at home.

Sometimes medicines stay in the cupboard long after they've expired. Groceries are forgotten in the refrigerator, and important documents like passports or insurance papers have renewal dates that are easy to miss.

Instead of keeping track of all these dates manually, SmartExpiry stores everything in one place.

Users can quickly check what they have, identify items that have already expired, and see which ones will expire soon. Even though the current version is a simple command line application, it demonstrates how software can help organize everyday tasks.

I can also see how this idea could grow into a larger application with email reminders, barcode scanning, cloud storage, and a web or mobile interface.


## What new concepts did I understand?

### Applying OOP in a Real Project

Today's biggest learning wasn't a new Python topic it was understanding how OOP is actually used while building software.

Instead of practicing classes in isolation, I created different classes for different item types and connected them using inheritance. This made the code easier to organize and reduced duplication.

I finally understood why OOP is useful in real applications.

### Working with JSON

I learned how to save and load application data using JSON.

Every time an item is added, updated, or deleted, the changes are written to a JSON file. When the application starts again, it loads the saved data automatically.

This made the application feel much closer to something people could actually use.

### Building a Complete CLI Application

Before this project, most of my programs solved only one problem.

Today I completed a menu driven application where multiple features work together.

I also added input validation so that invalid entries don't immediately crash the application, making it more user friendly.


## What computer/software engineering fundamentals did I learn today?

One thing I realized today is that writing code is only one part of software development.

A complete project also needs:

- A clean folder structure
- Meaningful Git commits
- Proper documentation
- A good README
- Screenshots
- A `.gitignore` file
- A License
- Clean and readable code

These things may seem small individually, but together they make a project much more professional and easier for others to understand.

I also learned the importance of testing every feature before considering a project complete.


## What changed in my thinking?

Completing SmartExpiry gave me a lot more confidence.

Just a couple of days ago, Object Oriented Programming felt confusing. Today, I've built a complete application using those same concepts.

I also realized that the best way for me to learn programming is by building projects. Every bug I fixed and every design decision I made taught me something new.

More importantly, I learned that software development isn't only about writing code it's also about planning, organizing, testing, documenting, and continuously improving the project.

Finishing this project showed me that I can take an idea, break it into smaller tasks, and gradually turn it into a working application.


## Today's One-Line Summary

> "Today I completed SmartExpiry, my first Python OOP project. Along the way, I learned that building software is not just about writing code, but about solving real problems, improving the user experience, and creating something that others can understand and use."