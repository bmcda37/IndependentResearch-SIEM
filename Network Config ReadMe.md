# Configuration of Docker Compose, Docker Bridge Network, &  Port Forwarding

## Purpose

We will need to allow our XCP-ng server to communicate with our Docker containers which consist of the Wazuh Manager, Wazuh Indexer, and Wazuh Dashboard. The reason for this is so our agents installed on the VMs which are hosted on XCP-ng, will be able to communicate, sending information to the Wazuh cluster.

Let's begin by configuring our docker-compose.yml file.

Since I am using the single-node option for my cluster, you will need to go to the Docker-Compose.yml file located at ```/wazuh-docker/single-node``` . Once within the directory, you will be able to run the ```docker-compose up -d``` cmd to run all the containers outlined in the compose file.

## Docker-Compose File

Docker Compose allows us to group our containers within one network which is created by Docker. Within this group, the docker containers can be ran together while allowing them to communicate with each other. This is beneficial for our Wazuh cluster since we will need the Wazuh Manager, Wazuh Indexer, and Wazuh Dashboard to send/recieve data.

For each service defined in your docker-compose.yml file, ensure you have defined your network for each service.
```
    networks:
      - custom-network
```

After defining the services for your docker-compose, you will then need to define your Docker network in your docker-compose.yml file.

Add the following to the bottom of your docker-compose.yml file.
```
networks:
  custom-network:
    driver: bridge
    ipam:
      driver: default
      config:
        - subnet: <ip of subnet for your network>
```

## Docker Bridge Network
When defining my bridge network, I chose to do so in my docker-compose file. 

*    Note: By configuring the network this way, the 'custom-network' will only be created when docker-compose is running and will not be listed in 'network ls' if compose is not running.

```
networks:
  custom-network:
    driver: bridge
    ipam:
      driver: default
      config:
        - subnet: <ip of subnet for your network>
```

## Port Fowarding (Xcp-ng -> Host -> Docker-Compose)

