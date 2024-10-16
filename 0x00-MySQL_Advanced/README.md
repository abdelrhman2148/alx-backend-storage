# 0x00. MySQL Advanced

This repository contains advanced SQL tasks that demonstrate proficiency in working with MySQL. Each task focuses on a specific aspect of database management, optimization, and stored procedures. The goal is to optimize queries, work with indexes, views, and stored procedures, and implement efficient SQL solutions.

## Requirements
- MySQL 5.7 (or higher)
- Understanding of database optimization
- Basic knowledge of indexing, stored procedures, and views

## Table of Contents

### Task 0: My privileges!

- **File:** `0-privileges.sql`
- **Description:** Write a SQL script that lists all privileges of the MySQL users `root` and `mysql.session`.

---

### Task 1: Root user

- **File:** `1-create_user.sql`
- **Description:** Write a SQL script that creates the MySQL user `root` with password `root_password`.

---

### Task 2: Read user

- **File:** `2-create_read_user.sql`
- **Description:** Write a SQL script that creates a MySQL user `read_user` and grants read access to the `holberton` database.

---

### Task 3: Always a name

- **File:** `3-force_name.sql`
- **Description:** Write a SQL script that ensures the `name` column in the `users` table cannot be `NULL`.

---

### Task 4: ID can't be null

- **File:** `4-id_not_null.sql`
- **Description:** Write a SQL script that ensures the `id` column in the `users` table is not nullable.

---

### Task 5: Unique ID

- **File:** `5-unique_id.sql`
- **Description:** Write a SQL script that creates a unique index on the `id` column of the `users` table.

---

### Task 6: States table

- **File:** `6-states.sql`
- **Description:** Write a SQL script that creates a table `states` with an auto-incrementing `id` and `name` column.

---

### Task 7: Cities table

- **File:** `7-cities.sql`
- **Description:** Write a SQL script that creates a table `cities` with an auto-incrementing `id`, `name`, and a foreign key referencing the `states` table.

---

### Task 8: Optimize simple search

- **File:** `8-index_my_names.sql`
- **Description:** Write a SQL script that creates an index on the first letter of the `name` column in the `names` table.

Example:
```bash
mysql> SELECT COUNT(name) FROM names WHERE name LIKE 'a%';
+-------------+
| COUNT(name) |
+-------------+
|      302936 |
+-------------+
1 row in set (2.19 sec)

mysql> SHOW INDEX FROM names;
+----------------+------------+----------------+--------------+
| Table          | Non_unique | Key_name       | Seq_in_index |
+----------------+------------+----------------+--------------+
| names          |          1 | idx_name_first |            1 |
+----------------+------------+----------------+--------------+
```

---

### Task 9: Optimize search and score

- **File:** `9-index_name_score.sql`
- **Description:** Write a SQL script that creates an index on both the first letter of `name` and the `score` column.

Example:
```bash
mysql> SELECT COUNT(name) FROM names WHERE name LIKE 'a%' AND score < 80;
+-------------+
| COUNT(name) |
+-------------+
|       60717 |
+-------------+
1 row in set (2.40 sec)

mysql> SHOW INDEX FROM names;
+----------------------------+------------+----------------------+--------------+
| Table                      | Non_unique | Key_name             | Seq_in_index |
+----------------------------+------------+----------------------+--------------+
| names                      |          1 | idx_name_first_score |            1 |
+----------------------------+------------+----------------------+--------------+
```

---

### Task 10: Safe divide

- **File:** `10-div.sql`
- **Description:** Write a SQL script that creates a function `SafeDiv` to safely divide two numbers, returning `0` when the divisor is `0`.

Example:
```bash
mysql> SELECT SafeDiv(a, b) FROM numbers;
+----------------------+
| SafeDiv(a, b)        |
+----------------------+
| 5                    |
| 0.800000011920929     |
| 0.6666666865348816    |
| 2                    |
| 0                    |
+----------------------+
```

---

### Task 11: No table for a meeting

- **File:** `11-need_meeting.sql`
- **Description:** Write a SQL script that creates a view `need_meeting` listing students with a score under 80 and no `last_meeting` or a meeting more than one month ago.

---

### Task 12: Average weighted score

- **File:** `100-average_weighted_score.sql`
- **Description:** Write a SQL script that creates a stored procedure `ComputeAverageWeightedScoreForUser` to calculate and store the average weighted score for a user.

---

### Task 13: Average weighted score for all!

- **File:** `101-average_weighted_score.sql`
- **Description:** Write a SQL script that creates a stored procedure `ComputeAverageWeightedScoreForUsers` to calculate and store the average weighted score for all users.

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/alx-backend-storage.git
   ```

2. Navigate to the project directory:
   ```bash
   cd alx-backend-storage/0x00-MySQL_Advanced
   ```

3. Import the required `.sql` files:
   ```bash
   mysql -uroot -p < 8-index_my_names.sql
   ```

4. Run each script as needed to test functionality and optimize queries.

---

## Author
Abdelrhman Fikri Elrhmany
