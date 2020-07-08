# SQL

**SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.**

>Before learning the SQL syntax, it's important to have a model for what a relational database actually is. A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

>To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries. A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. It has a specific syntax though, which is what we are going to learn in the following exercises

>Now we know how to select for specific columns of data from a table, but if you had a table with a hundred million rows of data, reading through all the rows would be inefficient and perhaps even impossible.

>In order to filter certain results from being returned, we need to use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.

**When writing WHERE clauses with columns containing text data, SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching. We show a few common text-data specific operators below:**

Operator |	Condition |	Example
-------- | -------- | --------
= |	Case sensitive exact string comparison (notice the single equals) |	col_name = "abc"
!= | or <>	Case sensitive exact string inequality comparison |	col_name != "abcd"
LIKE |	Case insensitive exact string comparison |	col_name LIKE "ABC"
NOT LIKE |	Case insensitive exact string inequality comparison |	col_name NOT LIKE "ABCD"
% |	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE) |	col_name LIKE "%AT%"
(matches "AT", "ATTIC", "CAT" or even "BATS")
_ |	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) |	col_name LIKE "AN_"
(matches "AND", but not "AN")
IN (…) |	String exists in a list |	col_name IN ("A", "B", "C")
NOT IN (…) |	String does not exist in a list |	col_name NOT IN ("D", "E", "F")

>Even though the data in a database may be unique, the results of any particular query may not be – take our Movies table for example, many different movies can be released the same year. In such cases, SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.

>Tables that share information about a single entity need to have a primary key that identifies that entity uniquely across the database. One common primary key type is an auto-incrementing integer (because they are space efficient), but it can also be a string, hashed value, so long as it is unique.Using the JOIN clause in a query, we can combine row data across two separate tables using this unique key. The first of the joins that we will introduce is the INNER JOIN.

>As promised in the last lesson, we are going to quickly talk about NULL values in an SQL database. It's always good to reduce the possibility of NULL values in databases because they require special attention when constructing queries, constraints (certain functions behave differently with null values) and when processing the results.
