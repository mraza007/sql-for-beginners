# Inserting Data in `SQL` Database

In this we will be focusing mostly on `INSERT` basically adding the data to the tables.

To add data in the tables we can using the following command 

```sql
INSERT INTO <table_name>(<column_name>) VALUES (<value>)`;
```

#### For Example 

In order to add data in our `cats` table we might do the following
```sql
INSERT INTO cats (name,age) VALUES ('tom',3);
```

#### How to check if the command worked

In order to see if the values were added to the table you can use the following command 

```sql
SELECT * FROM cats;
```
```sh
MariaDB [colt_test]> select * from cats;
+-------+------+
| name  | age  |
+-------+------+
| tom   |    3 |
| jerry |    5 |
| jax   |    4 |
| kate  |    4 |
+-------+------+
4 rows in set (0.001 sec)
```



## Multiple INSERT

In order to the bulk insert in the table you can do the following command

```sql
INSERT INTO cats (name,age)
VALUES ('jerry',5)
      ,('jax',4)
      ,('kate',4)
```

```sh
MariaDB [colt_test]> select * from cats;
+-------+------+
| name  | age  |
+-------+------+
| tom   |    3 |
| jerry |    5 |
| jax   |    4 |
| kate  |    4 |
+-------+------+
4 rows in set (0.001 sec)

```

_Note: Use SHOW WARNINGS; to see the warning_

### NULL and NOT NULL
- `NULL` means the value is unknown and it doesn't means its ZERO.
- `NOT NULL` is something we specify when we define a table.This means that `NULL` values won't be permitted. Its a way of requiring things

### Default Values

```sql
CREATE TABLE cats
(
  name VARCHAR(100) DEFAULT 'unknown'
  age INT DEFAULT 99
)
```
## Primary Keys (Unique Identifier)

- We add unique identifiers to make row unique.

```sql
CREATE table uniq_cats(name VARCHAR(32),
                       age INT,
                       cat_id INT NOT NULL,
                       PRIMARY KEY(cat_id))
```

```sql
INSERT into uniq_cats(name,age,cat_id)
VALUES('tom',12,1)
```
- Primary keys stops you from adding duplicate entries
- use `AUTO_INCREMENT` SQL for uniq ids
-
