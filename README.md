# 🎬 Movie Library Desktop App

## Overview

Movie Library is a desktop application built with **PySide5** and **FastAPI**. The project is designed as a learning-oriented but professional-grade example that demonstrates how a desktop GUI can interact with a local backend API.

The focus is on:

- Clean project structure
- Basic backend/frontend separation
- Simple but realistic development workflow

------

## Tech Stack

- **Python**: 3.10.11
- **Backend**: FastAPI + Uvicorn
- **Frontend**: PySide5
- **Testing**: Pytest

------

## Project Structure

```
movie_library/
├─ api/            # FastAPI backend
├─ gui/            # PySide5 desktop application
├─ core/           # Shared logic and models
├─ tests/          # Automated tests
├─ requirements.txt
└─ README.md
```

------

## Development Workflow

- `main` → stable branch
- `develop` → active development
- `feature/*` → feature branches

All work is tracked using **GitHub Issues**.

------

## Ticket Management

This project uses **simple, single-level tickets** (no sub-ticket numbering).

Tickets are:

- tracked as GitHub Issues
- labeled by area and type (e.g. `api`, `gui`, `feature`, `chore`)
- implemented one at a time

Ticket numbering may evolve during development and does not need to strictly match this document.

------

## Initial Ticket Scope

The initial development phase includes:

- Backend project setup
- Health check endpoint
- Environment configuration
- Movie data model
- Basic CRUD API for movies
- PySide5 GUI skeleton
- GUI-to-API integration
- Basic test setup

Exact implementation details are defined in GitHub Issues.

------

## Definition of Done

A ticket is considered done when:

- Code is committed and pushed
- Feature works as expected locally
- No existing functionality is broken

------

## Goal

The goal of this project is not to build a production-ready movie server, but to:

- practice FastAPI fundamentals
- understand desktop ↔ backend integration
- follow a clean and professional workflow

------

## Notes

This project intentionally avoids over-engineering. The focus is clarity, correctness, and learning.