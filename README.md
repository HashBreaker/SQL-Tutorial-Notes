# SQL-Tutorial-Notes
This repository includes SQL Tutorial &amp; Notes from freecodecamp YouTube video &amp; pdf notes.

## Team Members & Contributors

All the below mentioned are prominent element of this project and without them it wouldn't be possible.
SQL tutorial for beginners from freecodecamp YT.
# SQL 
### What is a Database (DB)?
 Any collection of related information
    1. Phone Book
    2. Shopping list
    3. Todo list
    4. Your 5 best friends 
    5. Facebook's user base, etc..
- Database can be stored in different ways
    1. On paper
    2. In your mind
    3. On a computer
    4. This Notion note on SQL itself
    5. Comment section
    
#  Database Management System (DBMS) : 
- A special software program that helps users to create and manage a database
    - makes its easy to manage large amount of information
    - handles security
    - backups
    - importing/exporting data
    - concurrency - In a database management system (DBMS), concurrency control manages simultaneous access to a database.
    - Interacts with software application
        - Programming languages

## CRUD

- CRUD (CREATE, READ/RETRIEVE, UPDATE, DELETE) is use to perform following functionalities - to create a database, read or retrieve informations from database, update the existing information database and delete the information in database.
- These are core 4 operations or functionalities in DBMS.

## Two Types of Databases

1. Relational databases (SQL)
    - Organize data into one or more tables
        - Each table has columns and rows
        - A unique key identifies each row

  2.  Non-Relational (no-SQL / not just SQL)

- Organize data in anything but a traditional table
    - Key-value stores
    - Documents(JSON, XML, etc.)
    - Graphs
    - Flexible table

## 1. Relational Databases (SQL)

- Relational Database Management System (RDBMS)
    - Example: MySQL, Oracle, PostgreSQL, MariaDB, etc.
- Structured Query Language
    - Standardized language for interacting with RDBMS
    - Used to perform 4 core operations i.e. CRUD operations, as well as other administrative tasks(user management, security, backups, etc.).
    - Used to define tables and structures
    - SQL code used on one RDBMS is not always portable to another without modification
- Example of Relational Database i.e. SQL  
    -  Below ID and Username is unique
##  ![Capture PNG](https://user-images.githubusercontent.com/67586773/141994086-b2728146-a2dc-45b9-899a-0091e4e9d1ab.png)

## 2. Non-Relational Databases (noSQL, not just SQL)

- Non-Relational Database management System (NRDBMS)
    - Helps users to create and maintain a non-relational database
        - Example: MongoDB, DynamoDB, Apache Cassandra, Firebase, etc.
- Implementation specific
    - Any non-relational databases falls under this category, so there is no set of language standard.
    - Most NRDBMS will implement their own language for performing CRUD and administrative operations on databases.
- Example of Non-Relational Databases (noSQL, not just SQL) -
![Capture2 PNG](https://user-images.githubusercontent.com/67586773/141994929-7d2d5825-b97a-4c48-a625-b6373d6926f7.png)

### Database Queries

- Queries are requests made to the database management system for specific information
- As database's structure become more and more complex, it becomes more difficult to get the specific pieces of information we want.
- A google search is a query

# Tables & Keys
![capture4 PNG](https://user-images.githubusercontent.com/67586773/142226373-9de485ff-6f1f-4931-956e-588713de1074.png)

All tables in Relational Databases we have 2 things Rows & Columns
 -  Row or horizontal entry represents individual entry i.e. row represents single student (in above example)  eg. 1(student id), Jack(student name), biology(major)
 -  Column or vertical entry represents single attribute  eg. major, name, student_id

# Primary Key
 - Whenever we are creating table in Relational Databases we always have 1 very special column which is called primary key.
 
 ![Capture5 PNG](https://user-images.githubusercontent.com/67586773/142227085-7f15c7f9-4910-4fbc-9378-e89e086bae68.png)
 
  - Primary key is a attribute which uniquely defines row in database.
  - Primary key will always unique for each rows in table even if all of attribute will same in row.
  - Primary key can be anything it can be a number or it can be string of text but it has uniquely identify the specific row.
  
 ### Types of Primary key 
 
  1. **Surrogate key** - Surrogate key is a key which has no mapping to anything in real world.
     - In below table just a random number assign to employee and that necessarily mean anything.
   
   ![Capture6 PNG](https://user-images.githubusercontent.com/67586773/142614438-7d3ab538-e6bf-450b-9d5f-734f690f81e7.png)

   2. **Natural Key** - Natural key is a key which has mapping to real world.
      - In below table emp_ssn ( social sequrity number is the number used in USA to identify each citizens uniquely)
      
   ![captur7 PNG](https://user-images.githubusercontent.com/67586773/142733871-452fe316-fce8-4975-aba9-deff0b362066.png)

   3. **Foreign Key** - Foreign key is an attribute in table that links us to another table in database. Or Foreign key is primary key of linked table.
      - In below table i.e. Employee table, branch_id is foreign key which linked with another table i.e. Branch table. And mgr_is also a foreign key.
      
   ![Capture8 PNG](https://user-images.githubusercontent.com/67586773/142733953-234dd158-8610-48ba-b4a4-73642ff809f2.png)

      - One table can have more than one foreign key.
      - In below table super_id (supervisor id) is also a foreign key that links employee table itself. (eg. Jan Levinson is supervisor of Michael Scott & Josh Porter)


 **Composite Key** - Composite key is a candidate key that consists of two or  more attributes(table columns) that together identify an entity occurrence(table row).
 - In below table, there are 2 primary keys (branch_id, supplier_name) and that are composite keys.
 - We need composite key because here, supplier_name or  branch_id doesn't uniquely identify row by itslef and they are repeating. Only together they can identify row.
 - Eg. Hammer Mill supply Paper to branch_id 2 & 3. Uni-ball supply Writing Utensils to branch_id 2 & 3.
 
 ![Capture11 PNG](https://user-images.githubusercontent.com/67586773/142803624-ddfdf5ce-dc26-4316-9231-86676ed27f60.png)
 
 - In below example, in Works_With table, both emp_id & client_id are composite key and also foreign key helps us to link relationship between Employee table and Client table.
 - Eg, emp_id 101 (i.e. Michael Scott) sold paper(suppose) to client_id 401 (i.e. Lackawana Country) in branch_id 2 (i.e. Scranton Branch) worth $2,67,000 .

![Capture12 PNG](https://user-images.githubusercontent.com/67586773/142803752-3de1e605-b90e-43a4-b7c6-3e7352fd9c80.png)
