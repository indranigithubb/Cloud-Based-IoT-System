# Cloud-Based-IoT-System

This project is to build a cloud-based IoT system which collects data from a set of virtual sensors that are
deployed to collect environmental information using the MQTT protocol. It display the latest sensor data values received from all the sensors of a specified environmental station. It display the sensor data values received during the last five hours from all environmental station
of a specified sensor. 

Steps to follow :

First I created an account in Wokwi and selected ESP32 and micropython to do my simulation task.
Based on the requirement I have written a python code to represent a virtual environment IoT station that periodically generates a set of random virtual sensor values for the following sensors: 1. Temperature (Range: -50 to 50 Celsius) 2. Humidity (Range: 0 to 100%) 3. Co2 sensor (Range: 300ppm to 2000ppm). The code includes Wokwi SSID and password.Also I have included my MQTT credentials created in Thinkspeak in my python code in order to send sensor data to Thinkspeak for visual representation of data.
I have also designed the simulation diagram in diagram.json file in Wokwi.
Side by side, the MQTT is controlled by the cloud-based backend which was implemented using ThingSpeak technology. I created an account in Thinkspeak and created my channel. I created MQTT device in it , and added my channel into the device and given permission for publish and subscribe in it.The MQTT account has it’s own userid, password, clientid details.
The output generated in Wokwi after running the python program and also generated temparature, humidity and CO2 value randomly within the range mentioned. 
As the MQTT credential was already added in the python code, it was able to send the sensor data via MQTT to Thinkspeak and gave a visualization of data separately for temperature, humidity and CO2 for field 1, field 2 and field 3 respectively.
At last I have selected MALTAB analysis from Thinkspeak to plot 2D representation of data for temperature, humidity and CO2. To execute it, I had to write MATLAB code to generate the graphical representation of data for temperature, humidity and CO2. It was able to collect sensor data received during the last five hours.
