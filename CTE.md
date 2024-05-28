## Common Table Expressions (CTE)

Common Table Expressions (CTE), SQL'de daha karmaşık sorguları daha okunabilir ve yönetilebilir hale getirmek için kullanılan bir yapıdır. CTE'ler, sorgunun başında tanımlanan geçici sonuç kümeleridir ve ana sorgu içinde kullanılabilirler. CTE'ler, özellikle tekrar kullanılacak veya karmaşık alt sorguların anlaşılır olmasını sağlar.

CTE'ler, `WITH` anahtar kelimesiyle başlar ve adlandırılmış geçici sonuç kümeleri oluşturur. Bu geçici sonuç kümeleri, ana sorguda kullanılabilir.

### Örnekler

#### Basit CTE
- Bu örnekte, EmployeeCTE adlı bir CTE oluşturulmuş ve daha sonra bu CTE'den veri seçilmiştir.
```sql
WITH EmployeeCTE AS (
    SELECT EmployeeID, FirstName, LastName, Department
    FROM Employees
)
SELECT * FROM EmployeeCTE;
```

#### Karmaşık CTE
- Bu örnekte, SalesCTE adlı bir CTE oluşturulmuş, Sales tablosundaki toplam satış miktarlarını hesaplamış ve ardından bu sonuçlar Employees tablosu ile birleştirilmiştir.
```sql
WITH SalesCTE AS (
    SELECT EmployeeID, SUM(SalesAmount) AS TotalSales
    FROM Sales
    GROUP BY EmployeeID
)
SELECT e.FirstName, e.LastName, s.TotalSales
FROM Employees e
JOIN SalesCTE s ON e.EmployeeID = s.EmployeeID
ORDER BY s.TotalSales DESC;
```

#### Özyinelemeli CTE
```sql
WITH RecursiveCTE AS (
    SELECT EmployeeID, ManagerID, FirstName, LastName, 1 AS Level
    FROM Employees
    WHERE ManagerID IS NULL
    UNION ALL
    SELECT e.EmployeeID, e.ManagerID, e.FirstName, e.LastName, r.Level + 1
    FROM Employees e
    INNER JOIN RecursiveCTE r ON e.ManagerID = r.EmployeeID
)
SELECT * FROM RecursiveCTE;
```

