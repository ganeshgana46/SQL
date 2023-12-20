# DBMS (Database Management System)

Database Management Systems (DBMS) are software systems used to store, retrieve and run queries on data.

A Database Management System (DBMS) is a software system that is designed to manage and organize data in a structured manner. 
It allows users to create, modify, and query a database, as well as manage the security and access controls for that database.

DBMS can be classified into two types: 
1.Relational Database Management System (RDBMS)
2.Non-Relational Database Management System (NoSQL or Non-SQL)

RDBMS:
     Data is organized in the form of tables and each table has a set of rows and columns. The data are related to each other through primary and foreign keys.
NoSQL: 
     Data is organized in the form of key-value pairs, documents, graphs, or column-based. These are designed to handle large-scale, high-performance scenarios.

Database Languages
Data Definition Language
Data Manipulation Language
Data Control Language
Transactional Control Language


Data Definition Language:
           DDL is the short name for Data Definition Language, which deals with database schemas and descriptions, of how the data should reside in the database.

> CREATE: to create a database and its objects like (table, index, views, store procedure, function, and triggers)
> ALTER: alters the structure of the existing database
> DROP: delete objects from the database
> TRUNCATE: remove all records from a table, including all spaces allocated for the records are removed
> COMMENT: add comments to the data dictionary
> RENAME: rename an object

Data Manipulation Language:
           DML is the short name for Data Manipulation Language which deals with data manipulation and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is used to store, modify, retrieve, delete and update data in a database.

> SELECT: retrieve data from a database
> INSERT: insert data into a table
> UPDATE: updates existing data within a table
> DELETE: Delete all records from a database table
> MERGE: UPSERT operation (insert or update)
> CALL: call a PL/SQL or Java subprogram
> EXPLAIN PLAN: interpretation of the data access path
> LOCK TABLE: concurrency Control

Data Control Language:
          DCL is short for Data Control Language which acts as an access specifier to the database.(basically to grant and revoke permissions to users in the database

> GRANT: grant permissions to the user for running DML(SELECT, INSERT, DELETE,…) commands on the table
> REVOKE: revoke permissions to the user for running DML(SELECT, INSERT, DELETE,…) command on the specified table

Transactional Control Language:
          TCL is short for Transactional Control Language which acts as an manager for all types of transactional data and all transactions.Some of the command of TCL are

> Roll Back: Used to cancel  or Undo changes made in the database 
> Commit: It is used to apply or save changes in the database
> Save Point: It is used to save the data on the temporary basis in the database

#Overview

> Quick Introduction of SQL
> Create a Database and Table
> Insert
> Select Data
> Where Clauses
> Update Data
> Delete
> Change Table (new column, update column)
> Create a primary key
> Create an index
> Create Foreign Keys
> Joins and Relationships
> Functions
> Group By


#Tools to write SQL

> SQL server management studio (SSMS)
> SQL Developer
> SQL Workbench
> TOAD

#SQL

     SQL is a standard language for storing, manipulating and retrieving data in databases.
     
     Our SQL tutorial will teach you how to use SQL in: MySQL, SQL Server, MS Access, Oracle, Sybase, Informix, Postgres, and other database systems.

     SQL:
     
     > SQL is Language to manage databases.
     > SQL is used to query Databases.
     > SQL does not provide connections
     > SQL codes are used in oracle, SQL server, PostgreSQL, DB2, MySQL etc.

     MYSQL:

     > MySQL is databases Software.
     > MySQL stores the data.
     > It provides an integrated tool called MySQL Workbench.
     > MySQL uses SQL for data Management.

# Session - 1
> What is DBMS and RDBMS and non-RDBMS ?
> What is Database ? ---> Data Storage area
> What is SQL ?
      SQL (Structure Query Language) --> used to communicate to the database to perform different kinds of operations.
> Database Components - Client & Server
     Server :
        Data is actually stored in the Database server (Remote machines)
     Client :
        We can send SQL Commands using client software
      
# Session - 2

1) Create database
2) Created Table Student
3) Inserted data into student table
4) Select / Retrieve the data from a table
5) Where (Filtering records based on condition)
6) Distict (Displays unique records or removing duplicates)
7) AND, OR and NOT
8) BETWEEN, NOT BETWEEN
9) Pattern Matching (Wild Card Characters)

>> What is Database and schema ?
>> Database Languages
  1.DDL (Data Definition Language)
  2.DML (Data Manipulation Language)
  3.DRL/DQL (Data Retrieval Language / Data Query Language)
  4.TCL (Transaction Control Language)
  5.DCL (Data Control Language)

- DDL (Data Definition Language):
    CREATE, ALTER, DROP, TRUNCATE, RENAME
- DML (Data Manipulation Language):
    INSERT, UPDATE, DELETE
- DRL/DQL (Data Retrieval Language / Data Query Language):
    SELECT
- TCL (Transaction Control Language):
    COMMIT, ROLLBACK, SAVE POINT
