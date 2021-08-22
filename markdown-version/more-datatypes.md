## Few More Data Types.


### CHAR and VARCHAR

- They both store text but `CHAR` has a fixed length which you declare and you cannot do more than 255
- `CHAR` is faster for fixed length text. For example STATE, YES/NO Flags. 


### DECIMAL

```sql
CREATE TABLE items(
  price DECIMAL(5,3)
)

```

- In the query above we specified price column is going to take Decimal upto 5 digits with three  places such as `54.984`


### Float & Double

- Float and Double data types are floating point types and calculations are approximate.
