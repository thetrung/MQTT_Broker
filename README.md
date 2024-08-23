MQTT Broker (Mosquitto)
========================
Simple config to build MQTT Broker using Docker.

### CONFIG
Remember to open port `1883` to remote if using localhost. Change to any other port inside `./config/mosquitto.conf`.

### COMMANDS

- To run with `docker-compose` inside this project folder :

        sudo docker compose up -d

- To run container manually, use `run.sh` or :

        sudo docker run -it -p 1883:1883 -p 9001:9001 -v ./config/mosquitto.conf:/mosquitto/config/mosquitto.conf -v /mosquitto/data -v /mosquitto/log eclipse-mosquitto

- To whip-up Bash : 

        sudo docker exec -it mosquitto-mosquitto-1 sh
  
- To subscribe a topic (ex: `test`) from inside container :

        mosquitto_sub -t test 
