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

CREATE: to create a database and its objects like (table, index, views, store procedure, function, and triggers)
ALTER: alters the structure of the existing database
DROP: delete objects from the database
TRUNCATE: remove all records from a table, including all spaces allocated for the records are removed
COMMENT: add comments to the data dictionary
RENAME: rename an object

Data Manipulation Language:
           DML is the short name for Data Manipulation Language which deals with data manipulation and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is used to store, modify, retrieve, delete and update data in a database.

SELECT: retrieve data from a database
INSERT: insert data into a table
UPDATE: updates existing data within a table
DELETE: Delete all records from a database table
MERGE: UPSERT operation (insert or update)
CALL: call a PL/SQL or Java subprogram
EXPLAIN PLAN: interpretation of the data access path
LOCK TABLE: concurrency Control

Data Control Language:
          DCL is short for Data Control Language which acts as an access specifier to the database.(basically to grant and revoke permissions to users in the database

GRANT: grant permissions to the user for running DML(SELECT, INSERT, DELETE,…) commands on the table
REVOKE: revoke permissions to the user for running DML(SELECT, INSERT, DELETE,…) command on the specified table

Transactional Control Language:
          TCL is short for Transactional Control Language which acts as an manager for all types of transactional data and all transactions.Some of the command of TCL are

Roll Back: Used to cancel  or Undo changes made in the database 
Commit: It is used to apply or save changes in the database
Save Point: It is used to save the data on the temporary basis in the database

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


