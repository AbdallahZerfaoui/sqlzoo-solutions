# sqlzoo-solutions
I will compile here the solutions of all the levels on the SQLZOO Tutoral.

# Table of contents
1. [SELECT basics](#SELECT_basics)
2. [SELECT names](#SELECT_names)
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
## SELECT names <a name="SELECT_names"></a>

#### 1. Find the country that start with Y
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE 'Y%'
 ```
    
#### 2. Find the countries that end with y
```SQL
  SELECT name FROM world
    WHERE name LIKE '%Y'
```
#### 3. Find the countries that contain the letter x
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 4. Find the countries that end with "land"
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 5. Find the countries that start with "C" and end with "ia"
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 6. Find the country that has oo in the name
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 7. Find the countries that have three or more a in the name
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 8. Find the countries that have "t" as the second character
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 9. Find the countries that have two "o" characters separated by two others
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 10. Find the countries that have exactly four characters.
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
### Harder Questions
The next questions are optional and only for students who are finding the basic questions too easy.
#### 11. Find the country where the name is the capital city
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 12. Find the country where the capital is the country plus "City"
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 13. Find the capital and the name where the capital includes the name of the country
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 14. Find the capital and the name where the capital is an extension of name of the country
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
#### 15. Show the name and the extension where the capital is an extension of name of the country
```SQL
  SELECT population 
  FROM world
    WHERE name = 'Germany'
```
