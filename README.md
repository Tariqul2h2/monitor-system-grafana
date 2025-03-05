# Dockerized Monitoring Stack with Grafana, Prometheus, and Nginx

This repository provides an easy-to-deploy monitoring stack using **Grafana**, **Prometheus**, and **Nginx** with Docker Compose. The stack includes **Prometheus** for metric scraping, **Grafana** for data visualization, and **Nginx** as a reverse proxy to access the Grafana dashboard securely without directly exposing the port.

## Directory Structure

├── docker-compose.yml  
├── env.example  
├── nginx  
│   └── nginx.conf  
├── prometheus  
│   └── prometheus.yml  


## Prerequisites

To run this project, you need to have the following installed on your machine:
- Docker
- Docker Compose

You can download docker instalation file from the following repository:
[download-docker-setup-file](https://github.com/Tariqul2h2/docker/tree/main)


## Getting Started


### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/Tariqul2h2/monitor-system-grafana.git
cd monitor-system-grafana
```

Create a `.env` file using the provided `env.example` as a template:
```bash
cp env.example .env
```
Example `.env` file:
```
GRAFANA_ADMIN_PASSWORD=yourpasswordhere
```

## Start the Docker Containers
Run the following command to start the Grafana, Prometheus, and Nginx containers:
```bash
docker-compose up -d
```

This will start the following services:

* Grafana: Available at http://serverip:3000 (Behind Nginx proxy).  
*Prometheus: Scraping metrics from various targets, as specified in the prometheus.yml file.  
* Nginx: Reverse proxy for Grafana, accessible through http://serverip.  

Also available in `localhost` if you installed in your computer instead of  a virtual machine.
<br><br><br><br>
>Feel free to submit issues and pull requests. If you want to enhance the project, consider adding new features, improving documentation, or fixing bugs.