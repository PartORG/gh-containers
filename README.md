# gh-containers

A backend application built with JavaScript and Express.js, designed to interact with MongoDB for data storage. This project includes automated testing using Playwright and is containerized using Docker.

## Table of Contents
1. [Features](#features)
2. [How It Works](#how-it-works)
3. [Technology Stack](#technology-stack)
4. [Requirements](#requirements)
5. [Installation](#installation)
6. [Configuration](#configuration)
7. [Quick Start](#quick-start)
8. [Usage](#usage)
9. [Project Structure](#project-structure)
10. [Development](#development)
11. [Testing](#testing)
12. [Limitations](#limitations)
13. [License](#license)

## Features
### Express.js
- **What it does:** Handles routing and request handling for the application.
- **Why it exists:** Provides a robust framework for building web applications in Node.js.
- **Why it is useful:** Simplifies the process of creating scalable and maintainable backend services.

### MongoDB
- **What it does:** Manages data storage and retrieval.
- **Why it exists:** Offers high performance, high availability, and automatic scaling.
- **Why it is useful:** Provides a flexible schema for storing complex data structures.

## How It Works
The application uses Express.js to define routes and handle incoming requests. MongoDB is used to store and retrieve data. The Dockerfile sets up the environment with Node.js 16 and installs dependencies from `package.json`.

## Technology Stack

| Technology | Purpose |
|------------|---------|
| **Node.js** | Runtime environment for executing JavaScript code on the server side. |
| **Express.js** | Framework for building web applications in Node.js. |
| **MongoDB** | NoSQL database for storing and retrieving data. |
| **Playwright** | End-to-end testing framework for modern web applications. |

## Requirements
- Node.js 16 or higher
- MongoDB instance

## Installation
To install the project, follow these steps:

```bash
git clone https://github.com/PartORG/gh-containers.git
cd gh-containers
npm install
```

## Configuration
The following environment variables are used:

- `MONGODB_CONNECTION_PROTOCOL`: Protocol for connecting to MongoDB.
- `MONGODB_DB_NAME`: Name of the database.
- `MONGODB_CLUSTER_ADDRESS`: Address of the MongoDB cluster.
- `MONGODB_USERNAME`: Username for authenticating with MongoDB.
- `MONGODB_PASSWORD`: Password for authenticating with MongoDB.

These variables can be set in a `.env` file or directly in your environment.

## Quick Start
To start the application, run:

```bash
npm run start
```

To run tests, use:

```bash
npm run test
```

## Usage
Here are some example commands and usage scenarios:

- **Starting the server:**
  ```bash
  npm start
  ```

- **Running tests:**
  ```bash
  npm run test
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
├── routes/events.js
└── tests/events-api.spec.js
```

- **app.js:** Main entry point of the application.
- **data/database.js:** Handles database operations using MongoDB.
- **routes/events.js:** Defines routes for handling events.
- **tests/events-api.spec.js:** Contains test cases for the API endpoints.

## Development
The development workflow involves setting up a Node.js environment, installing dependencies, and running tests. The Dockerfile automates this process by building an image with all necessary dependencies installed.

## Testing
Automated testing is performed using Playwright. Test cases are located in `tests/events-api.spec.js`.

## Limitations
- The application assumes MongoDB is accessible at the specified connection string.
- No authentication mechanism is implemented for accessing the API endpoints.

## License
This project is licensed under the ISC license.