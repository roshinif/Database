# Week 03
# Exercise 03

## Task 01
SELECT country.name AS "country name", airport.name AS "airport name" FROM country JOIN airport ON country.iso_country = airport.iso_country WHERE country.name = "Iceland";
![img_32.png](img_32.png)

## Task 02
SELECT airport.name AS "airport name" FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE country.name = "France" AND airport.type = "large_airport";
![img_33.png](img_33.png)

## Task 03
SELECT country.name AS "country_name", airport.name AS "airport_name" FROM country JOIN airport ON country.iso_country = airport.iso_country WHERE country.continent = "AN";
![img_34.png](img_34.png)

## Task 04
SELECT airport.elevation_ft FROM airport JOIN game ON airport.ident = game.location WHERE game.screen_name = "Heini";
![img_35.png](img_35.png)

## Task 05
SELECT airport.elevation_ft * 0.3048 AS "elevation_m" FROM airport JOIN game ON airport.ident = game.location WHERE game.screen_name = "Heini"
![img_36.png](img_36.png)

## Task 06
SELECT airport.name FROM airport JOIN game ON airport.ident = game.location WHERE game.screen_name = "Ilkka";
![img_37.png](img_37.png)

## Task 07
SELECT country.name FROM country JOIN airport ON airport.iso_country = country.iso_country JOIN game ON airport.ident = game.location WHERE game.screen_name = "Ilkka";
![img_38.png](img_38.png)

## Task 08
SELECT goal.name FROM goal_reached INNER JOIN goal ON goal_reached.goal_id = goal.id INNER JOIN game ON goal_reached.game_id = game.id WHERE game.screen_name = "Heini";
![img_39.png](img_39.png)

## Task 09
SELECT airport.name FROM goal_reached INNER JOIN goal ON goal_reached.goal_id = goal.id INNER JOIN game ON goal_reached.game_id = game.id INNER JOIN airport ON airport.ident = game.location WHERE game.screen_name = "Ilkka" AND goal.name = "CLOUDS";
![img_40.png](img_40.png)

## Task 10
SELECT country.name FROM goal_reached INNER JOIN goal ON goal_reached.goal_id = goal.id INNER JOIN game ON goal_reached.game_id = game.id INNER JOIN airport ON airport.ident = game.location INNER JOIN country ON country.iso_country = airport.iso_country WHERE game.screen_name = "Ilkka" AND goal.name = "CLOUDS";
![img_41.png](img_41.png)
