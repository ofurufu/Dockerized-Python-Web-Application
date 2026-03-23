# Dockerized Python Web Application  
### From Single-Container Build to Multi-Container Production-Style Stack

A hands-on Docker project that demonstrates the evolution of a Python Flask application from a basic single-container deployment to a more production-minded multi-container stack using Docker Compose, Redis, persistent storage, and container hardening techniques.

This project was built as part of my DevOps learning journey to develop practical, portfolio-ready Docker skills aligned with real-world engineering workflows.

---

## Project Summary

This repository showcases a staged Docker learning and implementation path across five progressively improved versions of the same application.

The project begins with containerizing a simple Flask application and then evolves through:

- development-friendly bind mounts
- Docker-managed persistent storage
- multi-container orchestration with Docker Compose
- service-to-service communication with Redis
- image optimization and runtime hardening using a multi-stage build, Gunicorn, and a non-root user

The goal of this project is not just to “run a container,” but to demonstrate practical Docker knowledge in a way that reflects how containerized applications mature in real DevOps environments.

---

## Why This Project Matters

Docker is one of the most important tools in modern DevOps and cloud engineering. It enables teams to package applications consistently, improve development workflows, standardize deployments, and prepare workloads for platforms such as ECS, EKS, and other container-based systems.

This project demonstrates my ability to:

- build and run Docker images from custom Dockerfiles
- manage container lifecycle with Docker CLI
- use bind mounts for development workflows
- persist application data with Docker volumes
- define and run multi-container applications with Docker Compose
- connect services through container networking
- improve image quality with multi-stage builds
- run containers more securely using a non-root runtime user
- transition from development-style containers toward production-minded container design

---

## Tech Stack

- Docker
- Docker Compose
- Python 3.12
- Flask
- Redis
- Gunicorn

---

## Final Architecture (v5)

The latest version of the project includes:

- **web** — Python Flask application served by Gunicorn
- **redis** — Redis backend service
- **named volume** — persistent application file storage
- **Docker Compose** — multi-container orchestration
- **multi-stage Dockerfile** — cleaner image build workflow
- **non-root runtime user** — improved container security posture

---

## Project Evolution

### v1 — Basic Dockerized Flask Application
Initial version of the project focused on Docker fundamentals.

**Key highlights**
- containerized a simple Flask application
- created a custom Dockerfile
- built and ran the image with Docker CLI
- practiced logs, inspect, port mapping, and container lifecycle operations

**Skills demonstrated**
- Docker images vs containers
- Dockerfile basics
- image building and tagging
- port publishing
- container inspection and logs

---

### v2 — Bind-Mounted Development Workflow
Added a development-oriented workflow using a bind mount.

**Key highlights**
- mounted the local project directory into the container
- enabled host-container source sharing
- improved iteration speed during local development

**Skills demonstrated**
- bind mounts
- host/container file sharing
- development workflow improvement
- debugging with `docker logs`, `docker inspect`, and `docker exec`

---

### v3 — Persistent Storage with Docker Volumes
Introduced persistent application data using a Docker-managed named volume.

**Key highlights**
- added file write and read endpoints
- mounted a named volume into the container
- validated that application data survives container removal and recreation

**Skills demonstrated**
- named volumes
- persistent data management
- separation of container lifecycle and data lifecycle

---

### v4 — Multi-Container Application with Docker Compose
Expanded the application into a multi-service stack.

**Key highlights**
- added a Redis backend service
- defined the full stack in `docker-compose.yml`
- connected services using Compose networking
- retained persistent file storage with a named volume

**Skills demonstrated**
- Docker Compose
- multi-container orchestration
- service-name networking
- environment-based configuration
- centralized stack definition

---

### v5 — Production-Minded Optimization and Hardening
Improved the application image and runtime approach for a more production-style setup.

**Key highlights**
- replaced Flask development server with Gunicorn
- introduced a multi-stage Dockerfile
- ran the container as a non-root user
- removed development-style bind mounts from runtime
- added restart behavior in Compose
- preserved Redis integration and persistent storage

**Skills demonstrated**
- multi-stage builds
- non-root container execution
- production-style runtime server
- cleaner runtime image design
- container hardening fundamentals

---

## Key Features

- Custom Dockerfile-based application build
- Docker image versioning across multiple stages of project maturity
- Persistent application file storage using Docker volumes
- Redis-backed visit counter
- Multi-container orchestration with Docker Compose
- Production-minded Gunicorn runtime
- Non-root application container
- Health and runtime test endpoints

---

## Repository Structure

```text
dockerized-python-web-application/
├── app.py
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
└── README.md