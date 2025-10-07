# README

This is a small development environment for running Apache Kafka locally using Docker Compose.

It's intended to help you test and debug Kafka message flows for your projects.

This particular Kafka image runs in a single-node KRaft mode (zero-ZK), e.g. only suitable for dev/test purposes.

## Starting the Kafka service

1. Make sure Docker and Docker Compose are installed and running on your machine.

2. From the repository root run:

   ```bash
   cd infra/kafka-service
   docker compose up -d --build
   ```

3. Monitor logs (optional):

   ```bash
   docker compose logs -f
   ```

4. To stop the cluster:

   ```bash
   docker compose down
   ```

## Using the test files

The `test` files are small helper files used by the extension "Tools for Apache Kafka" for VS Code. They might work with other tools, but it's not guaranteed.

They contain human-readable instructions for producing and consuming messages to any topic (change topic, key and value as required).

IMPORTANT: Before producing/consumig messages, be sure you have created the topic using Tools for Apache Kafka extension.
