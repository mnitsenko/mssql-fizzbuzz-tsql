# mssql-fizzbuzz-tsql
T-SQL implementation of FizzBuzz task for MS SQL

```
WITH nums AS
   (SELECT 1 AS value
    UNION ALL
    SELECT value + 1 AS value
    FROM nums
    WHERE nums.value <= 99)
SELECT 
  [value], 
  CASE 
    WHEN (([value] % 3 = 0) AND ([value] % 5 = 0)) THEN 'fizzbuzz'
    WHEN ([value] % 3 = 0) THEN 'fizz'
    WHEN ([value] % 5 = 0) THEN 'buzz'    
    ELSE '' 
  END AS [result]
FROM nums  
```

That's all, folks! =)
