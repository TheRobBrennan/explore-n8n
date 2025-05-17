# Explore n8n

This repository contains explorations and automations using [n8n](https://n8n.io/), a workflow automation tool.

## Prerequisites

- [Node.js](https://nodejs.org/) (v20 or higher - LTS)
- [Docker](https://www.docker.com/) (for local services and workflow testing)
- [act](https://github.com/nektos/act) (for local GitHub Actions testing)

## Quick Start

```bash
# Install project dependencies
npm install
```

## Development

### Available Scripts

- `npm test` - Run all workflow tests
- `npm run test:workflows` - Test GitHub Actions workflows locally
- `npm run test:workflows:semantic` - Test semantic PR checks
- `npm run test:workflows:version` - Test version bump workflow
- `npm run test:workflows:merge` - Test merge workflow

### Testing GitHub Actions Locally

We recommend using [act](https://github.com/nektos/act) to test GitHub Actions workflows locally before pushing changes.

Prerequisites for macOS:

- Homebrew
- Docker Desktop (must be running)

```sh
# Install act using Homebrew
brew install act

# Verify installation
act --version
```

### Running Tests

```bash
# Run all workflow tests
npm run test:workflows
```

## Contributing

1. Create a feature branch following the `YYYY.MM.DD/description` format
2. Make your changes
3. Submit a pull request
