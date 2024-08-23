MQTT Broker (Mosquitto)
========================
Simple config to build MQTT Broker using Docker.

1. COMMANDS

- To whip-up Bash : 

        sudo docker exec -it mosquitto-mosquitto-1 sh

- To run container manually, use `run.sh` or :

        sudo docker run -it -p 1883:1883 -p 9001:9001 -v ./config/mosquitto.conf:/mosquitto/config/mosquitto.conf -v /mosquitto/data -v /mosquitto/log eclipse-mosquitto
