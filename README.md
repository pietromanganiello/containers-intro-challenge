# Multi-Container Flask + Redis App (Docker)

## Overview
This project demonstrates a simple multi-container application using Docker and Docker Compose.

It consists of:
- A Flask web application
- A Redis database for persistent counting

The application tracks how many times the /count endpoint is visited.

---

## Tech Stack
- Python (Flask)
- Redis
- Docker
- Docker Compose

---

## How it Works
- Flask app handles HTTP requests
- Redis stores a counter (visits)
- Each request to /count increments the value
- Docker Compose manages networking between containers

---

## Project Structure

    .
    ├── app.py
    ├── Dockerfile
    ├── docker-compose.yml
    ├── requirements.txt
    └── .gitignore

---

## Run the Application

docker-compose up -d --build

Access:
http://72.61.201.12:5000
http://72.61.201.12:5000/count

---

## Persistent Storage

Redis uses a Docker volume to persist data.

Even after restarting containers:

docker-compose down
docker-compose up -d

The counter continues from the previous value.

---

## Example Output

Count: 1
Count: 2
Count: 3

---

## Key Learnings
- Multi-container architecture
- Service communication via Docker networks
- Stateless vs stateful services
- Persistent storage using Docker volumes
- Containerized Python applications
