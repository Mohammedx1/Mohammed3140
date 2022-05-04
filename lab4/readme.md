Simple NodeJS Rest API with CRUD routes. Using SQLite database

Add new product:
http://localhost:4300/api/product

Sending a JSON body:

{
	"name": "ExampleProductName",
	"description": "Example product description",
	"price": 2.00,
	"currency": "EUR" 
}




PUT
Update a product:
http://localhost:4300/api/product

Sending a JSON body: ID is the only MANDATORY

{
	"id": "1",
	"name": "ExampleProductName",
	"description": "Example product description",
	"price": 2.00,
	"currency": "EUR" 
}




DELETE
Delete a product:
http://localhost:4300/api/product
Sending a JSON body: ID is the only MANDATORY

{
	"id": "1",
	"name": "ExampleProductName",
	"description": "Example product description",
	"price": 2.00,
	"currency": "EUR" 
}



GET
Load products by ID:
http://localhost:4300/api/product/id/$id
example: http://localhost:4300/api/product/id/15


Load all products:
http://localhost:4300/api/product/
Load products by any attribute and value:
http://localhost:4300/api/product/$attribute/$name

example:
http://localhost:4300/api/product/price/24
http://localhost:4300/api/product/name/Suntone $attribute = ['name', 'price', 'currency', 'description'] (this is not checked values, wrong parameters will return a DB error.)

Load products sorting ASC or DESC by any attribute:
http://localhost:4300/api/product/sort/$direction/$attribute
example:

http://localhost:4300/api/product/sort/asc/price
http://localhost:4300/api/product/sort/desc/price
$attribute = ['name', 'price', 'currency', 'description']* $direction [ASC or DESC]C]* (the direction is checked and when wrong will return a 401 business error)

SQLite database
The database is already populated with 30 random values from https://www.mockaroo.com/

Node version
The Node version used was v16.15.0.
