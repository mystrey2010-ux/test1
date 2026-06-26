# AGENTS.md

## Project Rules

- Python 3.12+ only
- Use `hatchling` as the build backend (see `pyproject.toml`)
- Type hints required on all public functions
- Docstrings required on all public functions and classes
- No unnecessary comments
- Prefer existing patterns over new abstractions
- Always run `python -m pytest` after changes to tests
- Commit messages follow conventional commits format

## OpenSpec Workflow

This project uses OpenSpec for spec-driven development. Every change must:

1. Create a proposal under `openspec/changes/<change_id>/proposal.md`
2. Include design decisions in `design.md`
3. List concrete tasks mapped to acceptance criteria in `tasks.md`
4. Update or create capability specs in `openspec/specs/` after implementation

## Environment

- Conda environment: `test1` (same as project name)
- Create with: `conda create -n test1 python=3.12`
- Activate with: `conda activate test1`
