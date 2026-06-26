# Design: Calculator Module

## Architecture

Two-module layout:

```
src/myapp/
├── __init__.py        # Package marker + version
├── calculator.py      # Pure functions (no dependencies)
└── cli.py             # argparse CLI, imports from calculator
```

## Design Decisions

### 1. Calculator as pure functions

The math operations are implemented as standalone functions in `calculator.py`
with no class or state. This keeps the module testable and importable without
side effects.

### 2. CLI via argparse

Python's built-in `argparse` is used — no third-party CLI libraries needed.
The interface takes three positional arguments: `<operation> <a> <b>`.

### 3. Error handling

- Division by zero → `ValueError` with message `"Cannot divide by zero"`
- CLI catches `ValueError`, prints to stderr, exits with code 1
- Invalid operation names are rejected by argparse's `choices` parameter

### 4. Type hints

All public functions use type hints (`float`) for clarity and IDE support.

## File Structure

```
src/myapp/
├── __init__.py         # Package marker + version
├── calculator.py       # Core math operations (add, subtract, multiply, divide)
└── cli.py              # CLI entry point with argparse
```

## API Surface

See `openspec/specs/calculator.md` for full API surface.
