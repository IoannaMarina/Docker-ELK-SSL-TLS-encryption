# Docker-ELK-SSL-TLS-encryption
ELK Stack Deployment

This repository contains the necessary configuration files to deploy an ELK (Elasticsearch, Logstash, and Kibana) stack with additional components like Metricbeat and Filebeat, secured with TLS/SSL certificates. The TLS/SSL certificates provide encryption and authentication, ensuring secure communication between the various components of the ELK stack.

![image](https://github.com/IoannaMarina/Docker-ELK-SSL-TLS-encryption/assets/56870509/20c5d3ac-2c6f-4df5-b5e9-e3859dddf5b4)


Prerequisites:
- Docker and Docker Compose installed on your machine.
- Filebeat version 8.8.2 downloaded and configured according to your requirements.

Deployment Instructions:
1. Clone this repository to your local machine.
2. Navigate to the root directory of the repository.
3. Start the ELK stack containers (Elasticsearch, Logstash, and Kibana) using the following command:
   docker-compose up -d
This will launch the ELK stack containers in detached mode, allowing them to run in the background.
4. (Optional) To include Metricbeat in the stack, run Docker Compose from the root of the repository with an additional command line argument referencing the metricbeat-compose.yml file:
   docker-compose -f docker-compose.yml -f extensions/metricbeat/metricbeat-compose.yml up -d
This will start the Metricbeat container along with the ELK stack containers.
5. (Optional) If you have set up Filebeat, start it using the appropriate command based on your system. For example, on Linux, you can use:
   sudo systemctl start filebeat

Adjust the command based on your operating system and configuration.

Note: Once the containers are up and running, you can access the Kibana user interface by opening a web browser and navigating to `https://192.168.100.45:5601`. Replace `192.168.100.45` with the actual IP address of the machine running the ELK stack.