- DCL (Data Control Language):
    GRANT, REVOKE

>> Craete Database / Schema
> Note : Both Database and Schema

  - CREATE DATABASE mybd; ---> command used to create database
  - DROP DATABASE mybd;   ---> command used to delete database

  - CREATE SCHEMA mydb;   ---> command used to create database
  - DROP SCHEMA mybd;     ---> command used to delete database

  - CRAETE DATABASE IF NOT EXISTS mydb;

>> Create Table
>  create table <<TABLE NAME>> (col1 datatype,col2 datatype, col3 datatype...);

Example:
- USE mydb;
- CREATE TABLE STUDENTS(SNO INT(5), SNAME VARCHAR(15), MARKS INT(3));

>> Inserting data into table
>  INSERT INTO <<TABLE NAME>> VALUES(VAL1,VAL2,VAL3...);

Example:
- USE mydb;
- INSERT INTO STUDENTS VALUES (101,"KIRAN",80);
- INSERT INTO STUDENTS (SNAME,SNO,MARKS) VALUES("RAM",102,60);
- INSERT INTO STUDENTS VALUES (103,"KRISHNA",NULL);

>> Selecting Rows from a table
- USE hr;
- SELECT * FROM EMPLOYEES;
- SELECT EMPLOYEE_ID, FIRST_NAME, SALARY FROM EMPLOYEES;
- SELECT EMPLOYEE_ID EMPID, FIRST_NAME, SALARY+5000 SAL FROM EMPLOYEES;

>> SQL Data Types :
- https://www.w3schools.com/mysql/mysql_datatypes.asp

>> Where Clause

- Used for selecting the rows based on condition. (Filtering the rows using where condition)
- USE hr;
- SELECT * FROM EMPLOYEES;
- SELECT * FROM EMPLOYEES WHERE SALARY>3000;
- SELECT * FROM EMPLOYEES WHERE SALARY<=3000
- SELECT * FROM EMPLOYEES WHERE DEPARTMENT_ID=30;
- SELECT * FROM EMPLOYEES WHERE COMMISION_PCT is null;
- SELECT * FROM EMPLOYEES WHERE FIRST_NAME='jennifer';
- SELECT DISTINCT DEPARTMENT_ID FROM EMPLOYEES;
- SELECT DISTINCT * FROM EMPLOYEES;

>> Logical Operators (AND, OR, NOT)

- USE hr;
- SET SQL_SAFE_UPDATES = 0;
- SELECT * FROM EMPLOYEES;
- SELECT * FROM EMPLOYEES WHERE SALARY>15000 AND JOB_ID = 'AD_VP';
- SELECT * FROM EMPLOYEES WHERE SALARY>15000 OR JOB_ID = 'AD_VP';
- SELECT * FROM EMPLOYEES WHERE NOT FIRST_NAME='david';

>> Between & In Operators

- Between --> Used to display the rows which is following in the range of values.
- Not Between
- USE hr;
- SELECT * FROM EMPLOYEES WHERE SALARY BETWEEN 10000 AND 12000;
- SELECT * FROM EMPLOYEES WHERE SALARY NOT BETWEEN 10000 AND 12000;
- IN --> IN operator return the rows when the values are matching in the list
- Not In
- SELECT * FROM EMPLOYEES WHERE SALARY=3400 OR SALARY=2500 OR SALARY=3000;
- SELECT * FROM EMPLOYEES WHERE SALARY IN (3400,2500,3000);
- SELECT * FROM EMPLOYEES WHERE SALARY NOT IN (3400,2500,3000);

>>Pattern Matching Operators (whiled card characters)

- % --> many characters
- _ --> single character
- SELECT * FROM EMPLOYEES WHERE FISRT_NAME LIKE 'S%';
- SELECT * FROM EMPLOYEES WHERE FISRT_NAME LIKE '%r';
- SELECT * FROM EMPLOYEES WHERE FISRT_NAME LIKE 'S%r';
- SELECT * FROM EMPLOYEES WHERE FISRT_NAME LIKE '%m%';
- SELECT * FROM EMPLOYEES WHERE FISRT_NAME NOT LIKE 'S%';
- SELECT * FROM EMPLOYEES WHERE FISRT_NAME LIKE '%e_';
- SELECT * FROM EMPLOYEES WHERE FISRT_NAME LIKE '___';

# Session - 3

>> DDL Commands (Data Definition Language)
   1) CREATE
   2) ALTER
          -> Add new column
          -> Drop a column
          -> Modify Existing column
          -> Rename the column
   3) DROP
   4) TRUNCATE
   5) RENAME

 Question : Difference between DROP, TRUNCATE and DELETE ?

CREATE & ALTER

