# sql-exercises.sql
-- SQL Exercises – Data Analyst Journey

-- 1. Orders per country
SELECT country, COUNT(*)
FROM orders
GROUP BY country;

-- 2. Revenue per country
SELECT country, SUM(amount)
FROM orders
GROUP BY country;

-- 3. Top customer by spending
SELECT customer, SUM(amount) AS total_spent
FROM orders
GROUP BY customer
ORDER BY total_spent DESC;
