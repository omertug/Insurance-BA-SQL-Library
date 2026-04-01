**Monthly GWP Trend / Aylık Brüt Prim Üretimi:**
```sql
    SELECT TO_CHAR(start_date, 'YYYY-MM') AS period, SUM(premium) AS total_premium
    FROM D_POLICY
    WHERE status = 'Active'
    GROUP BY period ORDER BY period;
