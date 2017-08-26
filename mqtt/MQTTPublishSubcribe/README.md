## MQTT Subscribe / Publish

Durch die Kombination von Subscribe und Publish können u.a. Sensordaten abgefragt werden.

### Programm

* [mbed Compiler](https://developer.mbed.org/compiler/#import:/teams/smdiotkit2ch/code/MQTTPublishSubcribe/)

### Client 

Servo setzen
                       
	mosquitto_pub -t mbed/k64f/iotkit/get/servo1 -m "0.9" -q 0
	
Sensordaten abfragen (Kombination Publish und Subscribe)

	mosquitto_pub -t mbed/k64f/iotkit/get/poti -m "0.5" -q 0 ; mosquitto_sub -t "#" -C 1

