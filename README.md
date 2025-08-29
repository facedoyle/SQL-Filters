# SQL-Filters# Apply filters to SQL queries

## Project description  
This project investigates potential security incidents and employee machine updates using SQL queries. Filters were applied to the `log_in_attempts` and `employees` tables to identify failed logins after business hours, logins on specific dates, and logins originating outside of Mexico. Additional queries retrieved employees in specific departments and office locations to support IT and security updates. The objective was to demonstrate how SQL filters can be used to extract relevant data for analysis and operational decision-making.  

---

## Retrieve after hours failed login attempts  

**Query:**  
```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00:00'
  AND success = 0;
