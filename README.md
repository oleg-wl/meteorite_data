# meteorite_data
Educational project to collect data from NASA Meteorite-Landing API.
First of all it helps me to have some SQL and Python practice but you are welcome to use in in your projects.
## About 
Information about [NASA Meteorite-Landings API](https://data.nasa.gov/Space-Science/Meteorite-Landings/gh4g-9sfh)

Script gets data from Nasa API, converts ans stores it into table in sql database: meteorites.db
Than script adds a table with geodata from OWM API, so to use it you should have an OWM api key. 

meteorites.db schema:
1. Table 'Meteorites':
 * id - primary key
 * name - meteorite's name
 * nametype
 * recclass - meteorite's class
 * mass - weight of meteorite
 * fall 
 * year - %YYYY year of meteorite's falling to Earth
2. table 'Geodata':
 * geoid - foreighn key
 * latitude
 * longtitude
 * place - information apaut landing place from OWM
 * country
 * state
 
**Note.** Free OWM API Key has limitations 60 api calls per minute, so requesting to API has time.sleep (1m) limitation. Full refreshing of database takes about 15 minutes.

## Usage

1. git clone https://github.com/nolegvl/meteorite_data
2. pip install -r requests.txt
3. create enviroment variable: export METEO_API='your api key'. _You can also replace source code with your api-key in app.py_
3. run: python main.py
This actions create meteorites.db in project's dir. You can use this in your prijects or analytics.

## Analytics
TODO
[] Create jupyter notebook with folium to make data visualisetion