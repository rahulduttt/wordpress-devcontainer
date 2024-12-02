# WordPress Development Container

A ready-to-use development environment for WordPress using Docker containers, complete with debugging capabilities and development tools.

## Features

- PHP 8.2 with Apache server
- MySQL 8.0 database
- Xdebug pre-configured for debugging
- Development tools (git, composer, etc.)
- VS Code integration
- Hot-reload support for development

## Prerequisites

- Docker and Docker Compose
- Visual Studio Code
- VS Code Remote - Containers extension

## Quick Start

1. Clone this repository
2. Open the project in VS Code
3. When prompted, click "Reopen in Container"
4. WordPress will be available at `http://localhost:8080`

## Development Environment

The container includes:
- PHP development configuration
- Xdebug for debugging
- Composer for dependency management
- Common development tools (git, ssh, nano)
- MariaDB client for database access

## Configuration

Environment variables can be configured in `.devcontainer/.env-default`:
- WordPress port (default: 8080)
- Database credentials
- Debug mode settings

To override default settings, create a `.env` file in the `.devcontainer` directory.

## VS Code Integration

Included extensions:
- PHP IntelliSense
- PHP Debug
- DotENV support

## License

MIT
