# OpenAquarium-System

Components making up the St Peter's Mbare Aquaponics System 1:

## Hardware
1. Open Aquarium (Cooking Hacks)
2. Raspberry Pi 3 (Element 14, CanaKit)

## Software
1. Arduino
2. Node.js and npm
3. Node-red
4. Node-red nodes: Dashboard, Serialport, mongodb
5. Mongodb NoSQL DBMS

## Nodered Functions
1. Format Data for MongoDB: scrubs the data from Arduino microcontroller, formats it and saves it in a Mongodb Database named "aquadb" within a collection named "SensorReadings"

### Temperature

2. Temperature: Extracts temperature value from Arduino, forwarding the value to "Plot Temperature" Chart and "Check Temperature" Function nodes
3. Check Temperature: checks the most recent temperature reading. If the value is greater than 25 Degrees Celsius it will send a notification email every 15 minutes

## Important Changes
Had to suppress the Water Level Serial output by commenting them out in OpenAquarium.cpp file in the OpenAquarium library.
