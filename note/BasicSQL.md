# Query SQL

## Basic
```sql
SELECT <columns>
FROM <tbl>;
```

## Distinct
```sql
SELECT DISTINCT name, num_dogs
FROM Person;
```
## Where
```sql
SELECT DISTINCT name, num_dogs
FROM Person;
WHERE num_dogs > 10
```
### like
```sql
SELECT DISTINCT name, num_dogs
FROM Person;
WHERE name LIKE 'haha%'
```

### And/Or
```sql
SELECT name, num_dogs
FROM Person
WHERE age >= 18 (AND/OR) num_dogs > 3;
```

## Limit
```sql
SELECT name, num_dogs
FROM Person
LIMIT 5;
```
```sql
SELECT name, num_dogs
FROM Person
LIMIT 5, 5;
```

## Group by
```sql
SELECT name, count(*) as nums
FROM Person
GROUP BY name;
```

### Having
```sql
SELECT name, count(*) as nums
FROM Person
GROUP BY name
Having count(*) > 1;
```

## Order by
```sql
SELECT name, num_dogs
FROM Person
ORDER BY name desc, num_dogs;
```

