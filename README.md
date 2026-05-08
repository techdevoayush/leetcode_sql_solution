# leetcode_sql_solution

# 175. Combine Two Tables

## Problem
Write an SQL query to report the first name, last name, city, and state of each person in the `Person` table.

If the address of a person is not present in the `Address` table, return `NULL` instead.

---

## Approach
- Use `LEFT JOIN` to combine `Person` and `Address` tables.
- `LEFT JOIN` ensures all records from the `Person` table are included.
- If no matching address exists, `NULL` values are returned.

---

## SQL Query

```sql
SELECT 
    P.firstName,
    P.lastName,
    A.city,
    A.state
FROM Person P
LEFT JOIN Address A
ON P.personId = A.personId;
```

---

## Key Concept

| JOIN Type | Description |
|------------|-------------|
| INNER JOIN | Returns only matching rows |
| LEFT JOIN | Returns all rows from left table |

---

## Complexity
- Time Complexity: `O(N)`
- Space Complexity: `O(1)`

---

## Learnings
- Understanding `LEFT JOIN`
- Difference between `INNER JOIN` and `LEFT JOIN`
- Using aliases in SQL
