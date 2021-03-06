# Getting Started 

_SQL is structured Query Language that is written to interact and manipulate databases. A database is the organization of data into a structure such as table with rows and columns so that data can be easily stored, managed, updated, and retrieved._ 

# Basic Queries: 

## SELECT:
  -  The most basic query to manipulate a database by selecting specified columns 
  
  ### Syntax: 
  ```
    SELECT column 1, column 2... FORM TABLE;
  ```
  
  ### Example: 
  ```
    SELECT name FROM Student;
  ```

  - To select all columns from a table use * symbol: 

  ```
    SELECT * FROM  Student;
  ```

## WHERE:
  - Retrieves data that meet the requirements of the specified condition.
  ```
    SELECT fname FROM Student WHERE  city='Mexico';
  ```

## LIMIT:
  - Retrieves the specified number of data 

  ```
    SELECT fname, lname FROM Student WHERE grade > 75 LIMIT 5;
  ```

## AND:
  - An operator that displays a record if all the conditions separated by AND are true. 

  ```
    SELECT * FROM Student WHERE fname='John' AND lname='Doe';
  ```
## OR:
  - An operator that displays a record if any the conditions separated by the OR is true.

  ```
    SELECT * FROM Student WHERE fname='John' OR lnam='Doe';
  ```
## NOT: 
  - An operator that displays a record if the condition/conditions  are NOT true.

    ### Syntax: 

    ```
      SELECT column 1, column 2, ... FROM table_name WHERE NOT condition;
    ```

    ### Example: 
  ```
    SELECT * FROM Student WHERE NOT lname='Doe';
  ```
## LIKE:
  - An operator that used in WHERE clause to search for a specified pattern in a column.
  - The two wild cards often used in conjunction with the LIKE operator: 
    - % the percent sigh represents zero, one, or multiple characters.
    - _ the underscore represents a single character. 

    ### Syntax: 

    ```
      SELECT column 1, column 2, ... FROM table_name WHERE column LIKE pattern; 
    ```

    ### Example: 
  ```
    SELECT * FROM Student WHERE lname LIKE 'a%';
  ```

  This will return all students with a last name that starts with "a".

## ORDER BY:
  - A keyword used to sort the result-set in ascending or descending order. 

    ### Syntax: 

    ```
      SELECT column 1, column 2, ... FROM table_name ORDER BY column 1, column 2, ... ASC|DESC;
    ```

    ### Example: 
  ```
    SELECT * FROM Student ORDER BY Country DESC;
  ```

## IN:
  - An operator that allows you to specify multiple values in a WHERE clause. 
  - A short hand for multiple OR conditions.

    ### Syntax: 

    ```
      SELECT column 1, column 2, ... FROM table_name WHERE column  IN (value 1, value 2,...);
    ```

    ### Example: 
  ```
    SELECT * FROM Student WHERE Country IN ('Germany', 'France', 'UK');
  ```

  This will return all students that are located in either country.

# Server Functions (String functions) : 

 - Built-in SQL server functions.

  ## UPPER(): 
   - A function that converts column data to upper-case.

  ### Syntax: 
  ```
    SELECT UPPER(column)
  ```

  ### Example: 
  ```
    SELECT UPPER(fname) FROM Students;
  ```

  This will return a column of all fnames capitalized.

  ## LOWER(): 
   - A function that converts column data to lower-case.

  ### Syntax: 
  ```
    SELECT LOWER(text)
  ```

  ### Example: 
  ```
    SELECT LOWER(fname) FROM Students;
  ```

  This will return a column of all fnames lower cased.


# Set-up

[Database Normalization](https://www.youtube.com/watch?v=ABwD8IYByfk): 

_Database Normalization is a technique of organizing the data in the database. It is systematic approach of decomposing tables to eliminate redundancy.A multi-step process of putting a data in tabular form to reduce the redundancy of data  and improves data integrity._

[Entity Relationship Diagram](https://www.youtube.com/watch?v=QpdhBUYk7Kk): 

