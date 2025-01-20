
---

# Introduction

This documentation outlines the setup, configuration, and management of the services running on the Raspberry Pi 4B, along with additional resources and basic Linux commands. All settings and further details regarding the hardware and services are provided below.

---

# Hardware

- **Device:** Raspberry Pi 4B
  - **CPU:** Quad-core ARM Cortex-A72 (1.5 GHz)
  - **RAM:** Available in 8GB configurations
  - **Storage:** external SSD
  - **Network:** Gigabit Ethernet, Dual-band 802.11ac Wi-Fi
  - **Ports:** 2 USB 3.0, 2 USB 2.0, HDMI (dual 4K support), GPIO pins, USB-C power

The Raspberry Pi 4B is the ideal device for running lightweight server applications and Docker-based containerized services due to its small form factor and strong processing capabilities.

---

# Service

| No. | Service                 | Port      | Group           | Short Description                                                                                                                                                                    |
| --- | ----------------------- | --------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1.1 | Portainer               | 5000      | Management Tool | Portainer is a user-friendly web-based management platform for Docker and Kubernetes environments, enabling easy deployment, monitoring, and management of containers.               |
| 1.2 | Watchtower              | (5010)    | Management Tool | Docker Watchtower automates the process of checking for and updating running Docker containers to their latest versions without manual intervention.                                 |
| 1.3 | Duplicati (Backup)      | 5020      | Management Tool | Duplicati is a backup solution designed for Docker that supports encrypted, incremental, and scheduled backups to cloud storage or local destinations like NAS or external disks.    |
| 1.4 | Uptime Kuma             | 5030      | Management Tool | Uptime Kuma is an open-source monitoring solution for server and service uptime, providing real-time monitoring, alerts, and historical uptime statistics.                           |
| 2.1 | Home Assistant          | 8123      | Smart Home      | Home Assistant is a powerful open-source platform for smart home automation, allowing users to control, automate, and monitor smart devices from a single interface.                 |
| 2.2 | ESPHome                 | 6052      | Smart Home      | ESPHome is a platform that simplifies the process of creating custom firmware for ESP8266 and ESP32-based smart home devices, allowing for seamless integration with Home Assistant. |
| 2.3 | Mosquitto (MQTT Broker) | 8020      | Smart Home      | Mosquitto is a lightweight and efficient MQTT broker that facilitates the communication between IoT devices using the MQTT protocol.                                                 |
| 2.4 | Matter                  | 8030      | Smart Home      | Matter is an open-source standard for smart devices, enabling easy connectivity and integration of Matter-certified devices with smart home platforms like Home Assistant.           |
| 3.1 | Pi-Hole                 | 9010      | Network         | Pi-hole is a network-wide ad blocker that filters DNS queries and blocks ads, improving network performance and user privacy.                                                        |
| 3.2 | Nginx Proxy Manager     | 80/9020/443 | Network         | Nginx Proxy Manager simplifies the management of Nginx as a reverse proxy, allowing for easy configuration of SSL certificates and routing traffic to different services.            |
| 3.3 | Twingate                |           | Network         | Twingate is a secure, software-based network access solution that allows remote access to corporate resources without the need for traditional VPN infrastructure.                   |
| 4.1 | Paperless               | 7000      | Tool            | Paperless is a document management software that digitizes, organizes, and enables searching of paper documents, improving workflow and document retrieval efficiency.               |
| 4.2 | IT Tools                | 7010      | Tool            | IT Tools is a collection of essential and practical IT tools for managing systems, troubleshooting, and performing network and server tasks.                                         |
| 4.3 | Obsidian                | 7020      | Tool            | Obsidian is a powerful knowledge management and note-taking application that uses Markdown and allows for networked thought, making it ideal for building a personal knowledge base. |
| 4.4 | Vaultwarden             | 7030      | Tool            | Vaultwarden is an open-source password manager providing a self-hosted alternative to Bitwarden, offering secure password storage and management.                                    |
| 5.1 | WordPress               | 8010      | Testing         | WordPress is a popular, user-friendly content management system (CMS) that allows users to easily create, manage, and update websites and blogs.                                     |
| 6.1 | Minecraft Server        | 10010      | Gaming          | A Minecraft server allows multiple players to interact and play together in a custom, persistent world. The server can be configured to host different types of gameplay.            |

---

# Linux Basic Commands

Here is an expanded version of the Linux basic commands table, with more useful commands, descriptions, and examples:

