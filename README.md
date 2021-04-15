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
  SELECT name FROM world
    WHERE name LIKE '%x%'
```
#### 4. Find the countries that end with "land"
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE '%land'
```
#### 5. Find the countries that start with "C" and end with "ia"
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE 'c%ia'
```
#### 6. Find the country that has oo in the name
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE '%oo%'
```
#### 7. Find the countries that have three or more a in the name
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE '%a%a%a%'
```
#### 8. Find the countries that have "t" as the second character
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE '_t%'
```
#### 9. Find the countries that have two "o" characters separated by two others
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE '%o__o%'
```
#### 10. Find the countries that have exactly four characters.
```SQL
  SELECT name 
  FROM world
    WHERE name LIKE '____'
```
### Harder Questions
The next questions are optional and only for students who are finding the basic questions too easy.
#### 11. Find the country where the name is the capital city
```SQL
  SELECT name 
  FROM world
    WHERE name=capital
```
#### 12. Find the country where the capital is the country plus "City"
```SQL
  SELECT name 
  FROM world
    WHERE capital = concat(name, ' City')
```
#### 13. Find the capital and the name where the capital includes the name of the country
```SQL
  SELECT capital, name
  FROM world
    WHERE capital LIKE concat('%', name, '%')
```
#### 14. Find the capital and the name where the capital is an extension of name of the country
```SQL
  SELECT capital, name
  FROM world
    WHERE capital LIKE concat('%', name, '%') AND 
          capital<>name
```
#### 15. Show the name and the extension where the capital is an extension of name of the country
```SQL
  SELECT capital, name, REPLACE(capital, name, '') AS extension
  FROM world
    WHERE capital LIKE concat('%', name, '%') AND 
          capital<>name
```
