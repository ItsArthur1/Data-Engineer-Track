<h1>Writing Queries - Chapter Five</h1>

<h2> - Aliasing </h2>

Aliasing is used to rename columns, not in the database, just in the result set.


A query can either be a request for data results from your database or for action on the data, or for both.

For example:

```SQL

SELECT name AS first_name, year_hired
FROM employees;

# In this query, aliasing is used to rename name as first_name

```
The keyword AS is used to indicate the alias.

<br>

<h2> - Selecting distinct records. </h2>

The keyword DISTINCT, eliminates all duplicate records from the result returned by the SQL query.

For example:

````SQL

SELECT DISTINCT year_hired
FROM employees;

--The result set of this query are the unique values of the year_hired field.


````

<br>

<h2> - Distinct with multiple fields. </h2>

We have to add the keyword DISTINCT before the fields to select

Query code:


````SQL
SELECT DISTINCT dept_id, year_hired
FROM employees;

````

<br>


<h2> - Views. </h2>

In SQL, a view refers to a table that is the result of a saved SQL SELECT statement.

Views are considered virtual tables, this means that the data a view contains is not generally stored in the database. Rather, it is the query code that is stored for future use

A benefit of this is that whenever the view is accessed, it automatically updates the query results to account for any updates to the underlying database.

To create a view, we'll add a line of code before the SELECT statement: CREATE VIEW, then the name we'd like for the new view, then the AS keyword to assign the results of the query to the new view name.


Query code example:

````SQL

CREATE VIEW employee_hire_years AS
SELECT id, name, year_hired
FROM employees;

````
There is no result set when creating a view.


<br>

<h2> Using Views </h2>

Using the last query example, this is how a view is used.

Query code:

````SQL

SELECT id, name
FROM employee_hire_years;

````

Once a view is created, however, we can query it just as we would a normal table by selecting FROM the view.


<h2> QUERY CODE EXAMPLES: </h2>

<br>

<h3> Example one, using Distinct: </h3>


````SQL
SELECT DISTINCT author, genre
FROM books;

````

<h3> Using Aliasing (AS) with DISTINCT <h3>

```SQL
SELECT DISTINCT author AS unique_author
FROM books;

```

<h3> Viewing a query: </h3>

<br>

- Creating the view:

````SQL
CREATE VIEW library_authors AS
SELECT DISTINCT author AS unique_author
FROM books;

````
- Viewing, querying the view:

````SQL
SELECT * 
FROM library_authors
````