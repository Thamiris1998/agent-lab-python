# Development Checklist
- [ ] Lint: `uv run ruff check .`
- [ ] Build: `uv sync`
- [ ] Test: `uv run pytest`

# Project Guidelines

## Code Style
Use Python type hints, FastAPI patterns, Jinja2 with HTMX. Reference `app/main.py` and `app/templates/`.

## Architecture
FastAPI backend with HTMX frontend (no JS frameworks). Session-based state, modular components in `app/templates/components/`.

## Build and Test
- Install: `uv sync`
- Test: `uv run pytest`
- Run: `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000`
- Lint: `uv run ruff check .`

## Conventions
HTMX for dynamics, session cookies for state, game logic in `app/game_logic.py`, static files in `app/static/`.

See `workshop/` for guides and `docs/` for docs.