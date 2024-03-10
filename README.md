# IES_Gateway

This Project provides a software solution for easy data collection of IoT Sensors by using the MQTT and CoAP communication protocol.

## MODULES

- IES_Gateway_Backend     : provides the Backend which is responsible to check incomming data and store them into Database
- IES_MQTT_Client         : provides a module which is responsible to receiving data from the MQTTBroker, checking and forwarding to the Backend using the MQTT pub/sub mechanism
- IES_CoAP_Client         : provides a module which is responsible of receiving data using the CoAP server/client mechanism

## Config

- mosquitto.conf          : holds the configuration for the MQTT Broker
- .env                    : holds the envirionment variables for setup the Gateway components

## HOW TO RUN

1. Create a .env file
2. Inside .env create a MARIADB_ROOT_PW envirionment variable and assign a root password to Database e.g MARIADB_ROOT_PW=1234
3. Use docker compose to start the Gateway components
   1. For production choose the profile **fullgateway**
