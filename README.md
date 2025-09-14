# 📚** LIBRARY  DATABASE SYSTEM** 

This project is a **MySQL relational database** for managing a **secondary school library**.  
It was designed to handle **students, books, borrowings, services, and penalties**, following the real needs of a school library.

---

## 📌 Project Overview

A library must be able to:  
- Register and manage members (students).  
- Keep track of books and their availability.  
- Allow borrowing and returning of books.  
- Enforce rules such as **borrowing duration, renewals, and fines**.  
- Provide additional **services beyond book borrowing**.  

This database project implements all these features in SQL.

---

## 🚀 Features

### 👥 Members
- Each student has:
  - `member_id` (Primary Key, Auto Increment)  
  - `name` (Full name)  
  - `email` (Unique, cannot be duplicated)  
  - `phone` (Optional contact)  

👉 Example: 15 members have been added.

---

### 📚 Books
- Each book has:
  - `book_id` (Primary Key, Auto Increment)  
  - `title` (Book title)  
  - `author` (Book author)  
  - `isbn` (Unique, prevents duplicates)  
  - `available_copies` (default = 1)  

👉 Example: Books from **secondary school syllabus** are included (Math, English, Kiswahili, Science, History, CRE, etc.).

---

### 🔄 Borrowings
- Each borrowing record tracks:
  - `borrowing_id` (Primary Key, Auto Increment)  
  - `member_id` (Foreign Key → members)  
  - `book_id` (Foreign Key → books)  
  - `borrow_date` (Default = current date)  
  - `return_date` (NULL until returned)  

#### Rules:
- Minimum borrowing period = **7 days (1 week)**.  
- Maximum renewals = **2 times per book**.  
- Late returns incur a fine of **30 KES per book**.  

👉 Example: 3 members each borrowed 3 different syllabus books.

---

### 🏛️ Services
Apart from borrowing, the library provides extra services:  

1. ✅ **Free Services**
   - Free use of library space for reading.  
   - Free access for more than a week.  
   - Free **basic research support** for students.  

2. 💰 **Paid Services**
   - Advanced/Deep Research → **KES 200 per 2 hours**.  

---

## 🛠️ Tools & Technologies

- **MySQL** → Database engine.  
- **VS Code** → SQL script editing.  
- **Git & GitHub** → Version control and hosting.  
- **Bash / Git Bash** → Running commands.  

---

## 📊 Example Data

- **15 members** registered.  
- **Multiple syllabus books** added (Math, English, Kiswahili, Physics, Chemistry, Biology, Geography, History, etc.).  
- **3 members borrowed 3 different books** each (one per subject).  

---

## ⚡ Installation & Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/DEV-Bradly/library_db-.git
   cd library_db-
## Open MySQL and create the database:

CREATE DATABASE library_db;
USE library_db;

## import the SQL file
SOURCE library_db.sql;

## confirm  tables
SHOW TABLES;


📈 ***  Future Improvements ***

Add Librarian/Admin accounts for management.

Add reports (most borrowed books, fines collected, overdue reports).

Add student performance integration (link borrowed books to subjects).

Connect with a web app or mobile app for real-time borrowing.

👨‍💻 Author

Name: DEV-Bradly (Kip Tech)

Location: Kenya

Project: Secondary School Library Database

📜 License

This project is free to use for learning and school projects.
You may modify and expand it to fit your own school library needs.
