# Lab: Filter SQL queries

## Goal
Practice filtering login attempts and employee records with WHERE, AND, OR, NOT, and LIKE.

## Tables
- log_in_attempts: event_id, username, login_date, login_time, country, ip_address, success
- employees: employee_id, device_id, username, department, office

## Queries I used
#After-hours failed logins (both conditions):
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00'
AND success = FALSE;

#Logins on 2022-05-09 or the day before
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09'
OR login_date = '2022-05-08';

#Logins outside Mexico (table stores MEX and MEXICO)
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';

#Marketing employees in the East building
SELECT *
FROM employees
WHERE department = 'Marketing'
AND office LIKE 'East%';

#Finance or Sales
SELECT *
FROM employees
WHERE department = 'Finance'
OR department = 'Sales';

#Everyone except IT
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
