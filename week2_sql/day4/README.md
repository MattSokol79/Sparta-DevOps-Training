# Day 4 - Finishing JOINs and Subqueries

```sql
SELECT 
    OrderID,
    CONVERT(VARCHAR(10), OrderDate, 103)
FROM Orders; -- Before 2012

SELECT
    OrderID,
    FORMAT(OrderDate, 'dd/MM/yyyy')
FROM Orders; -- After 2012
```

## Subequeries
- A subequery is a nested query inside another SELECT statement.
- This allows you to take the results of one query and apply them to another query.

A subquery may occur in any of the following clauses
1. SELECT (nested subquery - returns single value only)
2. FROM (inline view)
3. WHERE (nested subquery)


**Below is an example of a subquery in the WHERE clause. PURPOSE is to check to see which Customers have not places any orders. This could also be achieved using JOINs.**
```sql
SELECT CompanyName AS 'Customer'
FROM Customers
WHERE CustomerID NOT IN
    (SELECT CustomerID FROM Orders)
```
**Below is an example of a nested subquery in the SELECT clause (acts like a column). Subqueries MUST be contained by parenthesis (excluding any alias). Outputs the highest price in the table on every row in the result set.**
```sql
SELECT 
    OrderID,
    ProductID,
    UnitPrice,
    Quantity,
    Discount,
    (SELECT MAX(UnitPrice) FROM [Order Details] od) AS 'Max Price'
FROM [Order Details]
```

**This is an example of an inline view (SELECT in the FROM clause: acts like a table). The inline view sq1 calculates the total for each product which is used to calculate percent of total. This is quite an advanced query. In SSMS highlight part of the query and press F5 to Exxecute/test part of your code.**
```sql
SELECT 
    od.ProductID,
    sq1.totalamt AS 'Total Sold for this Product',
    UnitPrice,
    UnitPrice/totalamt*100 AS '% of Total'
FROM [Order Details] od
    INNER JOIN 
        (SELECT ProductID, 
            SUM(UnitPrice*Quantity) AS totalamt
        FROM [Order Details]
        GROUP BY ProductID) sq1 ON sq1.ProductID = od.ProductID
```

