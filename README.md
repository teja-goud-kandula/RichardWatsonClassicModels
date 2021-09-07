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
