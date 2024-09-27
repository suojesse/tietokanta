Yhteen tauluun kohdistuvien kyselyiden harjoitukset

1 tehtävä: 
select * from goal;
![image](https://github.com/user-attachments/assets/89250105-9fe5-4eee-940b-f65377ac9ba1)

2 tehtävä:
select name airport_type from airport where iso_country = "FI";
![image](https://github.com/user-attachments/assets/42201626-6076-4260-b3ce-c662c6889b06)

3 tehtävä:
select name from airport where iso_country = "FI" order by name;
![image](https://github.com/user-attachments/assets/7fde082d-8555-4cd5-889a-aea79161595d)

4 tehtävä:
select name, type from airport where iso_country = "FI" order by type, name;
![image](https://github.com/user-attachments/assets/77d37be5-2bd8-408b-87d4-a275ce3c0cde)

5 tehtävä:
select name from country where name like "F%";
![image](https://github.com/user-attachments/assets/619743b2-0eb5-45bf-95da-54774e0be197)

6 tehtävä:
select name from country where name like "%F%";
![image](https://github.com/user-attachments/assets/cdd27a32-4119-4b22-9b2f-d8bea3fd2482)

7 tehtävä:
select location from game where screen_name = "Vesa";
![image](https://github.com/user-attachments/assets/0fadaae8-fdfc-4947-8f34-c637bebab08b)

8 tehtävä:
select co2_consumed from game where screen_name = "Ilkka";
![image](https://github.com/user-attachments/assets/6375a628-bfaf-4155-a4d0-333ad512a665)

9 tehtävä:
select distinct co2_budget from game;
![image](https://github.com/user-attachments/assets/b2879e1b-0a36-4cbb-94c6-64b3d12bdaf6)

Where osan liitosehto harjoitukset

1 tehtävä:
SELECT country.name AS "country name", airport.name AS "airport name" FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE country.name = 'Iceland';
![image](https://github.com/user-attachments/assets/cc204a12-81dc-443e-a8a6-130fc38849d2)

2 tehtävä:
SELECT airport.name AS "airport name" FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE country.name = 'France' AND airport.type = 'large_airport';
![image](https://github.com/user-attachments/assets/89c37036-c976-4ac7-8fc4-a762de259f13)

3 tehtävä:
SELECT country.name AS country_name, airport.name AS airport_name FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE airport.continent = 'AN';
![image](https://github.com/user-attachments/assets/12f67575-1427-4236-a1c5-f7fcaa8912f3)

4 tehtävä:
SELECT airport.elevation_ft FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Heini';
![image](https://github.com/user-attachments/assets/7ee1d8fe-99da-4125-8360-6e4cfe0a5917)

5 tehtävä:
SELECT airport.elevation_ft * 0.3048 AS elevation_m FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Heini';
![image](https://github.com/user-attachments/assets/377299ab-0e22-4c7a-85f5-484eb77ecdad)

6 tehtävä:
SELECT airport.name FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Ilkka';
![image](https://github.com/user-attachments/assets/203b2622-8ead-40da-99f6-6795a39b38f8)

7 tehtävä:
SELECT country.name FROM game JOIN airport ON game.location = airport.ident JOIN country ON airport.iso_country = country.iso_country WHERE game.screen_name = 'Ilkka';
![image](https://github.com/user-attachments/assets/d1adb2e5-a3e7-4d08-a4d8-1aac8349d7fe)

8 tehtävä:
select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
![image](https://github.com/user-attachments/assets/5c35a773-3697-4b2d-b0ad-c6b125d07925)

9 tehtävä:
select airport.name from airport, game, goal, goal_reached where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
![image](https://github.com/user-attachments/assets/983325c5-86e9-4649-b164-7fa58006a371)

10 tehtävä:
select country.name from country, airport, game, goal, goal_reached where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
![image](https://github.com/user-attachments/assets/17f64b4a-831e-4ede-a669-2c83325b7b18)

