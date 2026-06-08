```sql
-- Problem1: Modify it to show the population of Germany

SELECT population
FROM world
WHERE name='Germany';

<p>Problem1 result</p>

![Problem1 result](/Images/SQL/SQLZoo/SELECT_basics_1.jpg)


-- Problem2: Show the name and the population for 'Sweden', 'Norway' and 'Denmark'.

SELECT name, population
FROM world
WHERE name IN ('Sweden', 'Norway', 'Denmark');


-- Problem3: show the country and the area for countries with an area between 200,000 and 250,000.

SELECT name, area
FROM world
WHERE area BETWEEN 200000 AND 250000;
```

<p>Problem1 result</p>

![Problem1 result](/Images/SQL/SQLZoo/SELECT_basics_1.jpg)
