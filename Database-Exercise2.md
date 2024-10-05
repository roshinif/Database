# Week 3
# Exercise 2


## Task 1
SELECT * FROM goal;
![img_42.png](img_42.png)

## Task 2
SELECT name, type FROM airport WHERE iso_country = "FI";
![img_43.png](img_43.png)

## Task 3
SELECT name FROM airport WHERE iso_country = 'FI' ORDER BY name ASC;
![img_44.png](img_44.png)

## Task 4
SELECT name, type FROM airport WHERE iso_country = 'FI' ORDER BY type ASC, name ASC;
![img_45.png](img_45.png)

## Task 5
SELECT name FROM country WHERE name LIKE "F%";

![img_46.png](img_46.png)

## Task 6
SELECT name FROM country WHERE name LIKE "%F%";
![img_47.png](img_47.png)

## Task 7
SELECT location FROM game WHERE screen_name = "Vesa";

![img_48.png](img_48.png)

## Task 8
SELECT co2_consumed FROM game WHERE screen_name = "Ilkka";
![img_49.png](img_49.png)

## Task 9
SELECT co2_budget FROM game LIMIT 1;
![img_50.png](img_50.png)

## Task 10
SET @co2_budget := (SELECT co2_budget FROM game WHERE screen_name = "Ilkka"); SET @co2_consumed := (SELECT co2_consumed FROM game WHERE screen_name = "Ilkka"); SELECT screen_name, @co2_budget AS co2_budget, @co2_consumed AS co2_consumed, (@co2_budget - @co2_consumed) AS co2_left FROM game WHERE screen_name = "Ilkka";
![img_51.png](img_51.png)
