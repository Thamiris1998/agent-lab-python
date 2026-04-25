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

## Design System

### Theme & Colors
- **Background**: Dark slate gradient (`#0f172a` to `#1e293b`)
- **Accent**: Bright blue (`#3b82f6`) for CTAs and highlights
- **Success**: Vibrant green (`#10b981`) for marked squares
- **Text**: Light slate (`#f1f5f9`) for contrast
- All colors defined in `app/static/css/app.css` with semantic class names

### CSS Utilities
Custom utility classes (Tailwind-like) in `app/static/css/app.css`:
- Flexbox: `.flex`, `.flex-col`, `.items-center`, `.justify-center`
- Grid: `.grid`, `.grid-cols-5` for bingo board
- Spacing: `.p-*`, `.px-*`, `.py-*`, `.mb-*` (not all sizes - see CSS for available)
- Typography: `.text-xs`, `.text-sm`, `.text-lg`, `.text-3xl`, `.text-4xl`, `.text-5xl`, `.font-semibold`, `.font-bold`
- Borders & Radius: `.border`, `.border-gray-300`, `.rounded`, `.rounded-lg`, `.rounded-xl`
- Shadows: `.shadow-sm`, `.shadow-xl`
- Interactive: `.transition-all`, `.duration-150`, `.animate-[bounce_0.5s_ease-out]`

### Component Styling Tips
- Use `.bingo-square` class for game squares with built-in hover and marked states
- Buttons auto-style with blue accent and smooth transitions
- Use `.bg-accent` for primary buttons, `.bg-green-600` for success states
- Maintain consistent padding: `.p-6` for major sections, `.p-4` for cards
- Add `.shadow-xl` to elevated components like modals and cards
- Use `.text-gray-500` for secondary text, `.text-white` for headings

See `app/static/css/app.css` for complete utility reference and `.github/instructions/css-utilities.instructions.md` for detailed styling practices.