> CREATE is used to create database objects (Database, Table, views, synonymes etc...)
> ALTER
  - Adding a new column
  - Dropping the existing column
  - Modifying the existing column (Increase / Decrease size of the column & change the data 
    type of the column)
  - Renaming

  - USE mydb;
  - SELECT * FROM STUDENT;
  - DESCRIBE STUDENT;
    
  --> Adding a new column
  - ALTER TABLE STUDENT ADD (grade varchar(2));
    
  --> Dropping a column from table
  - ALTER TABLE STUDENT DROP COLUMN grade;

  --> Modifying the existing column
  - We can increase/decrease the size of the column.
  - We can decrease the column size ONLY when existing column values can fit into new size
  - Column should be empty should be empty to change its data type.

  - ALTER TABLE STUDENT MODIFY COLUMN SNAME VARCHAR(20);

  --> Remaining a column
  - ALTER TABLE STUDENT RENAME COLUMN SNAME TO STUNAME;


# Session - 4

MySQL Functions
  
> Strings functions - operate on string data types
> Numeric functions - operate on numeric data types
> Date functions - operate on date data types
> Aggregate functions - operate on all of the data types and produce summarized result sets.

-----------------

>> Strings Functions :

> UPPER() - converts into upper case letters
Eg : SELECT UPPER(First_name) from employees;

> LOWER() - converts into lower case letters
Eg : SELECT LOWER(First_name) from employees;

> LENGTH() - return the length of string.
Eg : SELECT LENGTH('GRADE');
Eg : SELECT * FROM EMPLOYEES WHERE LENGTH(FIRST_NAME) = 4;

> TRIM() : Removes the specified characters from both sides
Eg : SELECT TRIM('  welcome  ') FROM Dual;
Eg : SELECT TRIM('z' FROM 'zzoraclezz') FROM Dual;

> INSTR() : Returns the position of the character within a string
Eg : SELECT INSTR('WELCOME','O');

String Functions :

> SUBSTR()/SUBSTRING() : Returns the substring of the string.
  - SELECT SUBSTR('ORACLE',2,3);     --> RAC
  - SELECT SUBSTR('ORACLE',3,3);     --> ACL
  - SELECT SUBSTR('ORACLE',4,3);     --> CLE
  - SELECT SUBSTRING('ORACLE',2,3);  --> RAC
  - SELECT SUBSTRING('ORACLE',3,3);  --> ACL
  - SELECT SUBSTRING('ORACLE',2,3);  --> CLE
  - SELECT SUBSTRING(FIRST_NAME,1,3) FROM EMPLOYEES;

> CONCAT() : To join two strings.
  - SELECT CONCAT('ORACLE','TRAINING');
  - USE hr;
  - SELECT CONCAT(FIRST_NAME,LAST_NAME) FULLNAME FROM EMPLOYEES;

-----------------

>> Numeric Functions :
   - SELECT ABS(-40);
   - SELECT ABS(40);
   - SELECT SQRT(25;
   - select MOD(10,3);
   - select power(2,5);

   > TRUNCATE(): function truncates a number to the specified number of decimal places.
     - SELECT TRUNCATE(40.1234,3);     --  40.123
     - SELECT TRUNCATE(40.1234,2);     --  40.12
     - SELECT TRUNCATE(6876,-1);       --  6870
     - SELECT TRUNCATE(6876,-2);       --  6800
     - SELECT TRUNCATE(68763456,-5);   --  68700000
  > GREATEST() & LEAST(): returns greatest, least values in the provided values.
     - SELECT GREATEST(100,200,300,400,500);
     - SELECT LEAST(100,200,300);

-----------------

>> Date Functions

 > CURDATE()/CURRENT_DATE() function returns the current date
    - SELECT CURDATE();
    - SELECT CURRENT_DATE();
 > CURTIME()/CURRENT_TIME() function returns the current time
    - SELECT CURTIME();
    - SELECT CURRENT_TIME();
 > NOW() function returns the current date and time
    - SELECT NOW();
 > SYSDATE() function returns the current date and time
    - SELECT SYSDATE();
 > MONTH()
    - SELECT MONTH("2019-05-19");   --  5
 > YEAR()
    - SELECT YEAR("2019-05-19");    --  2019
 > DAY()
    - SELECT DAY("2019-05-19");     --  19

>> Queries on Date Functions

   > Display employees who are joined in 1987.
      - SELECT * FROM EMPLOYEES WHERE YEAR(HIRE_DATE) = "1987";
   > Display employees who are joined in june.
      - SELECT * FROM EMPLOYEES WHERE MONTH(HIRE_DATE) = "6";
      - SELECT * FROM EMPLOYEES WHERE MONTHNAME(HIRE_DATE) = "JUNE";

-----------------

>> Aggregate Functions

   - Aggregate Function are all about performing calculations on multiple rows of a single
     column of a table and returning a single value.
   - USE hr;
   - SELECT AVG(SALARY) FROM EMPLOYEEs;
   - SELECT SUM(SALARY) FROM EMPLOYEEs;
   - SELECT MIN(SALARY) FROM EMPLOYEEs;
   - SELECT MAX(SALARY) FROM EMPLOYEEs;
   - SELECT COUNT(*) FROM EMPLOYEEs;


# Session - 5 

