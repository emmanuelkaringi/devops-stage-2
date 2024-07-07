# Full-Stack FastAPI and React Template

Welcome to the Full-Stack FastAPI and React template repository. This repository serves as a demo application for interns, showcasing how to set up and run a full-stack application with a FastAPI backend and a ReactJS frontend using ChakraUI.

## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template locally, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)

To get started with this template with **Docker**, please follow the below instructions:

### Prerequisites
- **Docker** - Ensure Docker is installed on your machine. You can download and install Docker from [Docker's official website](https://www.docker.com/get-started/).

1. **Set Up Environment Variables** - Create a `.env` file in the root directory of the project. Fill in the necessary environment variables into this file. For example:
    ```txt
    POSTGRES_USER=john
    POSTGRES_PASSWORD=password
    POSTGRES_DB=app
    ```
2. **Build Docker Containers** - Navigate to the root directory `cd devops-stage-2` and run: `docker-compose build`
3. **Start Docker Containers** - Once the build process completes, start the Docker containers - `docker-compose up -d` or `docker-compose up`
4. **Stop the Application** - To stop the Docker containers and remove containers, networks, volumes, and images created by `docker-compose up -d`, run: `docker-compose down`. If you used `docker-compose up` press Ctrl+C in the terminal where Docker is running, and then run: `docker-compose down`