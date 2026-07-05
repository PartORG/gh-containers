# PartORG/gh-containers

**A Node.js backend for managing containerized applications with MongoDB and Express**

[![Node.js](https://img.shields.io/badge/node.js-16.x-blue.svg)] [![License](https://img.shields.io/badge/license-ISC-green.svg)] [![Tests](https://img.shields.io/github/actions/workflow/status/PartORG/gh-containers/deploy.yml?branch=main&label=tests)] [![Docker](https://img.shields.io/docker/pulls/partorg/gh-containers)] [![GitHub stars](https://img.shields.io/github/stars/PartORG/gh-containers?style=social)]

## Introduction

`gh-containers` is a robust Node.js backend designed to manage containerized applications using MongoDB and Express. It provides a scalable and efficient solution for developers looking to build modern web applications with ease.

This project aims to simplify the development process by offering a pre-configured environment, comprehensive testing, and easy deployment options. Whether you're building a microservices architecture or a monolithic application, `gh-containers` has got you covered.

## Table of Contents

- [Features](#features)
- [How It Works](#how-it-works)
- [Technology Stack](#technology-stack)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Development](#development)
- [Testing](#testing)
- [Limitations](#limitations)
- [License](#license)

## Features

### 1. Express Framework
**What it does:** Provides a robust framework for building web applications and APIs.
**Why it exists:** Simplifies the development process by abstracting common tasks.
**Why it is useful:** Enables developers to focus on business logic rather than infrastructure.

### 2. MongoDB Integration
**What it does:** Manages data storage and retrieval using MongoDB.
**Why it exists:** Offers a scalable and flexible database solution.
**Why it is useful:** Provides high performance and easy querying capabilities.

### 3. Docker Support
**What it does:** Containerizes the application for consistent deployment across environments.
**Why it exists:** Ensures consistency and ease of deployment.
**Why it is useful:** Simplifies the development and production workflows.

## How It Works

`gh-containers` follows a modular architecture, with each component responsible for specific tasks. The main components are:

- **Express Server**: Handles incoming HTTP requests and routes them to appropriate handlers.
- **MongoDB Database**: Stores application data using MongoDB's flexible schema design.
- **Docker Containerization**: Packages the application and its dependencies into a container for easy deployment.

## Technology Stack

| Technology | Purpose |
|------------|---------|
| Node.js    | Runtime environment for JavaScript applications. |
| Express    | Web framework for building APIs and web applications. |
| MongoDB    | NoSQL database for storing application data. |
| Docker     | Containerization platform for packaging and deploying applications. |

## Requirements

- **Node.js**: Version 16.x
- **Docker**: For containerized deployment (optional)

## Installation

To install `gh-containers`, follow these steps:

```bash
# Clone the repository
git clone https://github.com/PartORG/gh-containers.git

# Navigate to the project directory
cd gh-containers

# Install dependencies
npm install
```

## Configuration

The following environment variables can be configured in a `.env` file or directly in the Dockerfile:

- `MONGODB_CONNECTION_PROTOCOL`: MongoDB connection protocol (default: `mongodb+srv`)
- `MONGODB_DB_NAME`: Name of the database (default: `gha-demo1`)
- `MONGODB_CLUSTER_ADDRESS`: Address of the MongoDB cluster (default: `cluster0.ntrwp.mongodb.net`)
- `MONGODB_USERNAME`: Username for MongoDB authentication
- `MONGODB_PASSWORD`: Password for MongoDB authentication

## Quick Start

To start the application, run:

```bash
npm run start
```

This will start the Express server and connect to the MongoDB database.

## Usage

Here are some example commands and usage scenarios:

### Starting the Application

```bash
npm run start
```

### Running Tests

```bash
npm run test
```

### Accessing the API

You can access the API endpoints using tools like `curl` or Postman. For example, to get a list of events:

```bash
curl http://localhost:3000/events
```

## Project Structure

```
.
├── .DS_Store
├── .github/workflows/deploy.yml
├── .gitignore
├── .vscode/settings.json
├── Dockerfile
├── app.js
├── data/database.js
├── package-lock.json
├── package.json
├── playwright.config.js
└── routes/events.js
```

- **app.js**: Main entry point of the application.
- **data/database.js**: Handles database connection and operations.
- **routes/events.js**: Defines API endpoints for managing events.

## Development

To contribute to `gh-containers`, follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/AmazingFeature`).
3. Make your changes and commit them (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## Testing

Tests are written using Playwright for end-to-end testing:

```bash
npm run test
```

This will execute all tests defined in the `tests/events-api.spec.js` file.

## Limitations

- **MongoDB Atlas**: The project uses MongoDB Atlas, which may have limitations based on the free tier.
- **Docker Deployment**: While Docker is supported, it requires Docker to be installed and configured.

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.