<h1>Introducing to Queries - Chapter Four</h1>

<h2> - What is SQL useful for? </h2>

SQL is used to answer questions both wihtin and across relational database tables.

A query can either be a request for data results from your database or for action on the data, or for both.

For example: In the library database, we might use SQL to find which books James checked out from the library in 2022.

<br>

<h2> - Best for large datasets  </h2>

In the big organizations, SQL is used as a complement to other tools such as spreadsheets applications.

If the data we're interested in can fit in a spreadsheet and does not have many relationships to other data of interest, we can analyze it in a spreadsheet. But for sprawling and diverse data such as the data related to a retail platform, organizing the data in a database is best.


<h2>- Keywords of a query </h2>

To write SQL, is necesary to learn a few keywords, keywords are reserved words used to indicate what operation we'd like our code to perform. The most common keywors are:

- SELECT
- FROM

The SELECT keyword indicates which fields should be selected for the result set.

The FROM keyword indicatres indicates the table in which these fields are located.


<h2>- Query Code</h2>


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
 


This is a query from the library database above:

```

SELECT name
FROM patrons;

# The result set lists all names from the patrons table.


```
It's best practice to end the query with a semicolon to indicate that the query is complete.
Also it is necesary to capitalize the keywords while keeping the table and name fields names all lowercase.

The Query results are often called "result set".

<br>

<h2>- Selecting multiple fields</h2>

To select multiple fields, we can list multiple field names after the SELECT keyword, separated by commas

```

SELECT card_num, name
FROM patrons;

# The result set lists all names and card number from the patrons table.


```

Other example:


```

SELECT card_num, name, total_fine
FROM patrons;

# The result set lists all  names, card number and total fine from the patrons table.


```

<br>

<h2>- Selecting all fields</h2>


```

SELECT *
FROM patrons;

# The result set lists all the fields from the table patrons


```

The asterisk represent all the fields, it is a easier way to query all the fields from a table.