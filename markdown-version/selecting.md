# Refining Selections in SQL.

### DISTINCT
This will only return the `distinct` results even if there are duplicates in the table.

```sql
SELECT DISTINCT authors from books;
```
This will result unique results no duplicates.

### ORDER BY
It allows us to sort our results.

```sql
SELECT authors from books ORDER BY last_name;

```
This will order the authors by their last name.

The order is usually ascending but you can change that by choosing descending.

```sql

SELECT authors from books ORDER BY last_name DESC;
```

### LIMIT

its basically used to limit the results and it can be used with `ORDER BY`

```sql
SELECT authors from books LIMIT 3;
```

this will only return first three results.

### LIKE

It allows you to search through your data.

```sql
SELECT author from books WHERE author LIKE '%da%'
```
this query will return all the results containing `da`/\.

if you use `'%da'` this will return results ending with `da` and `'da%'` this will return results starting with `da`.


   
