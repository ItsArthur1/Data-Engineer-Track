<h1>SQL flavors - Chapter Six</h1>

SQL has a few different versions, some are free, while others are paid, but, have customer support and made to complement, like Microsoft's SQL Server or Oracle Database, which are used by many companies. 

All SQL versions are used whit table-based relational databases.

The vast majority of keywords are shared between all these versions. All SQL versions must follow universal standards set by the International Organization for Standards and the American National Standards Institute. 


<h2> Two popular SQL flavors.</h2>

- PostgreSQL is a free and open-source relational database system which was originally created at the University of California, Berkeley, and was sponsored by America's famous Defense Advanced Research Projects Agency, or DARPA. DARPA also sponsored research leading to creating the internet, the computer mouse, and GPS! The name "PostgreSQL" is used to refer to both the database system itself as well as the SQL flavor used with it. 

- SQL Server is also a relational database system which comes in both free and enterprise versions. It was created by Microsoft, so it pairs well with other Microsoft products. T-SQL is Microsoft's proprietary version of SQL, used with SQL Server databases.



<h2> Comparing PostrgreSQL and SQL Server</h2>

This is an example of a small difference between SQL Server and PostgreSQL: 

<br>

PostgreSQL:

Query Code:

````
SELECT id, name
FROM employees
LIMIT 2;

````
<br>


SQL Server:


Query Code:

````
SELECT id, name
FROM employees
TOP 2;

````

<h2> Using LIMIT </h2>

The keyword LIMIT is used for limiting the output of the result test.

Query code example:

````

SELECT genre
FROM books
LIMIT 10;

````
