```sql
---P1- Show the total population of the world.
SELECT SUM(population)
FROM world;

---P2- List all the continents - just once each.
SELECT DISTINCT (continent)
FROM world;

---P3- Give the total GDP of Africa
SELECT SUM(gdp) AS "Africa gdp"
FROM world
WHERE continent = "africa";

---P4- How many countries have an area of at least 1000000
SELECT COUNT(DISTINCT name)
FROM world
WHERE area >= 1000000;

---P5- What is the total population of ('Estonia', 'Latvia', 'Lithuania')
SELECT SUM(population)
FROM world
WHERE name IN ('Estonia', 'Latvia', 'Lithuania');

---P6- For each continent show the continent and number of countries.
SELECT continent, COUNT(DISTINCT name) AS "number of countries"
FROM world
GROUP BY continent;

---P7- For each continent show the continent and number of countries with populations of at least 10 million.
SELECT continent, COUNT(DISTINCT name) AS "number of countries"
FROM world
WHERE population >= 10000000
GROUP BY continent;

---P8- List the continents that have a total population of at least 100 million.
SELECT continent
FROM world
GROUP BY continent
HAVING SUM(population) >= 100000000;

```