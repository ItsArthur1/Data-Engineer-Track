<h1>Tables - Chapter two</h1>

- Tables hold related data about a particular subject.
- Tables are organized into rows and columns.
- Rows are oftern referred to as records
- Columns are often referred to as fields.
- Tables field are limited to those set when the database was created, but the number of rows is unlimited.


<br>

<h2> Good table manners </h2> 

- Table names should be lowercase and should not include spaces.
- Table names use underscores in place of spaces example: "table_name"
- Table name would refer to a collective group example "inventory", but it is also okay for the table to have plural name, example "products".

Field naming is important, field names should be lowercase and should not involve spaces, a field name should be singular rather tha plural, because it refers to the information contained in that field for a single record.

Field name should never share a name with the table they are housed in.


<br>


<h2> Laying the table: records</h2>

- A record is a row in a table.
- A record holds datan on an individual observation.

As we can see, the table patron only has 4 records, one for each of the patron.
Example: The record for Jasmin indicates that she became a member in 2022 and owes two dolars and five cents in fines. That example describes a record.




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

<h2>Laying the table: Fields</h2>

- A field is a column in a table.
- It holds one piece of information about all observations in the table.

The "name" field in the patrons table, lists all of the names of the library patrons.

<br>
<h2> Assigned Seats. </h2>

A unique indentifier is called "key", it is a unique value which identifies a record so that can be distinguished from other records in the same table.

- This value is very often a number.

For example, in the patrons table above, card_num field is the unique indetifier for each patron.

<br>


<h2> Suggest to improvement Table</h2>

| ids 	| customers 	| phone_nums  	| emails       	| zip_codes 	|
|-----	|-----------	|-------------	|--------------	|-----------	|
| 567 	| Jelle     	| 778-545-444 	| ex@mail.com  	| 89798     	|
| 568 	| Raushan   	| 756-863-333 	| ex2@mail.com 	| 55663     	|
| 569 	| Catalina  	| 666-666-666 	| ex3@mail.com 	| 88966     	|
| 570 	| Jorge     	| 789-556-664 	| ex4@mail.com 	| 00233     	|


In this table example, we can see some errors on it, so i created some suggestions so we can look and notice them.





<br>


| Suggest to improvemnt.                   	| Do not suggest for improvement.                         	|
|------------------------------------------	|---------------------------------------------------------	|
| The customers field should be renamed    	| Underscores in the field should be replaced with spaces 	|
| The field names should be made singular  	| The field names should be capitalized                   	|
| The table name should not be capitalized 	| The table name should be made singular                  	|

-  The customers field should be renamed because the table fields always have to be singular and a field refers to the information contained in that field for a single record.

- The field names should be made singular, the reason is explain above this point.

- The table name should not be capitalize beacause queries are harder to write if you do that, table name should be lowercase.