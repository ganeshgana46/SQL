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
