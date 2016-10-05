# Lecture 3 (03/10/2016)

## Joins

There are multiple ways of joining relations

### Cross join

The cross product is formed between the tuples of each table (not very useful):

```sql
SELECT *
FROM employee, projectemps
```

Another syntax:

```sql
SELECT *
FROM employee CROSS JOIN projectemps
```

### Inner join

We restrict ourselves to tuples that are related to each other:

```sql
SELECT employee.lname
FROM employee, projectemps
WHERE employee.empID = projectemps.empID
```

Another syntax:

```sql
SELECT employee.lname
FROM employee INNER JOIN projectemps
ON employee.empID = projectemps.empID
```

### Natural join

In the case where the relations to be joined have a common attribute name (and types), the natural join can be used (however pay attention to multiple common attributes).

```sql
SELECT employee.lname
FROM employee NATURAL JOIN projectemps
```

### Left join

The left join performs a join on two relations and then adds tuples from the left relation to the result if they were not already in the result.

```sql
SELECT project.projectName, project.projectLeader
project LEFT JOIN projectemps
ON project.projectID = projectemps.projectID;
```

### Right join

Same as left join (just right).

### Full outer join

The full outer join combines the results of the left and right joins.

## Set operations

Queries can be combined using the set operations UNION, INTERSECT and EXCEPT, provided they are 'union-compatible' (same number of attributes, in the same order, and with the same data types).

See examples in `DBL1b.pdf` in the `material` directory.

## Subqueries


