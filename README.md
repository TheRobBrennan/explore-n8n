# Explore n8n

This repository contains explorations and automations using [n8n](https://n8n.io/), a workflow automation tool. It's designed to help you quickly spin up n8n in Docker and explore its capabilities.

## Features

- 🐳 Docker Compose setup for easy n8n deployment
- 📁 Organized workflow examples with documentation
- 🔄 Persistent storage for your n8n data
- 🚀 Quick start with example workflows

## Prerequisites

- [Docker](https://www.docker.com/) (with Docker Compose)
- [Node.js](https://nodejs.org/) (v20 or higher - LTS, for development)
- [act](https://github.com/nektos/act) (for local GitHub Actions testing)

## Quick Start

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/explore-n8n.git
   cd explore-n8n
   ```

2. Start n8n with Docker Compose:

   ```bash
   docker-compose up -d
   ```

3. Access n8n at: `http://localhost:5678`

4. Import example workflows from the `workflows/examples/` directory.

## Project Structure

```text
.
├── docker-compose.yml    # Docker Compose configuration for n8n
├── workflows/            # Directory for n8n workflows
│   └── examples/         # Example workflows
│       └── hello-world/  # Example workflow
│           ├── README.md # Documentation for the example
│           └── workflow.json  # The workflow definition
└── docs/                 # Additional documentation
```

## Managing n8n

You can manage the n8n instance using the following npm scripts:

### Start n8n

```bash
npm start
```

### Stop n8n

```bash
npm stop
```

### View logs

```bash
npm run logs
```

### Restart n8n

```bash
npm run restart
```

### Reset n8n (clears all data)

```bash
npm run docker:clean
npm start
```

### Rebuild the n8n container

```bash
npm run docker:build
```

## Adding New Workflows

1. Create a new directory under `workflows/` for your workflow
2. Add a `workflow.json` file with your n8n workflow
3. Document your workflow in a `README.md` file
4. (Optional) Add screenshots to help explain the workflow

## Development

### Available Scripts

#### Docker Management

- `npm start` - Start the n8n container
- `npm stop` - Stop the n8n container
- `npm run restart` - Restart the n8n container
- `npm run logs` - View container logs
- `npm run docker:build` - Rebuild the n8n container
- `npm run docker:clean` - Remove containers and volumes (use with caution)

#### Testing

- `npm test` - Run all workflow tests
- `npm run test:workflows` - Test GitHub Actions workflows locally
- `npm run test:workflows:semantic` - Test semantic PR checks
- `npm run test:workflows:semantic:major` - Test major version bump
- `npm run test:workflows:semantic:minor` - Test minor version bump
- `npm run test:workflows:semantic:patch` - Test patch version bump
- `npm run test:workflows:semantic:invalid` - Test invalid version bump
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

## Contributing

1. Create a feature branch following the `YYYY.MM.DD/description` format
2. Make your changes
3. Submit a pull request
