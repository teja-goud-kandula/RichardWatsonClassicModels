# RichardWatsonClassicModels
Solutions to all the Richard Watson problems

# Single entity

1. Prepare a list of offices sorted by country, state, city.

SQL:
```SQL
select * from offices order by country, state, city;
```

2. How many employees are there in the company?

SQL:
```SQL
select COUNT(*) as 'Number of Employees' from employees;
```

3. What is the total of payments received?

SQL:
```SQL
select SUM(amount) as 'Total payments received'  from Payments;
```

4. List the product lines that contain 'Cars'.

SQL:
```SQL
select productLine from ProductLines where productLine like '%cars%';
```

5. Report total payments for October 28, 2004.

SQL:
```SQL
select * from Payments where date(paymentDate) = '2004-10-28';
```

6. Report those payments greater than $100,000.

SQL:
```SQL
select * from Payments where amount > 100000;
```

7. List the products in each product line.

SQL:
```SQL
select productName, productLine from products order by productLine;
```

8. How many products in each product line?

SQL:
```SQL
select  productLine, COUNT(1) as 'Number of Products' from products group by productLine;
```

9. What is the minimum payment received?

SQL:
```SQL
select MIN(amount) as 'Min amount' from Payments;
```

10. List all payments greater than twice the average payment.

SQL:
```SQL
select * from Payments where amount > ( select 2 * AVG(amount)  from Payments);
```
