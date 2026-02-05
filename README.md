# 🎬 Movie Library Server (Desktop)

**Target Python Version:** 3.10.11
**Stack:** PySide5 + FastAPI + SQLite

------

## 1. Project Objective

Build a **professional desktop application** that allows managing a local movie library and exposing that information through a **FastAPI API**, fully controlled from a **PySide5 GUI**.

The project is designed to simulate a **real-world working environment**, applying proper architecture, version control, and incremental deliverables.

------

## 2. Non‑Negotiable Principles

- Python **3.10.11** (pinned version)
- Mandatory use of **venv**
- **FastAPI = backend only** (no UI logic)
- **PySide5 = frontend only** (no business logic)
- Communication **exclusively via HTTP**
- **SQLite** as the database
- Reproducible, version-controlled code

------

## 3. Definition of Done (DoD)

A ticket is considered **done** only if:

- The code works correctly
- The project can be run from scratch following the README
- Commits are clear and atomic
- Existing functionality is not broken
- You can explain what you did and why

------

## 4. Git Workflow (Mandatory)

### Main branches

```
main        → stable, usable code only
develop     → feature integration branch
```

### Working branches

```
feature/<descriptive-name>
bugfix/<descriptive-name>
docs/<descriptive-name>
```

**Examples:**

- `feature/api-movies-crud`
- `feature/gui-movie-list`
- `bugfix/api-validation`

Direct work on `main` is forbidden.

------

## 5. Roadmap by Sprints

------

### 🟦 Sprint 0 — Initial Setup

**Goal:** Solid technical foundation

#### 🎫 Ticket 0.1 — Initialize repository

- Create GitHub repository
- Add `.gitignore`
- Create initial `README.md`

------

#### 🎫 Ticket 0.2 — Python environment

- Create virtual environment
- Create `requirements.txt`
- Create `requirements-dev.txt`
- Verify installation with Python 3.10.11

------

### 🟦 Sprint 1 — FastAPI Basics

**Goal:** Learn FastAPI core concepts

#### 🎫 Ticket 1.1 — Minimal FastAPI app

**Branch:** `feature/api-base`

- Create `FastAPI()` instance
- `/health` endpoint

```http
GET /health → { "status": "ok" }
```

------

#### 🎫 Ticket 1.2 — Pydantic Models

**Branch:** `feature/api-models`

`Movie` model fields:

- id
- title
- year
- duration

------

#### 🎫 Ticket 1.3 — In-memory CRUD

**Branch:** `feature/api-movies-crud`

Endpoints:

```http
GET    /movies
POST   /movies
GET    /movies/{id}
DELETE /movies/{id}
```

No database yet.

------

### 🟦 Sprint 2 — Persistence

**Goal:** Real, durable state

#### 🎫 Ticket 2.1 — SQLite setup

**Branch:** `feature/db-sqlite`

- Create database
- Automatic initialization

------

#### 🎫 Ticket 2.2 — Repository Pattern

**Branch:** `feature/db-repository`

- Separate data access layer
- Encapsulated CRUD

------

#### 🎫 Ticket 2.3 — API + DB integration

**Branch:** `feature/api-db-integration`

- Replace in-memory storage
- Preserve existing endpoints

------

### 🟦 Sprint 3 — PySide5 GUI

**Goal:** Decoupled frontend

#### 🎫 Ticket 3.1 — Base GUI

**Branch:** `feature/gui-base`

- Main window
- Initial layout

------

#### 🎫 Ticket 3.2 — HTTP client

**Branch:** `feature/gui-http-client`

- Use `httpx`
- Consume `/health`

------

#### 🎫 Ticket 3.3 — Movie list view

**Branch:** `feature/gui-movie-list`

- Table view
- Data loaded from API

------

### 🟦 Sprint 4 — Full Integration

**Goal:** Usable application

#### 🎫 Ticket 4.1 — Add movies from GUI

**Branch:** `feature/gui-add-movie`

- GUI form
- POST `/movies`

------

#### 🎫 Ticket 4.2 — Server control

**Branch:** `feature/gui-server-control`

- Start/stop FastAPI
- Dedicated thread

------

### 🟦 Sprint 5 — Quality & Closure

**Goal:** Professional finish

#### 🎫 Ticket 5.1 — Error handling

**Branch:** `feature/api-error-handling`

- Proper status codes
- Clear validations

------

#### 🎫 Ticket 5.2 — Basic tests

**Branch:** `feature/api-tests`

- Health check
- API CRUD tests

------

#### 🎫 Ticket 5.3 — Final documentation

**Branch:** `docs/readme`

- How to run the project
- Architecture overview
- Technical decisions

------

## 6. Expected Final Structure

```
movie_library/
├─ api/
│  ├─ main.py
│  ├─ routes.py
│  └─ models.py
├─ gui/
│  └─ main_window.py
├─ core/
│  └─ repository.py
├─ tests/
├─ requirements.txt
├─ requirements-dev.txt
└─ README.md
```