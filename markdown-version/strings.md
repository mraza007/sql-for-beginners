# String Functions in SQL Database.


### CONCAT
(Combine Data For Cleaner Output).

In order to CONCAT two columns together you can use `CONCAT`

```sql
SELECT
  CONCAT(first_name, ' ', last_name) AS 'fullname'
FROM employees;
```
##### CONCAT_WS -> CONCAT with separator
This allows you to add a separator instead of just typing everytime when using `CONCAT`

```sql
SELECT
  CONCAT_WS('-',first_name,last_name)
FROM employees;
```

### SUBSTRING
Working with parts of the strings for example you just needfirst 10 characters of the string.

_note: index starts at 1 in SQL_


```sql

SELECT SUBSTRING('Hello World',1,5)

SELECT SUBSTRING(title,1,10) AS short_title from books;

```

You can also use `SUBSTR()` instead of `SUBSTRING`


### REPLACE

You can use replace if you want to replace strings in sql

```sql
SELECT REPLACE(<column>,<What you are trying to replace> ,<With what you want to replace>) from <table>;

SELECT REPLACE(title,'e','3') from books;
```

In the example above I am replacing `e` with `3` in `title` column


### REVERSE 
It allows you to reverse a string

```sql
SELECT REVERSE(<col_name>) from <table>

SELECT REVERSE(title) from books;
```

### CHAR_LENGTH

Counts characters in a string

```sql

SELECT CHAR_LENGTH(<col_name>) from <table>

SELECT CHAR_LENGTH(title) from books;
```

### LOWER & UPPER

UPPER --> allows you to uppercase a word
LOWER --> allows you to lowercase a word

```sql

SELECT UPPER(title) from books;

SELECT LOWER(title) from books;
```
