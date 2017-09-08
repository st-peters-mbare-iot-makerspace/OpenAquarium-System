# OpenAquarium-System

Aquaponics

Hardware

Open Aquarium (Cooking Hacks)
Raspberry Pi 3 (Element 14)
Software

Arduino
Node.js and npm
Node-red
Node-red nodes: Dashboard, Serialport, mongodb
Mongodb NoSQL DBMS
Nodered Functions

Format Data for MongoDB: scrubs the data from Arduino microcontroller, formats it and saves it in a Mongodb Database named "aquadb" within a collection named "SensorReadings"
Temperature

Temperature: Extracts temperature value from Arduino, forwarding the value to "Plot Temperature" Chart and "Check Temperature" Function nodes
Check Temperature: checks the most recent temperature reading. If the value is greater than 25 Degrees Celsius it will send a notification email every 15 minutes
Important Changes

Had to suppress the Water Level Serial output by commenting them out in OpenAquarium.cpp file in the OpenAquarium library.
