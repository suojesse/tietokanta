Join harjoitukset

1 Tehtävä:
select country.name as "country name", airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";

2 Tehtävä:
select screen_name, airport.name
from game inner join airport on location = ident;

3 Tehtävä:
select screen_name, country.name
from game inner join airport on location = ident inner join country on airport.iso_country = country.iso_country;

4 Tehtävä:
select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";

5 Tehtävä:
select name, screen_name
from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;

Sisäkysely harjoitukset

1 Tehtävä:
select name from country where 
iso_country in( select iso_country from airport where name like "Satsuma%");

2 Tehtävä:
select name from airport where iso_country in( select iso_country from country where name = "Monaco");

3 Tehtävä:
select screen_name from game where id in ( select game_id from goal_reached where goal_id in( select id from goal where name = "CLOUDS"));

4 Tehtävä:
select country.name from country where iso_country not in (select airport.iso_country from airport);

5 Tehtävä:
select name from goal where id not in( select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini");
