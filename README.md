# Docker Compose Services

This repository contains Docker Compose configurations for several popular services, including SQL Server, MySQL, Redis, PostgreSQL, and RabbitMQ. Each service has its own `docker-compose` file for easy individual management.

## Available Services

- SQL Server
- MySQL
- Redis
- PostgreSQL
- RabbitMQ
- MongoDB

## How to Use

### Prerequisites

Ensure you have Docker and Docker Compose installed on your machine. To check the installation, run:

```bash
docker --version
docker-compose --version
```

### Steps to Run the Services

1. Clone this repository:
```bash
git clone https://github.com/rsantosdosanjos/docker-compose-services.git
cd docker-compose-services
```

2. For each service, navigate to the directory where the respective docker-compose file is located and execute the command to start the desired service.

### SQL Server
To start SQL Server:
```bash
docker-compose -f docker-compose-sql.yml up -d
```
Access SQL Server on port `1433`.

### MySQL
To start MySQL:
```bash
docker-compose -f docker-compose-mysql.yml up -d
```
Access MySQL on port `3306`.

### Redis
To start Redis:
```bash
docker-compose -f docker-compose-redis.yml up -d
```
Access Redis on port `6379`.

### PostgreSQL
To start PostgreSQL:
```bash
docker-compose -f docker-compose-postgres.yml up -d
```
Access PostgreSQL on port `5432`.

### RabbitMQ
To start RabbitMQ:
```bash
docker-compose -f docker-compose-rabbitmq.yml up -d
```
Access RabbitMQ on port `5672` and the management console on port `15672`.

### MongoDB
To start MongoDB:
```bash
docker-compose -f docker-compose-mongodb.yml up -d
```
Access MongoDB on port `27017`.

### Stopping the Services
To stop any service, use the corresponding command:
```bash
docker-compose -f <file> down
```
Replace <file> with the name of the docker-compose file for the service you want to stop. For example, to stop SQL Server, use:
```bash
docker-compose -f docker-compose-sql.yml down
```

### Volumes
Volumes are used to ensure data persistence between container restarts. Each service has a configured volume for its data.
