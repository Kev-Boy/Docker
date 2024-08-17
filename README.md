# Introduction
All settings and other information should be stored here.

# Hardware
  - Windows LTSC 64bit

# Service

| No. | Service                 | Port   | Group         | Short Description |
| --- | ----------------------- | ------ | ------------- | ----------------- |
| 1.1 | Portainer               | 5000   | Managmenttool |
| 1.2 | watchtower              | (5010) | Managmenttool |
| 1.3 | duplicati (Backup)      | 5020   | Managmenttool |
| 2.1 | Homeassistent           | 8000   | Smarthome     |
| 2.2 | ESP-Home                | 8010   | Smarthome     |
| 2.3 | mosquitto (mqtt Broker) | 8020   | Smarthome     |
| 2.4 | Matter                  | 8030   | Smarthome     |
| 3.1 | Pi-Hole                 | 9010   | Network       |
| 4.1 | paperless               | 7000   | Dokumentaiton |


# Linux basic commands

| Commands                                               | Description         | Example |
| ------------------------------------------------------ | ------------------- | ------- |
| ```sudo su```                                          | Login as admin      |
| ```sudo apt-get update && sudo apt-get dist-upgrade``` | Linux System Update |
| ```reboot now```                                       | System restart      |
| ```shutdown now```                                     | System Shutdown     |


# Docker basic
Website: https://www.docker.com/
## Installation
source: https://docs.docker.com/engine/install/debian/

## Commands
| Commands        | Description                                       |
| --------------- | ------------------------------------------------- |
| ```docker ps``` | Shows the current status of the Docker container. |

# Portainer
## Installation
Installation for the business edition..
source: https://docs.portainer.io/start/install-ce/server/docker/linux

- ```docker volume create portainer_data```
- ```sudo docker run -d -p 8010:8000 -p 8020:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest```


## Uninstallation
- ```sudo docker stop portainer```
- ```sudo docker rm portainer```
- ```sudo docker volume rm portainer_data```

| Commands                                                                                                                                                                                | Description                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| ```sudo docker volume create portainer_data```                                                                                                                                          | creates the volume for Portainer    |
| ```sudo docker run -d -p 5001:8000 -p 5000:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest``` | Start Portainer with the arguments. |

## Commands

| Commands | Description |
| -------- | ----------- |

# Standard YAML structure
```
version: '3'

name: <stack-name>
services:
  <service-name>:
    container_name: <container-name>
    image: <image-tag>
    ports:
      - "<extern-port>:<intern-port>/<tcp/udp>"
    privileged: <true/false> # root rights
    restart: <no/on-failure[:max-retries]/always/unless-stopped>
    volumes:
      - "/<path on local machine>:/<path on docker>"
    environment:
      <variable>: <value>
```
