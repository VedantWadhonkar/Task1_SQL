# Task1_SQL
# 📚 Library Management Database (SQL Project)

This project is a simple **Library Management System** implemented in SQL.  
It demonstrates how to create and manage relationships between **Authors, Publishers, and Books**.

---

## 🗂 Database Details

- **Database Name:** `LibraryDB`  

### Tables
1. **Author**  
   - `AuthorID` (Primary Key)  
   - `Author_Name`  

2. **Publisher**  
   - `PublisherID` (Primary Key)  
   - `Publisher_Name`  

3. **Book**  
   - `BookID` (Primary Key)  
   - `Title`  
   - `AuthorID` (Foreign Key → Author.AuthorID)  
   - `PublisherID` (Foreign Key → Publisher.PublisherID)  

---

## 📥 Sample Data Inserted
- **Authors**:  
  - J.K. Rowling  
  - George Orwell  

- **Publishers**:  
  - Bloomsbury  
  - Secker & Warburg  

- **Books**:  
  - *Harry Potter and the Philosopher’s Stone* (Author: J.K. Rowling, Publisher: Bloomsbury)  
  - *1984* (Author: George Orwell, Publisher: Secker & Warburg)  

---

## 🔍 Example Query
To fetch all book details along with author and publisher names:

```sql
SELECT b.BookID, b.Title, a.Author_Name, p.Publisher_Name
FROM Book b
JOIN Author a ON b.AuthorID = a.AuthorID
JOIN Publisher p ON b.PublisherID = p.PublisherID;

