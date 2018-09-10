#### world

`name         | continent | area    | population | gdp`<br/>
`Afghanistan  | Asia      | 652230  | 25500100   | 20343000000`<br/>
`Albania      | Europe    | 28748   | 2831741    | 12960000000`<br/>
`Algeria      | Africa    | 2381741 | 37100000   | 188681000000`<br/>
`Andorra      | Europe    | 468     | 78115      | 3712000000`<br/>
`Angola       | Africa    | 1246700 | 20609294   | 100990000000`<br/>

1. List each country name where the population is larger than that of 'Russia'.
* SELECT name FROM world WHERE population > (SELECT population FROM world WHERE name='Russia')

2. Show the countries in Europe with a per capita GDP greater than 'United Kingdom'.
* SELECT name FROM world WHERE continent = 'Europe' AND gdp/population > (SELECT gdp/population FROM world WHERE name='United Kingdom')

3. List the name and continent of countries in the continents containing either Argentina or Australia. Order by name of the country.
* (not working) SELECT name, continent FROM world WHERE continent = (SELECT continent FROM world WHERE name = 'Argentina') OR (SELECT continent FROM world WHERE name = 'Australia')

4. Which country has a population that is more than Canada but less than Poland? Show the name and the population.
* SELECT name, population FROM world WHERE population > (SELECT population FROM world WHERE name = 'Canada') AND population < (SELECT population FROM world WHERE name = 'Poland')

5. 