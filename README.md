# My Example Voting App

This repository was created by copying starter code from the `example-voting-app` repository. It demonstrates the deployment and orchestration of a multi-container application using Docker Compose. The application is designed to showcase a scalable and distributed architecture by integrating multiple services into a cohesive system.

## Getting Started

### Prerequisites

Before starting, ensure you have the following installed:

1. [Docker Desktop](https://www.docker.com/products/docker-desktop) for Mac or Windows (Docker Compose is included).
2. On Linux, make sure you have the latest version of [Docker Compose](https://docs.docker.com/compose/install/).
3. A modern web browser to access the application.

### Running the Application

1. **Clone this repository**:

   ```shell
   git clone https://github.com/your-username/my-example-voting-app.git
   cd my-example-voting-app

2. **Run the application using Docker Compose**:
   ```shell
   docker compose up --build

### Accessing the Applicaiton: 
* Voting app: http://localhost:5001
* Results app: http://localhost:5002

### Stopping the Application
* To greacefully stop the containers, run:
  ```shell
    docker compose down

## Architecture

![Architecture diagram](architecture.excalidraw.png)

* A front-end web app in [Python](/vote) which lets you vote between two options
* A [Redis](https://hub.docker.com/_/redis/) which collects new votes
* A [.NET](/worker/) worker which consumes votes and stores them in…
* A [Postgres](https://hub.docker.com/_/postgres/) database backed by a Docker volume
* A [Node.js](/result) web app which shows the results of the voting in real time

## Notes

The voting application only accepts one vote per client browser. It does not register additional votes if a vote has already been submitted from a client.

This isn't an example of a properly architected perfectly designed distributed app... it's just a simple
example of the various types of pieces and languages you might see (queues, persistent data, etc), and how to
deal with them in Docker at a basic level.
=======
# my-example-voting-app
This repository demonstrates the deployment and orchestration of a multi-container application using Docker Compose. It serves as an example of designing and managing a scalable, layered architecture by integrating various services into a cohesive, functional system.
>>>>>>> 79dd1a2b485a78ca5953740710d10865292a6c4d
