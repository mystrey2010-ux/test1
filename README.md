# test1 — OpenSpec Example Project

This project demonstrates the **OpenSpec (spec-driven development)** workflow using a simple Python CLI calculator application (`myapp`).

## What is OpenSpec?

OpenSpec is a methodology that bridges the gap between high-level requirements and low-level implementation by enforcing a structured documentation flow. Instead of jumping straight into coding, changes follow a strict lifecycle:

1.  **Proposal:** Defines *what* needs to be built and *why*.
2.  **Design:** Outlines *how* it will be built (architecture, API surface).
3.  **Tasks:** Breaks the work down into small, verifiable chunks.
4.  **Implementation:** The actual code writing.
5.  **Archive:** Once verified, the proposal/design/tasks are moved to `archive/` to keep the workspace clean while preserving history.

## Project Structure

```text
test1/
├── .gitignore
├── AGENTS.md          # Local rules and environment info
├── pyproject.toml     # Python package config (hatchling)
├── README.md          # This file
├── openspec/
│   ├── config.yaml    # OpenSpec configuration
│   ├── specs/         # Current capability specs
│   │   └── calculator.md
│   ├── changes/       # Active work in progress
│   └── archive/       # Completed work (history)
│       └── add-calculator/  # Example: The calculator feature we just built
└── src/
    └── myapp/         # Source code
        ├── __init__.py
        ├── cli.py
        └── calculator.py
```

## Current Status: `add-calculator` (Archived)

The **Calculator** feature has been completed and archived. You can review the full lifecycle of this change in:
*   [Proposal](openspec/archive/add-calculator/proposal.md)
*   [Design](openspec/archive/add-calculator/design.md)
*   [Tasks](openspec/archive/add-calculator/tasks.md)

## Usage

To use the calculator CLI:

```bash
# Activate environment (if not already active)
conda activate test1

# Run examples
myapp add 3 4        # Output: 7.0
myapp subtract 10 5  # Output: 5.0
myapp multiply 2 6   # Output: 12.0
myapp divide 10 2    # Output: 5.0
```

## Getting Started (New Changes)

To add a new feature, follow the OpenSpec workflow:

1.  Create a directory in `openspec/changes/<change-id>/`.
2.  Write `proposal.md` (What & Why).
3.  Write `design.md` (How).
4.  Write `tasks.md` (Steps).
5.  Implement the code in `src/myapp/`.
6.  Update `openspec/specs/` if requirements change.
7.  Move the change directory to `openspec/archive/` upon completion.
