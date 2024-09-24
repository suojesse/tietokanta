Yhteen tauluun kohdistuvien kyselyiden harjoitukset

1 tehtävä: 
select * from goal;

2 tehtävä:
select name airport_type from airport where iso_country = "FI";

3 tehtävä:
select name from airport where iso_country = "FI" order by name;

4 tehtävä:
select name, type from airport where iso_country = "FI" order by type, name;

5 tehtävä:
select name from country where name like "F%";

6 tehtävä:
select name from country where name like "%F%";

7 tehtävä:
select location from game where screen_name = "Vesa";

8 tehtävä:
select co2_consumed from game where screen_name = "Ilkka";

9 tehtävä:
select distinct co2_budget from game;

Where osan liitosehto harjoitukset

1 tehtävä:
SELECT country.name AS "country name", airport.name AS "airport name" FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE country.name = 'Iceland';

2 tehtävä:
SELECT airport.name AS "airport name" FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE country.name = 'France' AND airport.type = 'large_airport';

3 tehtävä:
SELECT country.name AS country_name, airport.name AS airport_name FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE airport.continent = 'AN';

4 tehtävä:
SELECT airport.elevation_ft FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Heini';

5 tehtävä:
SELECT airport.elevation_ft * 0.3048 AS elevation_m FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Heini';

6 tehtävä:
SELECT airport.name FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Ilkka';

7 tehtävä:
SELECT country.name FROM game JOIN airport ON game.location = airport.ident JOIN country ON airport.iso_country = country.iso_country WHERE game.screen_name = 'Ilkka';

8 tehtävä:
select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";

9 tehtävä:
select airport.name from airport, game, goal, goal_reached where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";


10 tehtävä:
select country.name from country, airport, game, goal, goal_reached where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";

