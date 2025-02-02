Pizza Express Management System

<== 
Overview

The Pizza Express Management System is a RESTful API built using ASP.NET Core and Entity Framework Core. It provides functionality to manage pizza types,
customers, and orders. The system also supports an optional Angular frontend for interacting with the API.

==>

<== Prerequisites

Ensure you have the following installed on your system:

.NET Core SDK (3.1 or 6)

SQL Server, SSMS

Visual Studio, Visual Studio Code, or CLI

==>

<== Configure Backend Project

1. restore all packages using nuget restore
2. run these two commands for setting database 
	before setting database first update connection string which is mentioned in appsettings.json
	"ConnectionStrings": {
 		 "DefaultConnection": "Server=YOUR_SERVER;Database=PizzaExpressDB;Trusted_Connection=True;MultipleActiveResultSets=true"
	}
	
	then run these commands, if anyone fails then check nuget packages is properly installed or restored if not then install manually these two packages
		( Microsoft.EntityFrameworkCore, Microsoft.EntityFrameworkCore.Relational, Microsoft.EntityFrameworkCore.SqlServer )

	a. add-migration init
	b. update database
3. then run the project using F5

==>

<== About API Endpoints

<==
Pizza Management

GET /api/pizzas - Get all pizzas

POST /api/pizzas - Create a pizza

PUT /api/pizzas/{id} - Update a pizza

DELETE /api/pizzas/{id} - Delete a pizza
==>

<==
Order Management

GET /api/orders - Get all orders

GET /api/orders/{id} - Get order by ID

POST /api/orders - Create an order

PUT /api/orders/{id}/status  - Update an order status

DELETE /api/orders/{id} - Delete an order

==>

<==
Customer Management

GET /api/customer - Get all customer

GET /api/customer/{id} - Get customer by ID

POST /api/customer - Create an customer

PUT /api/customer/{id}  - Update an customer

DELETE /api/customer/{id} - Delete an customer
==>


<== TEST Project

run test command (dotnet test) or run manually using visual studio 

==>
