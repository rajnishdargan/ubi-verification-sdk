# Build and Run Instructions

This document provides instructions on how to clone, build, and run the UBI Verification SDK both locally and using Docker.

## A. Running Locally without Docker

1. **Clone the Repository**
   ```bash
   git clone https://github.com/PSMRI/ubi-verification-sdk
   cd ubi-verification-sdk
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Run the Application**
   ```bash
   npm start
   ```
   The application will be available at `http://localhost:3000`.

   You can access the Swagger documentation at [http://localhost:3000/documentation](http://localhost:3000/documentation).

## B. Running using Docker Compose

1. **Start the Application**
   ```bash
   docker-compose up --build
   ```
   This will build and start the application along with any dependencies defined in the `docker-compose.yml` file.

2. **Run in Detached Mode**
   ```bash
   docker-compose up -d
   ```
   This will start the services in the background.

The application will be available at `http://localhost:3000`, and you can access the Swagger documentation at [http://localhost:3000/documentation](http://localhost:3000/documentation).
