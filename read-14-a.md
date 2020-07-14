# Introduction to Database Normalization

Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included. Take a spreadsheet containing the information as an example, where the data contains salespeople and customers serving several purposes:

* Identify salespeople in your organization
* List all customers your company calls upon to sell a product
* Identify which salespeople call on specific customers.

>By limiting a table to one purpose you reduce the number of duplicate data contained within your database. This eliminates some issues stemming from database modifications.

![db](https://miro.medium.com/max/534/1*EWVK-l6xn35SkwtHa8PQhA.png)

**There are three main reasons to normalize a database:**

1. to minimize duplicate data.
1. to minimize or avoid data modification issues.
1. to simplify queries. 

**There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively, let’s summarize the various forms:**

* **First Normal Form** – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
* **Second Normal Form** – The table is in first normal form and all the columns depend on the table’s primary key.
* **Third Normal Form** – the table is in second normal form and all of its columns are not transitively dependent on the primary key.






