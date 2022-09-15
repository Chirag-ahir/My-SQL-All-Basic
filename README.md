# My-SQL-All-Basic

¬¬¬¬¬¬¬¬Console for Run Queries: https://console.cloud.google.com/bigquery?project=maximal-centaur-340003
SELECT * FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality` LIMIT 1000
Order by will short your column in ascending order from a to Z
SELECT * 
FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality` 
ORDER BY Births 
LIMIT 10 


Asc is a function to set order from lowest to highest
SELECT *
FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality` 
ORDER BY Births
ASC 
LIMIT 10


Desc is a function to set order from highest to lowest
SELECT *
FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality` 
WHERE Year = '2018-01-01'
ORDER BY Births
DESC
LIMIT 10


SELECT * 
FROM `Mobie_data.Movies` 
WHERE Genre = "Comedy" AND Revenue > 300000000
ORDER BY Release_Date 
DESC

SELECT * FROM Customers
WHERE Country='Germany' AND City='Berlin';

SELECT * FROM Customers
WHERE City='Berlin' OR City='Brampton';

INSERT will insert the data into database columns.
INSERT INTO `customers`(`Name`,`City`,`PostalCode`) 
VALUES('Riddhi','Navasari','346789');


DELETE FROM Customers WHERE Name='chirag';

SELECT TOP will select the first 3 rows from database.
SELECT TOP 3 * FROM Customers; 

Limit will select the first 4 rows from database.
SELECT * FROM Customers LIMIT 4;

MIN will finds the price of the cheapest product.
SELECT MIN(Price) AS SmallestPrice
FROM Products;

MAX finds the most value from column.
SELECT MAX(Price) AS LargestPrice
FROM Products;
COUNT will count the number of items in column
SELECT COUNT(ProductID) FROM Products;

SUM will do the summation of whole price column
SELECT SUM(price) FROM Products

DROP will remove the column from Database
ALTER TABLE customers DROP COLUMN Fax;

Like %p will select all products with a ProductName ending with "p":
SELECT * FROM Products
WHERE ProductName like "%p"

Like p% will select all products with a ProductName starting with "p":
SELECT * FROM Products
WHERE ProductName like "p%"

Like %or% will selects all customers with a CustomerName that have "or" in any position
SELECT * FROM Products
WHERE ProductName LIKE '%or%'

 

Like a%o will selects all customers with a ContactName that starts with "a" and ends with "o":
SELECT * FROM Customers
WHERE ContactName LIKE 'a%o';

NOT Like a% will selects all customers with a CustomerName that does NOT start with "a"
SELECT * FROM Customers
WHERE CustomerName NOT LIKE 'a%';

Like ber% will select all Customers with a CityName starting with Ber.
SELECT * FROM Customers
WHERE City LIKE 'ber%';

 


Like %es% will select all customers that have es in their CityName. 
SELECT * FROM customers where city LIKE '%es%';


The following SQL statement selects all customers with a City starting with "L", followed by any character, followed by "n", followed by any character, followed by "on"
SELECT * FROM Customers WHERE City LIKE 'L_n_on';

 


This will select all the customers with a CityName where the second letter of a city is a.
SELECT * FROM Customers
WHERE City LIKE '_a%';

 

The following SQL statement selects all customers that are located in "Germany", "France" or "UK":
SELECT * FROM Customers
WHERE Country IN ('London','Paris');

The following SQL statement selects all City with a CityName between London and Paris.
SELECT * FROM `customers` 
WHERE City BETWEEN 'London' and 'Paris';

The following SQL statement selects all City with a CityName Not between London and Paris.
SELECT * FROM customers 
WHERE City NOT BETWEEN 'London' AND 'Paris';

BETWEEN and NOT BETWEEN more examples : https://www.w3schools.com/sql/sql_between.asp#:~:text=The%20following%20SQL%20statement%20selects%20all%20orders%20with%20an%20OrderDate%20between%20%2701%2DJuly%2D1996%27%20and%20%2731%2DJuly%2D1996%27%3A

The following SQL statement creates two aliases, one for the CustomerID column and one for the ContactName. This will create two separate column with name ID and CN respectively.
SELECT CustomerID AS ID, ContactName AS CN FROM customers;	
CONCAT command will use for merge rows. 
SELECT ContactName, CONCAT (Address , ' ' , City , ',' , Region , ',' , Country, ' ', PostalCode) AS FullAddress FROM customers;

