## Aggregate functions in SQL

These functions allows you to combine the data and get the meaning out of it.

### Count

It allows you to count the elements for instance how many employees are there in the company.

```sql
SELECT COUNT(*) from books;
```
This will count all the books in the books table.

```
SELECT COUNT(DISTINCT authors) from books;
```   

this is going to count unique authors in the books table.

```sql
SELECT COUNT (*) from books WHERE title LIKE '%the%'
```
This will return the count of number of titles containing `the`


### GROUP BY

`GROUP BY` Summarizes identical data into single rows


```sql
SELECT authors,years, COUNT(*) from books GROUP BY years;
```

This query will count the number of books released in each year.


### MIN & MAX

`MIN` Helps you find minimum values and `MAX` helps you find maximum values

```sql
SELECT MIN(years) from books;
```

This will output when the first book was released
