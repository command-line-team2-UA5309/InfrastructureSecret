# Infrastructure

This repository contains a Docker Compose setup for:

- Two PostgreSQL databases (auth-db, map-db)
- Django backend for authentication (auth-service)
- Django backend for map (map-service)
- Vue frontend (frontend)
- NGINX reverse proxy to route requests

## Submodules

This project uses Git submodules for backend and frontend.
After cloning, initialize them:

- DjangoBackend - DjangoBackend folder
- MapService - MapService folder
- VueFrontend - VueFrontend folder

## Quick Start

1. Clone this repository with submodules:

   ```sh
   git clone --recurse-submodules
   ```

   If you already cloned without --recurse-submodules, initialize them:

   ```sh
   git submodule update --init --recursive
   ```

2. Run

   ```sh
   git submodule update --remote
   ```

   to update submodules to point to latest commits.

3. Copy `.env.example` to `.env` and fill in your variables.

4. Build and start all services:

   ```sh
   docker compose up --build
   ```

## How to set up pre-commit hooks

1. Install pre-commit from <https://pre-commit.com/#install>
2. Run `pre-commit install`
3. Auto-update the config to the latest version `pre-commit autoupdate`
