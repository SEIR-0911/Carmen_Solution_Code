# Carmen_Solution_Code

Clue 1 
```
SELECT name, population FROM country WHERE region = 'Southern Europe' AND population = (SELECT MIN(population) FROM country WHERE region = 'Southern Europe'); -- Holy See Vatican City
```


Clue 2

```
SELECT language FROM countrylanguage WHERE countrycode = 'VAT'; -- Italian
```


Clue 3

```
SELECT name, language, percentage FROM country JOIN countrylanguage ON country.code = countrycode WHERE language = 'Italian' AND percentage = 100; -- San Marino (SMR)
```


Clue 4

```
SELECT city.name, countrycode FROM city JOIN country ON city.countrycode = code WHERE city.name != 'San Marino' AND city.countrycode = 'SMR'; -- Serravalle
```


Clue 5

```
SELECT country.code, country.name, country.continent FROM country JOIN city ON country.code = city.countrycode WHERE country.continent = 'South America' AND city.name iLIKE 'Serra%'; -- Brazil
```

Clue 6

```
SELECT city.name FROM city JOIN country ON city.countrycode = country.code WHERE country.name = 'Brazil' AND city.id = country.capital; -- Brasília
```

Clue 7

```
SELECT city.name, city.countrycode, city.district FROM city JOIN country ON city.countrycode = country.code WHERE city.population = 91084; -- Santa Monica, CA, USA
```



