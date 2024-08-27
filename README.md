# DB Testing PoC with Playwright and TypeScript

This project demonstrates a Proof of Concept (PoC) for database testing within an existing Playwright and TypeScript automation framework. The application is a simple full-stack setup with a frontend registration form, backend API, and SQLite database, all containerized with Docker.

## Features

- **Frontend**: A simple HTML form with fields for first name, last name, email, password, and date of birth.
- **Backend**: Node.js server using Express that handles form submissions and stores user data in an SQLite database.
- **Database**: Lightweight, in-memory SQLite database.
- **API**: RESTful API to handle user registration and data retrieval.
- **Dockerized**: The entire application runs in a Docker container, ensuring a consistent development and testing environment.

## Getting Started

### Prerequisites

- **Docker**: Ensure Docker is installed on your machine. You can download it from [here](https://www.docker.com/products/docker-desktop).

### Build and Run the Docker Container

```bash
docker-compose up --build
```

### access the application

```bash
http://localhost:3000
```

### Verify Data in the Database


```bash
curl http://localhost:3000/api/users
```

### Project Structure

Here’s an overview of the project structure:

```markdown
db-testing-poc/
├── Dockerfile                # Docker configuration
├── docker-compose.yml        # Docker Compose configuration
├── server.js                 # Node.js Express server
├── package.json              # Node.js dependencies and scripts
├── public/                   # Static files served by Express
│   └── index.html            # Registration form HTML
└── README.md                 # This file
