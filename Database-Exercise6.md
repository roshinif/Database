# Week 5
# Exercise 6


## Task 1
SELECT MAX(elevation_ft) FROM airport;
![img_4.png](img_4.png)

## Task 2
SELECT continent, COUNT(*) FROM country GROUP BY continent;
![img_5.png](img_5.png)

## Task 3
SELECT game.screen_name, COUNT(*) FROM game JOIN goal_reached ON game.id = goal_reached.game_id JOIN goal ON goal.id = goal_reached.goal_id GROUP BY game.screen_name;
![img_6.png](img_6.png)

## Task 4
SELECT game.screen_name FROM game WHERE co2_consumed = ( SELECT MIN(co2_consumed) FROM game );
![img_7.png](img_7.png)

## Task 5
SELECT country.name, COUNT(airport.ident) AS COUNT FROM country JOIN airport ON country.iso_country = airport.iso_country GROUP BY country.name ORDER BY COUNT DESC LIMIT 50;
![img_8.png](img_8.png)

## Task 6
SELECT country.name FROM country JOIN airport ON country.iso_country = airport.iso_country GROUP BY country.name HAVING COUNT(airport.iso_country) > 1000;
![img_9.png](img_9.png)

## Task 7
SELECT airport.name FROM airport WHERE elevation_ft = ( SELECT MAX(elevation_ft) FROM airport );
![img_10.png](img_10.png)

## Task 8
SELECT country.name FROM country JOIN airport ON country.iso_country = airport.iso_country WHERE airport.elevation_ft = ( SELECT MAX(elevation_ft) FROM airport );

![img_11.png](img_11.png)

## Task 9
SELECT COUNT(*) FROM game JOIN goal_reached ON game.id = goal_reached.game_id JOIN goal ON goal.id = goal_reached.goal_id WHERE game.screen_name = "Vesa";

![img_12.png](img_12.png)

## Task 10
SELECT name FROM airport WHERE ABS(latitude_deg) = ( SELECT MAX(ABS(latitude_deg)) FROM airport );
![img_13.png](img_13.png)

