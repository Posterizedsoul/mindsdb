# `#!sql DROP PREDICTOR` Statement

## Description

The `#!sql DROP PREDICTOR` statement deletes the model table.

## Syntax

Here is the syntax:

```sql
DROP PREDICTOR [predictor_name];
```

On execution, we get:

```sql
Query OK, 0 rows affected (0.058 sec)
```

Where:

| Name               | Description                      |
| ------------------ | -------------------------------- |
| `[predictor_name]` | Name of the model to be deleted. |

## Example

Let's list all the available predictor tables.

```sql
SELECT name
FROM mindsdb.predictors;
```

On execution, we get:

```sql
+---------------------+
| name                |
+---------------------+
| other_model         |
| home_rentals_model  |
+---------------------+
```

Now we delete the `home_rentals_model` table.

```sql
DROP PREDICTOR home_rentals_model;
```

On execution, we get:

```sql
Query OK, 0 rows affected (0.058 sec)
```

We can check if the deletion was successful by querying the `mindsdb.predictors` table again.

```sql
SELECT name
FROM mindsdb.predictors;
```

On execution, we get:

```sql
+---------------------+
| name                |
+---------------------+
| other_model         |
+---------------------+
```
