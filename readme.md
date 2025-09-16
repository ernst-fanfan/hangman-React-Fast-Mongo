This is hangman app with GUI
multiplayer
Developed in docker:
to run text:: 
- docker-compose build
- docker-compose up tests
to run::
- docker-compose build
- docker-compose up
# Hangman Web App

This is a full-stack Hangman game web application, designed to run locally using Docker Compose. The project features:

- **Frontend:** React
- **Backend:** FastAPI (Python)
- **Database:** MongoDB
- **Authentication:** Apple and Google OAuth
- **Feature:** Scoreboard

## Features

- Play classic Hangman in your browser
- Sign in with Apple or Google
- Track high scores on a persistent scoreboard

## Project Structure

```
frontend/      # React app
backend/       # FastAPI app
docker-compose.yaml
readme.md
```

## Prerequisites

- [Docker](https://www.docker.com/products/docker-desktop)
- [Docker Compose](https://docs.docker.com/compose/)

## Getting Started

1. **Clone the repository:**
	```bash
	git clone <your-repo-url>
	cd hangman
	```

2. **Configure OAuth Credentials:**
	- Set up Apple and Google OAuth credentials for local development.
	- Add your client IDs and secrets to the backend environment variables (see `backend/.env.example`).

3. **Start all services:**
	```bash
	docker-compose up --build
	```

4. **Access the app:**
	- Frontend: [http://localhost:3000](http://localhost:3000)
	- Backend API: [http://localhost:8000/docs](http://localhost:8000/docs) (Swagger UI)
	- MongoDB: [mongodb://localhost:27017](mongodb://localhost:27017)

## Docker Compose Overview

The `docker-compose.yaml` file defines three services:

- **frontend:** React app (Node.js)
- **backend:** FastAPI app (Python)
- **mongodb:** MongoDB database

All services are networked together for seamless local development.

## Authentication

Apple and Google OAuth are implemented using FastAPI social authentication libraries (e.g., `fastapi-users`, `authlib`).

## Scoreboard

The scoreboard tracks user scores and is stored in MongoDB. Only authenticated users can submit scores.

## Example Usage

1. Register or sign in with Apple/Google.
2. Play Hangman and try to beat your high score!
3. View the scoreboard to see top players.

## Screenshots

> _Add screenshots here_

## API Documentation

Interactive API docs are available at [http://localhost:8000/docs](http://localhost:8000/docs) when the backend is running.

## Development

- Frontend: `cd frontend && npm start`
- Backend: `cd backend && uvicorn main:app --reload`
- Database: MongoDB runs in Docker

## Notes

- This app is for local use only. No production deployment is included.
- Make sure to configure your OAuth credentials for local development.

---
_Happy coding!_
Structure:
