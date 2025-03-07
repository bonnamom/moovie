# MoovieAPI - Symfony Backend & Vue.js Frontend

## Description

This project is a streaming platform with a **Symfony** backend API and a **Vue.js** frontend. It is **dockerized** for easy setup.

## Prerequisites

- **Docker**
- **Node.js** and **npm**
- **Git**
  
## Setup

### 1. Clone the repository

SSH
```bash
git clone git@github.com:bonnamom/moovie.git
```

HTTPS
```bash
https://github.com/bonnamom/moovie.git
```

### 2. Environment configuration

Create a .env.local file in the moovieAPI directory. You'll need to configure your environment variables (like database credentials). Contact me for the necessary values (username, password, etc.).

### 3. Build docker containers

To build and start the Docker containers, use the following command:
```bash
docker compose up
```
This will set up the containers for the Symfony backend, the Vue.js frontend, and the database.

### 4. Database setup

 - Create the database
```bash
docker compose exec php php bin/console doctrine:database:create
```

 - Run database migrations:
```bash
docker-compose exec php php bin/console doctrine:migrations:migrate
```

### 5. Vue.js

Install dependencies
```bash
cd moovie/moovieVUE
npm install
```

Run vue
```bash
npm run dev
```

### 6. Access to the app

Backend API: http://localhost:8000
Frontend Vue.js: http://localhost:3000
Adminer: http://localhost:8082
