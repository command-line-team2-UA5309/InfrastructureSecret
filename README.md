# Infrastructure

This repository contains a Docker Compose setup for:

- Two PostgreSQL databases (auth-db, map-db)
- Django backend for authentication (auth-service)
- Django backend for map (map-service)
- Vue frontend (frontend)

## Submodules

This project uses Git submodules for backend and frontend.
After cloning, initialize them:

- DjangoBackend - DjangoBackend folder
- MapService - MapService folder
- VueFrontend - VueFrontend folder (branch feature/CLT-60-auth-frontend)

## Quick Start

1. Clone this repository with submodules:

   ```git clone --recurse-submodules <this-repo-url>```

   If you already cloned without --recurse-submodules, initialize them:

   ```git submodule update --init --recursive```

2. Copy `.env.example` to `.env` and fill in your variables.

3. Build and start all services:

   ```docker compose up --build```

## How to set up pre-commit hooks

1. Install pre-commit from <https://pre-commit.com/#install>
2. Run `pre-commit install`
3. Auto-update the config to the latest version `pre-commit autoupdate`