---

# Linux Basic Commands

This expanded list provides a comprehensive collection of useful commands to manage your Linux system, network, processes, and file system efficiently. You can use these commands to perform daily administrative tasks and troubleshooting.

| Commands                                               | Description                                       | Example                                            |
| ------------------------------------------------------ | ------------------------------------------------- | -------------------------------------------------- |
| ```sudo su```                                          | Switch to root user                               | `sudo su`                                          |
| ```sudo apt-get update && sudo apt-get dist-upgrade``` | Update Linux system packages                      | `sudo apt-get update && sudo apt-get dist-upgrade` |
| ```reboot now```                                       | Restart the system                                | `reboot now`                                       |
| ```shutdown now```                                     | Shutdown the system                               | `shutdown now`                                     |
| ```pwd```                                              | Print the current working directory               | `pwd`                                              |
| ```ls```                                               | List the contents of a directory                  | `ls` / `ls -l`                                     |
| ```cd <directory>```                                   | Change the current directory                      | `cd /home/user/`                                   |
| ```mkdir <directory>```                                | Create a new directory                            | `mkdir new_folder`                                 |
| ```rm <file>```                                        | Remove a file                                     | `rm filename.txt`                                  |
| ```rm -r <directory>```                                | Remove a directory and its contents recursively   | `rm -r old_folder/`                                |
| ```cp <source> <destination>```                        | Copy a file or directory                          | `cp file1.txt /home/user/destination/`             |
| ```mv <source> <destination>```                        | Move or rename a file or directory                | `mv file1.txt /home/user/new_name.txt`             |
| ```chmod <permissions> <file/directory>```             | Change file or directory permissions              | `chmod 755 file1.sh`                               |
| ```chown <user>:<group> <file/directory>```            | Change the owner and group of a file or directory | `chown user:group file1.txt`                       |
| ```ps aux```                                           | Display a list of all running processes           | `ps aux`                                           |
| ```top```                                              | Display real-time system resource usage           | `top`                                              |
| ```kill <PID>```                                       | Terminate a process by PID                        | `kill 1234`                                        |
| ```killall <process_name>```                           | Terminate all processes by name                   | `killall firefox`                                  |
| ```df -h```                                            | Display available disk space                      | `df -h`                                            |
| ```du -sh <directory>```                               | Show disk usage of a directory                    | `du -sh /home/user`                                |
| ```free -h```                                          | Display memory usage                              | `free -h`                                          |
| ```ifconfig```                                         | Display network interface configuration           | `ifconfig`                                         |
| ```ping <hostname/IP>```                               | Ping a network host to check connectivity         | `ping google.com`                                  |
| ```netstat -tuln```                                    | Display all listening ports                       | `netstat -tuln`                                    |
| ```grep <pattern> <file>```                            | Search for a pattern in a file                    | `grep "error" /var/log/syslog`                     |
| ```tar -czvf <archive.tar.gz> <directory>```           | Create a compressed archive of a directory        | `tar -czvf archive.tar.gz /path/to/directory/`     |
| ```tar -xzvf <archive.tar.gz>```                       | Extract a compressed archive                      | `tar -xzvf archive.tar.gz`                         |
| ```find <directory> -name <filename>```                | Find a file by name within a directory            | `find /home/user -name *.txt`                      |
| ```sudo apt-get install <package>```                   | Install a package using APT                       | `sudo apt-get install vim`                         |
| ```sudo apt-get remove <package>```                    | Remove a package using APT                        | `sudo apt-get remove vim`                          |
| ```sudo apt-get autoremove```                          | Remove unnecessary packages                       | `sudo apt-get autoremove`                          |
| ```sudo systemctl start <service>```                   | Start a systemd service                           | `sudo systemctl start apache2`                     |
| ```sudo systemctl stop <service>```                    | Stop a systemd service                            | `sudo systemctl stop apache2`                      |
| ```sudo systemctl restart <service>```                 | Restart a systemd service                         | `sudo systemctl restart apache2`                   |
| ```sudo systemctl enable <service>```                  | Enable a systemd service to start on boot         | `sudo systemctl enable apache2`                    |
| ```sudo systemctl disable <service>```                 | Disable a systemd service from starting on boot   | `sudo systemctl disable apache2`                   |
| ```alias <alias_name>="<command>"```                   | Create a shortcut for a command                   | `alias ll="ls -la"`                                |
| ```history```                                          | Show command history                              | `history`                                          |
| ```clear```                                            | Clear the terminal screen                         | `clear`                                            |

