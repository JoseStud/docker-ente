# Docker Compose Application

This project sets up a Docker Compose application that includes multiple services, including a reverse proxy using Nginx. The services defined in this application are:

- **socat**: A command-line based utility that establishes two bidirectional byte streams and transfers data between them.
- **MinIO**: A high-performance, S3 compatible object storage.
- **Museum**: A custom service (details to be defined).
- **Postgres**: A powerful, open-source object-relational database system.
- **EnteWeb**: A web application service (details to be defined).
- **Vaultwarden**: A self-hosted password manager.
- **MySQL**: A widely used open-source relational database management system.

## Prerequisites

- Docker installed on your machine.
- Docker Compose installed on your machine.

## Setup Instructions

1. Clone the repository or download the project files to your local machine.
2. Navigate to the project directory:
   ```
   cd docker-compose-app
   ```
3. Ensure that your Docker daemon is running.
4. Start the application using Docker Compose:
   ```
   docker-compose up -d
   ```
   This command will start all the defined services in detached mode.

## Accessing the Services

- The Nginx reverse proxy will route traffic for the domain `25thjose.online`. Ensure that your DNS settings are configured to point to the server running this application.
- Each service can be accessed through the specified ports as defined in the `docker-compose.yml` file.

## Stopping the Application

To stop the application, run:
```
docker-compose down
```

This command will stop and remove all the containers defined in the `docker-compose.yml` file.

## Additional Notes

- Make sure to configure the Nginx settings in `nginx/nginx.conf` to properly route requests to the respective services.
- Review the individual service documentation for more details on configuration and usage.