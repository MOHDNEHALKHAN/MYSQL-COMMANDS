# MYSQL CHEATSHEET

|                                              COMMANDS |                                            THEIR USES |
| --- | --- |
| `CREATE DATABASE db-name`   **or**  `create database db-name` | It will create a database |
| `CREATE DATABASE IF NOT EXITS db-name`    | It will create a database only if there is no other database of that same name |
| `DROP DATABASE db-name`   **or**  `drop database db-name` | It will help to delete the database |
| `DROP DATABASE IF NOT EXITS db-name` | It will delete database only if there is no other database of that same name |
| `USE db-name`    | It will start using the specified database i.e. now you can create tables in the selected database |
| `SHOW DATABASES;` | It will show all the databases in the system |
| `SHOW TABLES;` | It will show all the tables in a selected database |
| `DROP TABLE table-name`   **or**  `drop table table-name` | It will help to delete a table in a database |
| `CREATE TABLE table-name (                       column_name1 datatype constraint ,               column_name2 datatype constraint,                 column_name3 datatype constraint                      );` | This query is used to create a table in the selected database |
| `INSERT INTO  table_name VALUES( PARAMETERS);`  **or**                  `INSERT INTO table_name (column 1 , column 2)` | It will add data into the selected table |
| `SELECT * FROM table_name` | It will retrieve all the data of the selected table` |
| `SELECT * FROM table_name                           WHERE <condition_to_satisfy>;` | It will retrieve all the data of the row that will satisfy the condition |
| `UPDATE table_name                                    SET col1 = val1, col2 = val2                        WHERE condition;` | It will update the values of selected columns |
| `DELETE FROM table_name  WHERE condition;`  | It will delete the entire row that will satisfy the condition |
| `ALTER TABLE table_name ADD COLUMN coulmn_name datatype constraint;` | It will add a new column in your table |
| `ALTER TABLE table_name DROP COLUMN coulmn_name ;` | It will delete the complete table from the database |
| `ALTER TABLE table_name RENAME TO new_table_name;` | the table's name will be changed from old_table to new_table, |
| `ALTER TABLE table_name  CHANGE COLUMN old_name new_name new_datatype new_constraint;` | It will change the name of the old column in the table |
| `ALTER TABLE table_name                               MODIFY coulmn_name new_datatype new_constraint;` | It will update the data type or size of old column |
| `ALTER TABLE table_name                               TRUNCATE COLUMN table_name;` | This command will remove the specified column from the table.  |
|`SELECT column(s) FROM tableA INNER JOIN tableB ON tableA.col_name = table.col_name;` | It returns all rows from multiple tables where the join condition is satisfied.It is the mostcommon type of join.|
| `SELECT column(s)FROM  tableA LEFT JOIN tableB    ON tableA.col_name = table.col_name;` | It returns all rows from the left-hand table specified in the ON condition and only those rows from the other table where the join condition is fulfilled. |
| `SELECT column(s)                                    FROM tableA                                         RIGHT JOIN tableB                                      ON tableA.col_name = table.col_name;` | It returns all rows from the right-hand table specified in the ON condition and only those rowsfrom the other table where the join condition is satisfied |
| `SELECT column(s)     FROM table as a                                        JOIN table as b                                        ON a.col_name = b.col_name;` | In this join, table is joined with itself |
| `SELECT * FROM tableA as a                           LEFT JOIN tableB as b                                  ON a.id = b.id                                      UNION                                              SELECT * FROM tableA as a                           RIGHT JOIN tableB as b                                 ON a.id = b.id;` | It combines the results of both left and right outer joins |
| `SELECT column(s)                                    FROM table_name                                     WHERE col_name operator                      (Subquery);` | It will retrieve data of selected columns that will satisfy the condition` |
| `CREATE VIEW  view1 AS                             SELECT parameters FROM table_name` | It is to create a database view named view1 that presents data from the specified table_name using the SELECT statement provided. |
| `Desc table_name;` | It allows you to see the table structure |
| `Select No.1 + No.2;` | It will add two numbers |
| `Select No.1 - No.2;` | It will subtract the second number from first |
| `Select No.1 * No.2;` | It will give the product of supplied numbers |
| `Select No.1/No.2;` | It will divide the number |
| `Select <co11>, <col2>From table_name Where value1 Between value2;` | It will only retrieve data of those columns whose values will fall between value1 and value2 (both inclusive) |
| `Select * from table_nameWhere column_name IN (val1,val2,val3);` |Condition Based on a List |
| `"Select * from table_nameWhere column_name NOT IN (val1,val2,val3);”` | Condition Based on a List |
| `Select Char(72,97,114,114,121);` | It returns the character for each integer passed |
| `Select Concat("Nehal","Khan");` | It concatenates two strings |
| `Select Lower("Brother");` | It converts a string into lowercase |
| `Select Upper("nehal");` | It converts a string into uppercase |
| `Select Substr(string,m,n);` | It extracts a substring from a given string |
| `Select Trim(leading ' ' FROM ' Harry Bhai');` | It removes leading and trailing spaces from a given string |
| `Select Instr(String1,String2);` | It searches for given second string into the given first string |
| `Select Length(String)` | It returns the length of given string in bytes |
| `Select MOD(11,4);` | It returns modulus of two numbers |
| `Select Power(m,n);` | It returns the number m raised to the nth power |
| `Select Round(15.193,1);` | It returns a number rounded off number |
| `Select Sqrt(144);` | It returns the square root of a given number |
| `Select Truncate(15.75,1);` | It returns a number with some digits truncated |
| `Select Curdate();` | It returns the current date |
| `Select Date('2021-12-10 12:00:00');` | It extracts the date part of the expression |
| `Select Month(date);` | It returns the month from the date passed |
| `Select Day(date);` | It returns the day part of a date |
| `Select Year(date);` | It returns the year part of a date |
| `Select now();` | It returns the current date and time |
| `Select sysdate();` | It returns the time at which function executes |
| `Select AVG(<column_name>) "Alias Name" from <table_name>;` | It calculates the average of given data |
| `Select Count(<column_name>) "Alias Name" from <table_name>;` | It counts the number of rows in a given column |
| `Select Max(<column_name>) "Alias Name" from <table_name>;` | It returns the maximum value from a given column |
| `Select Min(<column_name>) "Alias Name" from <table_name>;` | It returns the minimum value from a given column |
| `Select Sum(<column_name>) "Alias Name" from <table_name>;` | It returns the sum of values in given column |
| `Select <column>, Count(*) from <table_name> group by <column>;` | It allows you to group two or more columns and then you can perform aggregate function on them |
| `Select avg(<column>), sum(<column>) from <table_name> group by <column_name>` | Having clause is used to put conditions on groups |
| `Create table <table_name>( col1 data_type NOT NULL,col2 data_type,col3 data_type);` | It will create a table with NOT NULL constraint to its first column |
| `Create table table_name( col1 data_type DEFAULT 50,col2 data_type,col3 data_type);` | DEFAULT constraint provides a default value to a column |
| `Create table table_name( col1 data_type UNIQUE,col2 data_type,col3 data_type);` | UNIQUE constraint ensures that all values in the column are different |
| `Create table table_name( col1 data_type CHECK (condition),col2 data_type,col3 data_type);` | CHECK constraint ensures that all values in a column satisfy certain conditions |
| `Create table table_name( col1 data_type Primary Key,col2 data_type,col3 data_type);` | Primary key is used to uniquely identify each row in a table |
| `CREATE TABLE Orders (OrderID int NOT NULL, OrderNumber int NOT NULL,PersonID int, PRIMARY KEY (OrderID), FOREIGN KEY (PersonID) REFERENCES Persons(PersonID));` | Foreign key is used to link data from another table |
| `Create table <table_name>( col1 data_type NOT NULL,col2 data_type,col3 data_type);` | It will create a table with NOT NULL constraint to its first column |
| `Create table table_name( col1 data_type DEFAULT 50,col2 data_type,col3 data_type);` | DEFAULT constraint provides a default value to a column |
| `Create table table_name( col1 data_type UNIQUE,col2 data_type,col3 data_type);` | UNIQUE constraint ensures that all values in the column are different |
| `Create table table_name( col1 data_type CHECK (condition),col2 data_type,col3 data_type);` | CHECK constraint ensures that all values in a column satisfy certain conditions |
| `Create table table_name( col1 data_type Primary Key,col2 data_type,col3 data_type);` | Primary key is used to uniquely identify each row in a table |
| `CREATE TABLE Orders (OrderID int NOT NULL, OrderNumber int NOT NULL,PersonID int, PRIMARY KEY (OrderID), FOREIGN KEY (PersonID) REFERENCES Persons(PersonID));` | Foreign key is used to link data from another table |

Download the Pdf for the Cheatsheet
[Click Here👇](https://nehalkhan.gumroad.com/l/ccwau?layout=profile)

### Note - `If face any issue regarding commands, please raise a issue i will solve for the same`
