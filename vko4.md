Koostetieto kyselyt

tehtävä 1: select max(elevation_ft) from airport;
![image](https://github.com/user-attachments/assets/144b9e3e-6669-4667-893d-f79806124ba1)

tehtävä 2: select continent, count(*) from country group by continent;
![image](https://github.com/user-attachments/assets/281de89d-d9a5-43c6-96a7-e45d08f5f7dc)

tehtävä 3: select screen_name, count(*) from game, goal_reached where id = game_id group by screen_name;
![image](https://github.com/user-attachments/assets/4d9d6c28-131c-41b1-8426-8f24b80a3830)

tehtävä 4: select screen_name from game where co2_consumed in(select min(co2_consumed) from game);
![image](https://github.com/user-attachments/assets/eaf05097-a47a-457c-a40c-55b0f4ada50b)

tehtävä 5:select country.name, count(*) from airport, country where airport.iso_country = country.iso_country 
group by country.iso_country order by count(*) desc limit 50;
![image](https://github.com/user-attachments/assets/fba79c7d-e7b8-4f2f-be49-42f4cb2bd338)

tehtävä 6:select country.name from airport, country where airport.iso_country = country.iso_country 
group by country.iso_country having count(*) > 1000;
![image](https://github.com/user-attachments/assets/4048842d-1b88-4ee2-ac87-a3e021adcfb6)

tehtävä 7: select name from airport where elevation_ft in ( select max(elevation_ft) from airport );
![image](https://github.com/user-attachments/assets/fcfc8d3d-17ce-4e5f-b303-0b5a381a3b3c)

tehtävä 8: select name from country where iso_country in (select iso_country from airport
where elevation_ft in(select max(elevation_ft)from airport));
![image](https://github.com/user-attachments/assets/c5224e68-8e75-48d1-b726-e536e14e8db4)

tehtävä 9: select count(*) from game, goal_reached where id = game_id and screen_name = "Vesa" group by screen_name;
![image](https://github.com/user-attachments/assets/5459e0aa-c792-4f82-a2aa-ba9bacbc06cf)

tehtävä 10: select name from airport where latitude_deg in( select min(latitude_deg) from airport);
![image](https://github.com/user-attachments/assets/6bff4b5a-470d-4d77-8958-0b2463a21af4)

Päivityskysely harjoitukset

tehtävä 1: 
update game 
set  location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed+500
where screen_name = "Vesa";
![image](https://github.com/user-attachments/assets/4eade91e-a2ce-4c27-b890-4bdd4b80502d)



tehtävä 2: 

tehtävä 3: delete from goal_reached;
![image](https://github.com/user-attachments/assets/527676cd-dcaf-450b-b5ed-1fd120e2e75f)

tehtävä 4: delete from game;
![image](https://github.com/user-attachments/assets/a1e62da7-7572-489f-8352-90b46e6fe109)
