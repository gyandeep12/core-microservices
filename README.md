## Core Micro-Services

<img src="/architecture.png">

These are the 3 basic components used in the most distributed Micro-Service Architecture Systems. We are using Go for creating a reverse proxy and Java for service discovery and registering profiles.

The services use heartbeats to stay registered. We use the MySQL database in service registry and profile. The applications are written using Spring Boot, with their jar files running in AWS.

The Gateway service is written in Go. Every service registers it's IP and ports to the service registry. The EC2 instance running the gateway and profile services is different from the one hosting the service registry.

We confirm that the services work using a GET and POST request using curl from the local machine.
