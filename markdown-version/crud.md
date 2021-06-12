CRUD(CREATE, READ, UPDATE, DELETE)

# READ
How do we retrieve and search data from the database. We use `SELECT` command.

- `SELECT * FROM <table>` means display all the elements from the table.

#### `SELECT` Expression
Its a way of defining what columns do you need when selecting data from the tables.

For example you can do `SELECT <column> from <table>` or 
`SELECT <column_1>,<column_2> from <table>`.

#### `WHERE` clause.
It allows you run more specialized query with specific requirement. This is useful when looking for specific data.

```sql
SELECT * FROM <table> WHERE condition
```
For Example,

```sql
SELECT * FROM employees WHERE age=25
```

This will list results where employee age is 25

_NOTE: String in Where Clause is usually case sensitive_

#### Aliases

Aliases allow us to give an alternative name to our column name.

```sql
SELECT <column> AS <alias> from <table>
```
Note: When using Alias the original column name doesn't change

#### UPDATE

How do we alter data in SQL Database

```sql
UPDATE <table> SET <element>='<something>'
WHERE <element>=`<where we want to change>`

```
For example 

```sql
UPDATE employee SET status='left'
WHERE status="newhire"
```

_Note: When updating try selecting the data first you want change_


#### DELETE
How to delete in SQL Database.

```sql
DELETE FROM employee WHERE name='john'
```

