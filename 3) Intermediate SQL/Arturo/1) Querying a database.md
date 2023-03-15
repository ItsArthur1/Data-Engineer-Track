<h1>Querying a Database - Chapter one</h1>

- A query is a request for data from a database.

<h2> COUNT() </h2>

The count function returns the number of records with a value in a field.

Query example:

````SQL
SELECT COUNT(birthdate) AS count_birthdates
FROM people;


````
The result set is a number of birthdates that exists in the database.

Result set example:

| count_birthdates 	|
|------------------	|
| 567 	            |   

<h2> COUNT with multiple fields </h2>

Query example:



````SQL

SELECT COUNT(name) AS count_names, COUNT(birthdate) as count_birthdates
FROM people;

````

<h2> Using * with COUNT() </h2>

If we use COUNT(*) this counts records in a table


Query example:

````SQL

SELECT COUNT(*) AS total_records
FROM people;

-- The result set is the total values of the table people.  The asterisk represents all fields. Passing the asterisk to COUNT is a shortcut for counting the total number of records.

````


<h2> DISTINCT </h2>

The DISTINCT keyword select all the unique values from a field. This is useful if we want to our query will remove all duplicates.

Query example:

````SQL

SELECT DISTINCT language
FROM people;

-- The result set is the total values of the table people.  The asterisk represents all fields. Passing the asterisk to COUNT is a shortcut for counting the total number of records.

````

<br>

<h2> COUNT() with DISTINCT </h2>

This is useful to count the number of unique values in a field.

Query example:

````SQL

SELECT COUNT(DISTINCT birthdate) AS count_distinct_birthdates
FROM people;

````

- COUNT() includes duplicates
- DISTINCT excludes duplicates

<h2> Query Example</h2>


````SQL

-- Count the number of records in the people table

SELECT COUNT(id) AS count_records
FROM people;

````



````SQL

-- Count the number of records with a birthdate in the people table, aliasing the result as count_birthdate.

SELECT COUNT(id) AS count_records
FROM people;

````

````SQL

-- Count the languages and countries represented in the films table

SELECT COUNT(language) AS count_languages , COUNT(country) AS count_countries
FROM films;

````


````SQL
-- Return the unique countries from the films table

SELECT DISTINCT country
FROM films;

````

````SQL
-- Count the distinct countries from the films table

SELECT COUNT(DISTINCT(country)) AS count_distinct_countries
FROM films;
````