<h1>SQL style - Chapter three</h1>



<br>

<h2> SQL formatting</h2>

- Formating is not required
- Lack of formatting can cause issues

New lines, capitalization, and indentation are not required in SQL as they sometimes are in other programming languages. 

for example:

````SQL

select title, release_year, country from films limit 3

````
The previus query will run just fine

<br>

<h2> Best Practices</h2>

- Capitalize keywords
- Add new lines between them
- Use underscores in fields rather than spaces
- End queries with a semicolon

Query example:

````SQL

SELECT title, release_year, country
FROM films
LIMIT 3;

````


<br>

<h2> Style guides</h2>

It's helpful to follow a SQL style guide, such as Holywell's, which outlines a standard of best practices for indentation, capitalization, and naming conventions for tables, fields, and aliases. It is important to remember, though, that there is no single required formatting in SQL: the guiding principle is writing clear and readable code.

This link has more info about style guides (https://www.sqlstyle.guide/)

<br>

<h2> Semicolon</h2>

The semicolon is unnecessary in PostgreSQL; we could leave it out of the query and still expect the same results with no errors. However, including a semicolon at the end of the query is considered best practice for several reasons. First, some SQL types require it, so it's a good habit to have. Including a semicolon in a PostgreSQL query means that the query is more easily translated to another type if necessary. Additionally, like a period at the end of a sentence, a semicolon at the end of a query indicates its end, which is helpful in a file containing several queries.

<br>

<h2> Dealing with non-standard field names</h2>

- Example: "release year" instead of "release_year"
- Put non-standard field names in doble-quotes

Query example:

````SQL

SELECT title, "release year", country
FROM films
LIMIT 3;

````


<br>

<h2> Why do we formay?</h2>

- Easier colaboration
- Clean and readable
- Looks professional
- Easier to understand



<br>


<h2> Query examples</h2>

<h3> Formatting :</h3>

Instructions: Adjust the sample code so that it is in line with standard practices

```SQL
-- Rewrite this query
select person_id, role from roles limit 10

```

Answer:

```SQL
SELECT person_id, role  
FROM roles 
LIMIT 10;

```



