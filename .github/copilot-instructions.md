# Copilot Instructions for Ecommerce Microservices Platform

## Big Picture Architecture
- This platform is a microservices-based eCommerce system. Each service (Catalog, Cart, Checkout, User, Order, Admin) is independently developed and documented in `eCommerce-docs/architecture/system-overview.md`.
- Services communicate via REST APIs, with a Gateway (optional) aggregating endpoints for the frontend.
- The Catalog service (in `eCommerce-catalog/`) manages products and categories, using FastAPI, SQLAlchemy, and PostgreSQL.

## Developer Workflows
- **Local Development (Catalog Service):**
  - Create a Python virtual environment and install dependencies: `python3 -m venv venv && source venv/bin/activate && pip install -r requirements.txt`
  - Start the API: `uvicorn app.main:app --reload`
  - API docs: [http://localhost:8000/docs](http://localhost:8000/docs)
- **Docker:**
  - Build and run: `docker build -t ecommerce-catalog . && docker run --env-file .env -p 8000:8000 ecommerce-catalog`
- **Testing:**
  - Run tests with pytest: `pytest tests/`
- **Database:**
  - PostgreSQL required. Connection string configured via `.env` (see `.env.example`).

## Project-Specific Patterns & Conventions
- **FastAPI Structure:**
  - API endpoints in `app/main.py`.
  - Business logic in `app/crud.py`.
  - Data models in `app/models.py` (SQLAlchemy) and `app/schemas.py` (Pydantic).
  - Database session management in `app/db.py`.
- **API Contracts:**
  - OpenAPI spec for Catalog in `eCommerce-docs/api/catalog-openapi.yaml`.
  - Update API docs/specs when endpoints change.
- **Documentation:**
  - All architecture, onboarding, and specs are in `eCommerce-docs/`.
  - Use diagrams for system explanations (see `architecture/system-overview.md`).
  - Glossary of domain terms in `glossary.md`.
- **Contribution:**
  - Follow onboarding guide in `onboarding/getting-started.md`.
  - PRs should update relevant docs/specs when code changes affect APIs or architecture.

## Integration Points & External Dependencies
- **PostgreSQL** for persistent storage (Catalog service).
- **FastAPI** for REST API.
- **SQLAlchemy** for ORM.
- **Docker** for containerization.
- **pytest** for testing.

## Examples
- To add a new product endpoint, update `app/main.py`, `app/crud.py`, `app/schemas.py`, and the OpenAPI spec in `api/catalog-openapi.yaml`.
- To add a new microservice, create a new directory, document its API in `eCommerce-docs/api/`, and update the system diagram in `architecture/system-overview.md`.

---

For questions about architecture or conventions, see `eCommerce-docs/architecture/system-overview.md` and `eCommerce-docs/onboarding/getting-started.md`.
