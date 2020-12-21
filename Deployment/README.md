
### Docker deploy
Ejecutar  'docker-compose up'. 

## Flujo de servicios
Luego de la ejecución del etl  , los datos serán disponibilizados por medio de una api llamada game_service en el puerto 8080 con python.


### etl

Este servicio ejecuta /core/etl.py para generar 4 archivos csv dentro de /processed_data  que posteriormente serán consumidos por games_api.

 - top_10_games_console_company.csv
 - top_10_games_consoles.csv
 - worst_10_games_console_company.csv
 - worst_10_games_consoles.csv

Esta carpeta sera persistente en la raíz del proyecto.

### games_api

 Api con 4 servicios ir a  : http://localhost:8080/docs 

 - http://localhost:8080/game_service/get_top_10_games_console_company
 - http://localhost:8080/game_service/get_top_10_games_consoles
 - http://localhost:8080/game_service/get_worst_10_games_console_company
 - http://localhost:8080/game_service/get_worst_10_games_consoles

 Dentro de la carpeta service_game se define el router y modelo de datos especifico para "games_service".
 En main.py se configura el app principal
 Dentro de core se agregan scripts con las rutas principales y parametrization  , funciones de ayuda y el etl principal.