Join harjoitukset

1 Tehtävä:
select country.name as "country name", airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";
![image](https://github.com/user-attachments/assets/394c3ab8-07cc-4ec2-bc95-1e1610c0b0a2)

2 Tehtävä:
select screen_name, airport.name
from game inner join airport on location = ident;
![image](https://github.com/user-attachments/assets/a6798d99-65fc-4093-8662-2e3677fd97d3)

3 Tehtävä:
select screen_name, country.name
from game inner join airport on location = ident inner join country on airport.iso_country = country.iso_country;
![image](https://github.com/user-attachments/assets/78363d02-6db3-47f2-a11a-3514adcb0c11)

4 Tehtävä:
select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";
![image](https://github.com/user-attachments/assets/4edd50e5-1f84-4925-8635-16a933baf0e4)

5 Tehtävä:
select name, screen_name
from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;
![image](https://github.com/user-attachments/assets/9547086f-3bd0-4220-9434-28e51a36a7ba)

Sisäkysely harjoitukset

1 Tehtävä:
select name from country where 
iso_country in( select iso_country from airport where name like "Satsuma%");
![image](https://github.com/user-attachments/assets/bce8156a-efa9-42ee-9d5d-e0916cd3aeba)

2 Tehtävä:
select name from airport where iso_country in( select iso_country from country where name = "Monaco");
![image](https://github.com/user-attachments/assets/6660affd-6d19-4e38-93e6-92b435d8bb04)

3 Tehtävä:
select screen_name from game where id in ( select game_id from goal_reached where goal_id in( select id from goal where name = "CLOUDS"));
![image](https://github.com/user-attachments/assets/52884bd0-5f64-430d-821d-ce2210dc755b)


4 Tehtävä:
select country.name from country where iso_country not in (select airport.iso_country from airport);

5 Tehtävä:
select name from goal where id not in( select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini");
