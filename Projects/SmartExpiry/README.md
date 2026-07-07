# SmartExpiry

> Never forget expiry dates again.

A smart inventory management application that helps users track expiry dates for medicines, groceries, cosmetics, important documents, warranties, and more.

Instead of manually remembering expiry dates, SmartExpiry keeps everything organized in one place and alerts users before items expire.


## Table of Contents

- About
- Problem Statement
- Solution
- Features
- Screenshots
- Project Workflow
- System Design
- Folder Structure
- Technologies Used
- OOP Concepts Used
- Installation
- Usage
- Future Scope
- Challenges Faced
- What I Learned
- Contributing
- License



# About

SmartExpiry is a Python-based inventory management application that helps users keep track of items that expire over time.

The project was built to solve a common real-world problem forgetting expiry dates.

Users can organize items into categories, monitor expiry dates, receive alerts, and view statistics from a single dashboard.



# Problem Statement

Many people forget expiry dates.

Examples include:

- Medicines
- Milk
- Vegetables
- Cosmetics
- Passport
- Driving License
- Insurance
- Warranty Cards

This often leads to

- Food waste
- Financial loss
- Health risks
- Missed renewals

Keeping all these dates in different places becomes difficult.


# 💡 Solution

SmartExpiry keeps everything in one place.

The application allows users to

- Add items
- Edit items
- Delete items
- Search items
- Track expiry dates
- Get reminders
- View statistics

This makes expiry management simple and organized.

# ✨ Features

## User Features

- Register
- Login
- Profile Management


## Inventory

- Add Item
- Update Item
- Delete Item
- Search Item
- Filter Items


## Categories

- Medicines
- Groceries
- Cosmetics
- Electronics
- Documents
- Kitchen
- Others


## Dashboard

Shows

- Total Items
- Expired Items
- Expiring Today
- Expiring This Week
- Safe Items


## Notifications

Example

- Milk expires tomorrow

- Passport expires in 15 days

- Crocin expired yesterday


## Statistics

- Total Inventory
- Category Wise Count
- Monthly Added Items
- Expired Percentage

## Export

- CSV
- PDF


# Project Workflow

User

↓

Login

↓

Dashboard

↓

Add Item

↓

Store in Database

↓

Track Expiry

↓

Generate Notifications

↓

Display Dashboard


# OOP Concepts Used

## Classes

- User
- Inventory
- Item
- Medicine
- Food
- Document
- Dashboard
- Notification


## Inheritance

Item

↓

Medicine

↓

Food

↓

Document

## Polymorphism

display_details()

Every item displays its information differently.


## Encapsulation

Sensitive data is accessed using methods instead of directly modifying variables.


## Composition

Inventory contains multiple Items.

Dashboard contains Inventory.


#  Folder Structure

SmartExpiry/

├── main.py

├── models/

│ ├── user.py

│ ├── item.py

│ ├── medicine.py

│ ├── food.py

│ ├── document.py

│

├── services/

│ ├── notification.py

│ ├── dashboard.py

│ ├── inventory.py

│

├── data/

│ └── inventory.json

│

├── utils/

│ ├── helper.py

│ └── validator.py

│

├── README.md


# Technologies Used

- Python
- OOP
- JSON
- Datetime Module
- OS Module
- File Handling


# Getting Started

## Clone Repository

git clone ...

## Move to Project

cd SmartExpiry

## Run

python main.py


# 📸 Screenshots

(Add screenshots here)

Dashboard

Inventory

Notifications

Statistics



# Future Improvements

- Email Notifications
- SMS Notifications
- Barcode Scanner
- QR Scanner
- OCR
- AI Expiry Prediction
- Mobile App
- Cloud Sync
- Multi-user Support


# Challenges Faced

- Designing the class hierarchy
- Handling expiry dates correctly
- Keeping the code modular
- Preventing duplicate entries


# What I Learned

While building this project I learned

- Python OOP
- Inheritance
- Polymorphism
- Encapsulation
- Composition
- File Handling
- JSON
- Date & Time
- Error Handling
- Project Structure
- Git & GitHub

# Contributing

Contributions are welcome.

Feel free to fork the repository and submit a pull request.


# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.