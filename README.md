# Openstreetmap TileServer

## Overview
You can use this project to deploy your own map stack on your local system. 

## Run the stack

1. first you need to download osm.pbf file from [download.geofabrik.de](https://download.geofabrik.de/) or any [osm data provider](https://wiki.openstreetmap.org/wiki/Processed_data_providers). this file is the source for the osm data you can store it on osm-data folder.
2. you need to convert your osm.pbf file to mbtiles file. you can use [Tilemaker](https://github.com/systemed/tilemaker) to convert your osm.pbf file to mbtiles file. [docker image](https://hub.docker.com/r/systemed/tilemaker) is also available for tilemaker.
3. then place your files into mbtiles folder
4. run `docker-compose up -d` to start the stack
5. open your browser and go to `http://localhost:8080` to see the map


## Stop the stack
run `docker-compose down` to stop the stack

## Remove the stack
run `docker-compose down -v` to remove the stack



## TODO

- [x] deploy using docker-compose and mbtiles with tileserver-gl
- [ ] add OSM update process
- [ ] add a good frontend 
- [ ] add support for maptunik
- [ ] add support for postgis database and better stack
