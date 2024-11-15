# lab11.sql
-- 1. Display all records from courses table
SELECT * FROM courses;

-- 2. Display the first 10 records from assignments table
SELECT * FROM assignments LIMIT 10;

-- 3. Count the number of courses
SELECT count(*) FROM courses;

-- 4. Find the earliest due date in assignments
SELECT min(due_date) FROM assignments;

-- 5. Display courses with names that start with "Intro"
SELECT * FROM courses WHERE course_name LIKE 'Intro%';

-- 6. Display assignments that are not completed, sorted by due_date
SELECT * FROM assignments WHERE status != 'Completed' ORDER BY due_date;

-- 7. Display specific fields for assignments in COMM courses due before 2025
SELECT course_id, title, status, due_date
FROM assignments
WHERE status != 'Completed'
  AND course_id LIKE 'COMM%'
  AND due_date < '2024-12-31'
ORDER BY due_date;
