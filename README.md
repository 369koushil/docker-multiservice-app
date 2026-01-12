# Dockerized Multi-Service Backend

This project demonstrates a containerized multi-service backend using Docker and Docker Compose on Linux (Ubuntu).

## Services
- Node.js + Express API
- MongoDB database
- Mongo Express UI

## Prerequisites
- Docker
- Docker Compose

## Project Structure
```
docker-multi-service-app/
├── backend/
│   ├── Dockerfile
│   ├── package.json
│   ├── server.js
│   └── models/User.js
├── docker-compose.yml
└── README.md
```

## Run the Project

From the project root:

```bash
docker compose up --build
```

Backend API: http://localhost:3000  
Mongo Express UI: http://localhost:8081  

## Test API

Create a user:

```bash
curl -X POST http://localhost:3000/users   -H "Content-Type: application/json"   -d '{"name":"Alice","email":"alice@test.com"}'
```

Get users:

```bash
curl http://localhost:3000/users
```

## Resume Mapping

- Backend and database are containerized using Docker.
- Docker images are built and containers are managed using Docker Compose.
- Multi-container networking is configured using Docker's internal network.
- Ports are exposed for API and database access.
- Services are tested locally using Docker Compose.