---




---

# Docker Basic Setup

**Website:** [Docker Official Website](https://www.docker.com/)

## Installation Guide

To install Docker on your Raspberry Pi, use the official instructions provided in the [Docker Docs](https://docs.docker.com/engine/install/debian/).

Install Docker by running:
```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

After installation, make sure to add the user to the Docker group:
```bash
sudo usermod -aG docker ${USER}
```

## Basic Docker Commands

Here’s an expanded version of the **Basic Docker Commands** table with additional useful commands for managing Docker containers:

---

## Basic Docker Commands
This expanded table includes a variety of essential and useful Docker commands to help with managing containers, images, networks, and resources. These commands cover both everyday operations and advanced Docker management tasks.

| Commands                                                    | Description                                                                  |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------- |
| ```docker ps```                                             | Lists the running Docker containers.                                         |
| ```docker stop <container_id>```                            | Stops a running container.                                                   |
| ```docker run -d <image_name>```                            | Run a Docker container in detached mode.                                     |
| ```docker exec -it <container_id> bash```                   | Access a running container's terminal.                                       |
| ```docker start <container_id>```                           | Starts a stopped container.                                                  |
| ```docker restart <container_id>```                         | Restarts a running or stopped container.                                     |
| ```docker rm <container_id>```                              | Removes a stopped container from the system.                                 |
| ```docker rmi <image_name>```                               | Removes a Docker image from the local machine.                               |
| ```docker images```                                         | Lists all Docker images on the system.                                       |
| ```docker pull <image_name>```                              | Downloads a Docker image from Docker Hub or another registry.                |
| ```docker build -t <image_name> <path>```                   | Builds a Docker image from a Dockerfile located at the given path.           |
| ```docker logs <container_id>```                            | Displays logs from a running or stopped container.                           |
| ```docker ps -a```                                          | Lists all containers (running and stopped).                                  |
| ```docker network ls```                                     | Lists all available Docker networks.                                         |
| ```docker volume ls```                                      | Lists all Docker volumes available.                                          |
| ```docker inspect <container_id>```                         | Provides detailed information about a container or image.                    |
| ```docker stats```                                          | Displays resource usage statistics for running containers.                   |
| ```docker-compose up```                                     | Starts all containers defined in a `docker-compose.yml` file.                |
| ```docker-compose down```                                   | Stops and removes all containers defined in a `docker-compose.yml` file.     |
| ```docker-compose logs```                                   | View logs for all containers defined in a `docker-compose.yml` file.         |
| ```docker-compose build```                                  | Builds or rebuilds services defined in a `docker-compose.yml` file.          |
| ```docker ps -q```                                          | Lists only the container IDs of running containers.                          |
| ```docker top <container_id>```                             | Displays running processes within a container.                               |
| ```docker cp <container_id>:<container_path> <host_path>``` | Copies files or folders from a container to the host machine.                |
| ```docker cp <host_path> <container_id>:<container_path>``` | Copies files or folders from the host machine to a container.                |
| ```docker exec -it <container_id> <command>```              | Executes a command in a running container.                                   |
| ```docker update <container_id>```                          | Updates a container's resource settings (e.g., memory, CPU limits).          |
| ```docker info```                                           | Displays system-wide Docker information, such as version and resource usage. |


---

# Portainer

Portainer simplifies Docker management by providing a user-friendly interface for managing containers, networks, and volumes.

## Installation

Follow these steps to install Portainer for Docker:

1. Create a Docker volume for persistent data:
   ```bash
   docker volume create portainer_data
   ```

2. Run the Portainer container:
   ```bash
   sudo docker run -d -p 5001:8000 -p 5000:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ee:latest
   ```

## Uninstallation

To uninstall Portainer, use the following commands:

1. Stop the Portainer container:
   ```bash
   sudo docker stop portainer
   ```

2. Remove the Portainer container:
   ```bash
   sudo docker rm portainer
   ```

3. Remove the Portainer data volume:
   ```bash
   sudo docker volume rm portainer_data
   ```

---

# Standard YAML Structure for Docker Compose

Docker Compose allows you to define and manage multi-container Docker applications with ease. Here's a standard YAML structure:

```yaml
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

This structure defines the basic setup for any Docker-based service or application, ensuring container management is standardized and easy to replicate.

---