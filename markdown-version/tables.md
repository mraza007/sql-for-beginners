# Tables in `MYSQL`

Database is just bunch of different tables and thats where our data is stored.
`MYSQL` is a relational database that stores our data in tables but not every database stores data in tables.

## What is a table? 
According to Wikipedia _a collection of related data held in a structured format within in a database_.

For example we can represent cars at dealership using a database table.

![](../images/tables.png)

As application grow large the database tables become more complex for example if you have an ecommerce store you might have tables for payments, people signing up and etc

## Data Types in `MYSQL`

In SQL we have different data types such as `Numeric Types`,`String Types` and `Date types`

#### Numeric Types
- INT
- SMALLINT
- TINYINT
- MEDIUMINT
- BIGINT
- DECIMAL
- NUMERIC
- FLOAT
- DOUBLE
- BIT

#### String Types
- CHAR
- VARCHAR
- BINARY
- VARBINARY
- BLOB
- TINYBLOB
- MEDIUMBLOB
- LONGBLOB
- TEXT
- TINYTEXT
- MEDIUMTEXT
- LONGTEXT
- ENUM

#### Dates Types
- DATA
- DATETIME
- TIMESTAMP
- TIME
- YEAR

I will mostly be focusing on `INT` and `VARCHAR`. `INT` represents a whole number and it cannot work for decimals and if we need to store numbers larger then we can look at other numeric types. `VARCHAR` is a variable length string and its used to represent strings. its usually between 1 and 255 characters and we have to specify the length when using `varchar(<length>)`

### Example `Tweets` Table with Data Types

![](../images/image-sql.png)