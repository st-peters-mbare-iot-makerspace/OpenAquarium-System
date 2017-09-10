# St Peter's Mbare Aquaponics System 1

Components making up the St Peter's Mbare Aquaponics System 1:

## Hardware
1. Arduino Uno (DFRobot)
2. Open Aquarium Arduino Shield (Cooking Hacks)
3. Electroconductivity Sensor (Cooking Hacks)
4. Temperature Sensor (Cooking Hacks)
5. Ph Sensor (Cooking Hacks)
6. Water Level Sensor (Cooking Hacks)
7. Fish Feeder (Cooking Hacks)
8. Raspberry Pi 3 (Element 14, CanaKit)

## Software
1. Arduino 1.8
2. Node.js 6 (LTS) and npm 3
3. Node-red 16
4. Node-red nodes: Dashboard, Serialport, mongodb
5. Mongodb NoSQL DBMS

## Nodered Functions
1. Format Data for MongoDB: scrubs the data from Arduino microcontroller, formats it and saves it in a Mongodb Database named "aquadb" within a collection named "SensorReadings"

### Temperature

2. Temperature: Extracts temperature value from Arduino, forwarding the value to "Plot Temperature" Chart and "Check Temperature" Function nodes
3. Check Temperature: checks the most recent temperature reading. If the value is greater than 25 Degrees Celsius it will send a notification email every 15 minutes

## Important Changes
Suppressed the Water Level Serial output by commenting them out in OpenAquarium.cpp file in the OpenAquarium library.
