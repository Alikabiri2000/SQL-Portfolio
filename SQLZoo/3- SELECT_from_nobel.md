```sql

-- P1- Change the query shown so that it displays Nobel prizes for 1950.
SELECT yr, subject, winner
  FROM nobel
 WHERE yr = 1950;

-- P2- Show who won the 1962 prize for literature.
SELECT winner
  FROM nobel
 WHERE yr = 1962
   AND subject = 'literature';

-- P3- Show the year and subject that won 'Albert Einstein' his prize.
SELECT yr, subject
FROM nobel
WHERE winner = 'albert einstein';

-- P4- Give the name of the 'Peace' winners since the year 2000, including 2000.
SELECT winner
FROM nobel
WHERE subject = 'peace'
AND yr >= 2000;

-- P5- Show all details (yr, subject, winner) of the literature prize winners for 1980 to 1989 inclusive.
SELECT yr, subject, winner
FROM nobel
WHERE yr >= 1980
AND yr <=1989
AND subject = 'literature';

-- P6- Show all details of the presidential winners:
-- Theodore Roosevelt
-- Thomas Woodrow Wilson
-- Jimmy Carter
-- Barack Obama
SELECT *
FROM nobel
WHERE winner IN ('Theodore Roosevelt',
'Thomas Woodrow Wilson',
'Jimmy Carter',
'Barack Obama');

-- P7- Show the winners with first name John
SELECT winner
FROM nobel
WHERE winner LIKE ('john%');

-- P8- Show the year, subject, and name of physics winners for 1980 together with the chemistry winners for 1984.
SELECT *
FROM nobel
WHERE subject = 'physics' AND yr = 1980
OR subject = 'chemistry' AND yr = 1984;

-- P9- Show the year, subject, and name of winners for 1980 excluding chemistry and medicine
SELECT *
FROM nobel
WHERE yr = 1980
AND subject != 'chemistry'
AND subject != 'medicine';

-- P10- Show year, subject, and name of people who won a 'Medicine' prize in an early year (before 1910, not including 1910) together with winners of a 'Literature' prize in a later year (after 2004, including 2004)
SELECT *
FROM nobel
WHERE (subject = 'medicine' AND yr < 1910)
OR (subject = 'literature' AND yr >= 2004);

-- P11- Find all details of the prize won by PETER GRÜNBERG
SELECT *
FROM nobel
WHERE winner = 'PETER GRÜNBERG';

-- P12- Find all details of the prize won by EUGENE O'NEILL
SELECT *
FROM nobel
WHERE winner = "EUGENE O'NEILL";

-- P13- List the winners, year and subject where the winner starts with Sir. Show the the most recent first, then by name order.
SELECT winner, yr, subject
FROM nobel
WHERE winner LIKE ('Sir%')
ORDER BY yr DESC, winner;

-- P14- Show the 1984 winners and subject ordered by subject and winner name; but list chemistry and physics last.
SELECT winner, subject
FROM nobel
WHERE yr = 1984
ORDER BY subject IN ('chemistry', 'physics'), subject, winner;

```

<p>
  P1 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_1.png">

<p>
  P2 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_2.png">

<p>
  P3 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_3.png">

<p>
  P4 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_4.png">

<p>
  P5 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_5.png">

<p>
  P6 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_6.png">

<p>
  P7 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_7.png">

<p>
  P8 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_8.png">

<p>
  P9 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_9.png">

<p>
  P10 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_10.png">

<p>
  P11 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_11.png">

<p>
  P12 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_12.png">

<p>
  P13 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_13.png">

<p>
  P14 result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_14.png">

<p>
  SELECT from nobel quiz result</p>
<img src="/Images/SQL/1-SQLZoo/3-SELECT_from_nobel_quiz.png">