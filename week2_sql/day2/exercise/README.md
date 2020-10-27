Question 1 - How many employees have a home City of London?
- 6
```sql
SELECT COUNT(City) FROM Customers WHERE City = 'London'
```

Question 2 - Which Employee is a Doctor?
- Andrew Fuller
```sql
SELECT TitleOfCourtesy, FirstName, LastName FROM Employees WHERE TitleOfCourtesy = 'Dr.'
```

Question 3 - How many Products are discontinued?
- 77
```sql
SELECT COUNT(Discontinued) FROM Products 
```

Question 4 - What are the names and product IDs of the products with a unit price below 5.00
- Guarana Fantastica 24
- Geitost 33
```sql
SELECT ProductName, ProductID FROM Products WHERE UnitPrice < 5.00
```

Question 5 - Which categories have a category name with initials beginning with B or S?
- Beverages
- Seafood
```sql
SELECT CategoryID, CategoryName FROM Categories WHERE CategoryName LIKE 'B%' OR CategoryName LIKE 'S%';
```

Question 6 - How many orders are there for Employee IDs 5 and 7 (The total for both)
- 114
```sql
SELECT COUNT(OrderID) FROM Orders WHERE EmployeeID = 7 OR EmployeeID = 5
SELECT COUNT(OrderID) FROM Orders WHERE EmployeeID IN(5,7);
```

Question 7 - Write a SELECT using the Employees table and concatenate First Name and Last Name together. Using a column alias
to rename the column to Employee Name
```sql
SELECT FirstName + ' ' + LastName AS 'Employee Name' FROM Employees;
```

Question 8 - Write a SELECT statement to list the 6 countries that have Region Codes in the Customers Table
- Brazil
- Canada
- Ireland
- UK
- USA
- Venezuela
```sql
SELECT DISTINCT Country FROM Customers WHERE Region != 'NULL';
```


