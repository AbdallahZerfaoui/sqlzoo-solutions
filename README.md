# sqlzoo-solutions
I will compile here the solutions of all the levels on the SQLZOO Tutoral.

# Table of contents
1. [SELECT basics](#SELECT_basics)
## SELECT basics <a name="SELECT_basics"></a>
We are going to use a table called World for the next exercices.
#### 1. show the population of Germany
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 2. Show the name and the population for 'Sweden', 'Norway' and 'Denmark'
```SQL
  SELECT name, population 
  FROM world
    WHERE name IN ('Sweden', 'Norway', 'Denmark')
```
#### 3. Just the right size
```SQL
  SELECT name, area 
  FROM world
    WHERE area BETWEEN 2e5 AND 25e4
```

