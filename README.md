# Metropolia Databases 1 (by Artur Roos)

## Week 1 

### Exercises 1



## Week 2

## Week 3

### Exercises 2

1.  `select * from goal`

![](3_2_01.jpg)

2.  `select name,type from airport where iso_country = "FI"`

![](3_2_02.jpg)

3.  `select name from airport where iso_country = "FI" order by name`

![](3_2_03.jpg)

4.  `select name,type from airport where iso_country = "FI" order by type,name`

![](3_2_04.jpg)

5.  `select name from country where name like "F%"`

![](3_2_05.jpg)

6.  `select name from country where name like "%f%"`

![](3_2_06.jpg)

7.  `select location from game where screen_name = "Vesa"`

![](3_2_07.jpg)

8.  `select co2_consumed from game where screen_name = "Ilkka"`

![](3_2_08.jpg)

9.  `select co2_budget from game limit 1`

![](3_2_09.jpg)

10. `select screen_name,co2_budget,co2_consumed,(co2_budget - co2_consumed) as co2_left from game where screen_name = "Ilkka"`

![](3_2_10.jpg)


### Exercises 3

1. `select country.name as "country name", airport.name as "airport name" from airport inner join country on airport.iso_country = country.iso_country where country.name = 'Iceland' order by airport.name`

![](3_3_01.jpg)

2. `select airport.name from airport
    inner join country on airport.iso_country = country.iso_country
                    where country.name = "France" and airport.type = "large_airport"`

![](3_3_02.jpg)

3. `select ("Antarctica") as "country_name",name as "airport_name" from airport where continent = "an" order by name`

![](3_3_03.jpg)

4. `select elevation_ft from game inner join airport on game.location = airport.ident where game.screen_name = "Heini"`

![](3_3_04.jpg)

5. `select (elevation_ft * 0.3048) as "elevation_m" from game inner join airport on game.location = airport.ident where game.screen_name = "Heini"`

![](3_3_05.jpg)

6. `select airport.name from airport inner join game on game.location = airport.ident where game.screen_name = "Ilkka"`

![](3_3_06.jpg)

7. `select country.name from airport inner join game on game.location = airport.ident inner join country on airport.iso_country = country.iso_country where game.screen_name = "Ilkka"`

![](3_3_07.jpg)

8. `select name from goal_reached inner join game on game.id = goal_reached.game_id inner join goal on goal.id = goal_reached.goal_id where game.screen_name = "Heini"`

![](3_3_08.jpg)

9. `select airport.name from airport
    inner join goal_reached
    inner join game on game.id = goal_reached.game_id
    inner join goal on goal.id = goal_reached.goal_id
                    where game.screen_name = "Ilkka" and goal.name = "CLOUDS" and airport.ident = game.location`

![](3_3_09.jpg)

10. `select country.name from airport
    inner join goal_reached
    inner join country
    inner join game on game.id = goal_reached.game_id
    inner join goal on goal.id = goal_reached.goal_id
                    where game.screen_name = "Ilkka"
                      and goal.name = "CLOUDS"
                      and airport.ident = game.location
                      and country.iso_country = airport.iso_country`

![](3_3_10.jpg)

## Week 4

## Week 5

