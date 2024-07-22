# Book-Search-SQL (Part 1)
Single search functionality used to locate a book within loaded library database.

### Project Description
Part I of the project involves design, development and implementation of the Database that could be used by
client-server application (to be utilized by librarians).

High level functionality to be developed and executed:
1. Load initial data files using SQL Developer Import utility. Load each file into its
own temporary table.
2. Create DB tables described in the high level schema. Write and execute SQL statements.
3. Write SQLs to Normalize and populate data into tables into normalized tables
4. Generate test data to simulate borrowing and fines transactions
5. Reports and Search SQL

### Data Sources
There are four files provided for the initial load.

Files:
- Books file: Books information, such as ISBN, authors, title, etc.
- Book copies file: number of copies of each book per library location
- Borrowers file: borrowers information, such as name, SSN (dummy), address, etc.
- Library branches file: branches address information

### Database and Tools 
- Database: Oracle Database 19c 
- ER Diagrams: MS Visio

### High Level Data Model
- The high level schema for this project is provided below. Not all attributes are listed. An ER
diagram will be created to match the high level design below.
![Screenshot (427)](https://github.com/user-attachments/assets/c5b8e8e9-7c90-40d7-8306-889fe6ed2e23)

## Functional Requirements 

### Design and DB Architecture 

The initial import of the dataset is considered to be an administration task and can be performed by utilizing
SQL Developer Import functionality while data normalization should be performed using SQL scripts.

Deliverables:
1. ER diagram
2. Database objects create statements: create table, foreign keys, indexes, etc.

### Data Load, Normalization, Data Generation

1. Load dataset files (provided with the project requirements) utilizing SQL Developer guided interface. 
2. Write SQL scripts to populate target application tables while normalizing the data loaded in #1.
3. Write SQL to generate (create/insert new records):
    1. Exactly 400 books check-outs for exactly 200 different borrowers and exactly 100 different books.
        Same borrower should not check out same book more than once
    2. Exactly 50 fines records for 50 different borrowers. Fines should be generated by books checked back
        in late.

### Book Search and Availability

Book search functionality should allow setting a specific library branch location context or performing it globally
for all locations.

Write SQL that will provide a single search functionality to locate a book given any combination of ISBN, title,
and/or Author(s). 

Search should display the following information for each book in the result set:
- ISBN
- Book title
- Book title
- All book author(s)
- Availability status at the currently selected branch (if branch is selected)

Deliverables: SQL statements, Screen Shots with output of the search for 3 search inputs.

### Reports 

Design and write SQL for 3 reports. The reports can accept input parameters, for example branch or date.
- Each report will have information presented from at least 3 tables
- Each report will have aggregation and accumulation functionality

Deliverables: SQL statement and Screen shot of results and SQL for each report
