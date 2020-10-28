# SQL day 2 - 3!

The following are the commands we covered in class!


```sql

  -- SELECT columns FROM Table WHERe Condition

  -- to use with Select
  --  TOP

  -- Count

  -- Distinct
  SELECT Country, ContactName FROM Customers
  WHERE ContactTitle = 'Owner';

  SELECT DISTINCT Country FROM Customers
  WHERE ContactTitle = 'Owner';

  -- count the Distinct
  SELECT COUNT(DISTINCT Country) FROM Customers
  WHERE ContactTitle = 'Owner';

  -- WHERE column = 'value'

  -- WHERE
  -- SELECT * FROM Products;

  SELECT ProductName, UnitPrice, CategoryID, Discontinued FROM Products
  WHERE CategoryID = 1;

  -- AND - must fulfill the two sides
  SELECT ProductName, UnitPrice, CategoryID, Discontinued FROM Products
  WHERE CategoryID = 1 AND Discontinued = 0;


  -- Using and to create range
  -- AND - must fulfill the two sides
  SELECT ProductName, UnitPrice, CategoryID, Discontinued FROM Products
  WHERE CategoryID > 2 AND CategoryID <= 5;

  -- using greater than and less than
  SELECT ProductName, UnitPrice FROM Products
  WHERE UnitsInStock > 0 AND UnitPrice > 29.99;

  -- OR - One of the sides needs to be fufilled to result in true
  SELECT ProductName, UnitPrice FROM Products
  WHERE UnitsInStock > 0 OR UnitPrice > 29.99

  SELECT ProductName, UnitPrice FROM Products
  WHERE CategoryID = 2 OR CategoryID = 7;

  SELECT ProductName, UnitPrice, CategoryID FROM Products
  WHERE CategoryID = 2 OR UnitPrice < 29.99;

  -- WildCards - using with LIKE
  -- Allows more matching, it's less restrictive

  -- LIKE allows for use of wild card and not case sensitive (this is not needed for mssql)
  -- %
  -- A substitute for zero or more characters
  -- _
  -- A substitute for a single character

  SELECT ProductName
  FROM Products WHERE ProductName LIKE 'Ch%';
  -- CHAAAAA
  -- CHZZZZ
  -- CHESDKDMDKDKMD
  SELECT ProductName
  FROM Products WHERE ProductName LIKE '_H%';

  SELECT ContactName, Region FROM Customers
  WHERE Region LIKE '_A';

  -- IN very useful to look for collections
  SELECT *
  FROM Customers WHERE Region IN ('WA','SP');

  -- using between to make a range
  SELECT *
  FROM EmployeeTerritories
  WHERE TerritoryID BETWEEN 06800 AND 09999

  -- As 'value' -- allows you to change the collumn name at the output -
  SELECT EmployeeID as 'Employee Number', TerritoryID as 'Territory Identification'
  FROM EmployeeTerritories
  WHERE TerritoryID BETWEEN 06800 AND 09999;

  SELECT CompanyName AS 'Company Name',
        City + ', ' + Country AS 'City' -- contructing output from two collumn
  FROM Customers;

  SELECT CompanyName AS 'Company Name',
        City + ', ' + Country AS 'City', -- contructing output from two collumn
              Region
  FROM Customers
  WHERE Region IS NULL;

```
