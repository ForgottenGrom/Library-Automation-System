# Library Automation System

A database project for library automation, developed as a university course project.

##  Description
The system is built on **PostgreSQL** and covers the full cycle of library management processes: from tracking books and authors to automated issuing, returning, and calculating overdue fines.

##  Key Features
* **Automation:** Database triggers automatically update book statuses (available/on loan) and calculate overdue fines.
* **Analytics:** Pre-configured `VIEW`s provide quick insights into active loans and current book availability.
* **Functionality:** Includes a convenient search function for finding books by title or author, as well as stored procedures for safely issuing book instances.

##  Tech Stack
* **DBMS:** PostgreSQL
* **Language:** SQL (PL/pgSQL)

##  How to Use
1. Create a new database in your PostgreSQL server:
   ```sql
   CREATE DATABASE library_db;
   ```
2. Execute the library.sql script using pgAdmin, DBeaver, or the psql command line tool.
##  Query Examples
Search for a book:
```sql
   SELECT * FROM search_books('Кобзар');
```
Issue a book (Instance ID, Reader ID, duration in days):
```sql
   CALL issue_book(1, 1, 14);
```
Developed as an educational project.



