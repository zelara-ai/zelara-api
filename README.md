# Zelara API Gateway Microservice

[![Build Status](https://github.com/zelara-ai/zelara-api/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/zelara-ai/zelara-api/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

The Zelara API Gateway Microservice serves as the central hub for managing API requests, authentication, rate limiting, caching, and billing functionalities for the Zelara AI platform.

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Service](#running-the-service)
- [Configuration](#configuration)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **API Routing**: Efficiently routes incoming API requests to appropriate worker services.
- **Authentication & Authorization**: Secure endpoints using JWT and OAuth 2.0, with RBAC implementation.
- **Rate Limiting**: Controls the rate of incoming requests based on user subscription tiers.
- **Caching**: Utilizes Redis for in-memory caching to improve performance.
- **Billing Integration**: Seamless integration with Stripe for payment processing and subscription management.
- **Logging & Monitoring**: Comprehensive logging and monitoring using industry-standard tools.
- **Error Handling**: Consistent and informative error responses across all API endpoints.

## Architecture

For detailed architectural information, refer to the [Architecture Documentation](docs/architecture.md).

## Getting Started

### Prerequisites

- **Node.js** v14.x or higher
- **Redis** v6.x or higher
- **Docker** (optional, for containerized deployment)
- **Stripe Account** for billing integration

### Installation

Clone the repository:

```bash
git clone https://github.com/zelara-ai/zelara-api.git
cd zelara-api
```

Install dependencies:

```bash
npm install
```

### Running the Service

#### Using Node.js

Set up environment variables by copying `.env.example` to `.env` and filling in the required values.

Start the server:

```bash
npm start
```

#### Using Docker

Build and run the Docker container:

```bash
docker-compose up --build
```

## Configuration

Configuration options are managed via environment variables and configuration files. Refer to the [Configuration Guide](docs/deployment-guide.md#configuration) for detailed instructions.

## API Documentation

API endpoints, request/response schemas, and error codes are documented using OpenAPI (Swagger). Access the interactive API docs at `http://localhost:3000/api-docs` when the server is running.

For detailed API specifications, see [API Documentation](docs/api-specification.md).

## Contributing

We welcome contributions from the community. Please read our [Contributing Guidelines](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) before submitting issues or pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or support, please contact the development team at [support@zelara.ai](mailto:support@zelara.ai).
