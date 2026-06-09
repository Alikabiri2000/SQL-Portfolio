```sql
-- Problem1: Modify it to show the population of Germany
SELECT population
FROM world
WHERE name='Germany';

-- P2: Show the name and the population for 'Sweden', 'Norway' and 'Denmark'.
SELECT name, population
FROM world
WHERE name IN ('Sweden', 'Norway', 'Denmark');

-- P3: show the country and the area for countries with an area between 200,000 and 250,000.
SELECT name, area
FROM world
WHERE area BETWEEN 200000 AND 250000;
```
<p>
  P1 result</p>
<img src="/Images/SQL/SQLZoo/SELECT_basics_1.jpg">

<p>
  P2 result</p>
<img src="/Images/SQL/SQLZoo/SELECT_basics_2.jpg">

<p>P3 result</p>
<img src="/Images/SQL/SQLZoo/SELECT_basics_3.jpg">
