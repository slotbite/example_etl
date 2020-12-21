
### Docker deploy
Ejecutar  'docker-compose up'. 

## Servicios

### etl

Corre el etl para generar 4 archivos csv dentro de /processed_data  que serán consumidos por games_api

 - top_10_games_console_company.csv
 - top_10_games_consoles.csv
 - worst_10_games_console_company.csv
 - worst_10_games_consoles.csv

### games_api

 Api con 4 servicios ir a  : http://localhost:8080/docs 

 - http://localhost:8080/game_service/get_top_10_games_console_company
 - http://localhost:8080/game_service/get_top_10_games_consoles
 - http://localhost:8080/game_service/get_worst_10_games_console_company
 - http://localhost:8080/game_service/get_worst_10_games_consoles
