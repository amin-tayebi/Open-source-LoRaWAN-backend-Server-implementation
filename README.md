# Open-source-LoRaWAN-backend-Server-implementation
Implementation of ChirpStack, open-source LoRaWAN backend Server (2020)

I implemented a LoraWAN backend system on a PC. It can act as LoraWAN Network Server, Join Server and Application Server based on chirpstack. The necessary components for implementing LoRaWAN infrastructure has been implemented locally. Some of the main parts of the procedure are

1-I set up postgre-sql database and related configurations to store data of app-server and network-server 

2-I set up following components and their related configuration file: -chirpstack-Application Server -chirp network Server -chirpstack-gw-bridge 

3-I generated the data from a sample virtual-lora-gateway (e.g. device-counter) 

4-I set up and start a web interface for app server using its configuration, inside the Application Server: -created service profile -created a device profile -defined gw, app and lora-device 

5-I received the payload of the virtual device on the web interface (application-server) also in the log file of Gateway in the terminal. Moreover It could be noticeable that there are different scenarios to locate chirp-gateway-brige:

when we have single physical-gw usually it installs on the physical-gateway itself (e.g on dragino GW) or it can install on separate server system.

In the current Lora-backend a simple java-script function created for: 1-Decoding the uplink (for the payload to be readable) 2-Encoding the downlink. Then we accessed the REST API to interact with chirpstack-app-server and now we are able to transfer the payload in another web-app-server or any web-server e.g. create a XAMP server and locate the data there using CURL, payloads can be saved in the HOST in a text file or a DataBase.
