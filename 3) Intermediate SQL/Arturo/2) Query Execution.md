<h1>Query execution - Chapter two</h1>

- SQL code is not processed in the order it is written. 

Order of Execution:

| Order 	| KEYWORD  	| Function                                     	|
|-------	|----------	|----------------------------------------------	|
| 1     	| FROM     	|The FROM command is used to specify which table to select or delete data from. 	    |
| 2     	| WHERE    	| The WHERE command filters a result set to include only records that fulfill a specified condition.                      	    |
| 3     	| GROUP BY 	| The GROUP BY command is used to group the result set (used with aggregate functions: COUNT, MAX, MIN, SUM, AVG).                    	    |   
| 4     	| HAVING   	| The HAVING command is used instead of WHERE with aggregate functions.               	|
| 5     	| SELECT   	| The SELECT command is used to select data from a database. The data returned is stored in a result table, called the result set.                     	|
| 6     	| ORDER BY 	| The ORDER BY command sorts the result set in ascending order by default. To sort the records in descending order, use the DESC keyword.                       	|
| 7     	| LIMIT    	| The LIMIT, SELECT TOP or ROWNUM command is used to specify the number of records to return.    	|

<br>

<h2> Debugging SQL</h2>

It is important to know how to read the error messages while working with SQL. Some messages are extremely helpful, pinpointing and even suggesting a solution, as this message does when we misspell the field we'd like to select. Other common errors may involve incorrect capitalization or punctuation.


<h2> Comma errors</h2>

- Look out for comma errors, example:

Query example:

````SQL

SELECT title, country duration 
FROM films

-- The error is that the comma does not exist between country and duration

-- syntax error at or near "duration"


````


<h2> Keyword errors errors</h2>

SQL displays a similar error message when a keyword is misspelled, but this time, the caret indicator below the offending line is spot on.

Query example:

````SQL

SELCT title, country, duration
FROM films;

-- syntax error at or near "SELCT"

````


<h2> Most common errors</h2>

- Misspelling
- Incorrect capitalization
- Incorrect or missing punctuation, especially commas

Learn from mistakes!



<h2> Debugging errors examples</h2>

This section is for examples of debugging errors examples

<br>

<h3>Example 1: </h3>

Instruction: Debug and fix the SQL query.

````SQL

SELECT certfication
FROM films
LIMIT 5;

````

Answer:

````SQL
SELECT certification
FROM films
LIMIT 5;

-- "certification" was misspelled

````

<br>


<h3>Example 2: </h3>

Instruction: Find the two errors in this code; the same error has been repeated twice.

````SQL

SELECT film_id imdb_score num_votes
FROM reviews;
````

Answer:

````SQL
SELECT film_id, imdb_score, num_votes
FROM reviews;

-- there was a missing comma betwen "imdb_score" and "num_votes", and betwen "film_id" and "imdb_score"
````


<br>


<h3>Example 3: </h3>

Instruction: Find the two bugs in this query.

````SQL
SELECT COUNNT(birthdate) AS count_birthdays
FROM peeple;

````

Answer:

````SQL
SELECT COUNT(birthdate) AS count_birthdays
FROM people;

-- "COUNT" and "people" were misspelled

````
