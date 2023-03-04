<h1>Database - Chapter one</h1>

- Database: A database stores data.
- The information is housed in objects
- Tables are objects (Patrons, books, checkouts)
- Data is orginized as the rows of the columns
- This database contains 3 tables.

<br>

This is a Relational Database containing three tables, from a Library:

<br>

patrons: 

| card_num 	| name   	| member_year 	| total_fine 	|
|----------	|--------	|-------------	|------------	|
| 54378    	| Izzy   	| 2012        	| 9.86       	|
| 94722    	| Maham  	| 2020        	| 0          	|
| 45783    	| Jasmin 	| 2022        	| 2.05       	|
| 90123    	| James  	| 1989        	| 0          	|

<br>

books:

| id  	| title                     	| author         	| genre       	| pub_year 	|
|-----	|---------------------------	|----------------	|-------------	|----------	|
| 638 	| Being Mortal              	| Atul Gawande   	| Non-Fiction 	| 2015     	|
| 912 	| Educated                  	| Tara Westover  	| Non-Fiction 	| 2018     	|
| 322 	| Night                     	| Elie Wiesek    	| Non-Fiction 	| 1956     	|
| 156 	| Where The Wild things Are 	| Maurice Sendak 	| Childrens   	| 1963     	|

<br>

checkouts:

| id  	| start_date 	| due_date   	| card_num 	| book_id 	|
|-----	|------------	|------------	|----------	|---------	|
| 567 	| 2022-05-13 	| 2022-05-27 	| 54378    	| 638     	|
| 568 	| 2022-06-10 	| 2022-06-24 	| 54378    	| 322     	|
| 569 	| 2022-06-27 	| 2022-07-11 	| 45783    	| 156     	|
| 570 	| 2022-08-14 	| 2022-08-28 	| 90123    	| 912     	|

<br>

<h2>Relational Databases</h2>

A relational database defines relationships between tables of data inside the database.

Example:

Library patron is associated with several checkouts, this can answer questions like: "Which books did James check out during 2022?" or "Which books are checked out most often?"

We can see above, the tables of the database, and we can look that, checkouts and books have also a relationship.

<br>

<h2>Database Advantages</h2>

- The tables could look similar to the way data is organized in spreadsheet.

- Databases are are far more powerful than a spreadsheets like the in Excel or Google Sheets.

- Databases can store much more data, storage is more secure due the encryption.

- The biggest advantage of a databes is that, many users can write queries to gather insights form the data at the same time.

- When a database is queried, the database information is accessed and presented according to instructions in the query.

Other advantages: 

- More Storage.
- Secured with encription.
- Many people can use at once

<h2>SQL</h2>

- SQL, S-Q-L, is short for Structured Query Lenguage.
- SQL is the most widely used programming lenguage for creating, quering and updating relational databases.



