# Tasks: Add Calculator Module

## Task 1: Create calculator module

**Description:** Create `src/myapp/calculator.py` with add, subtract, multiply, and divide functions. Each function takes two `float` arguments and returns a `float`.

**Acceptance:** AC-1

**Evidence:** File exists with all four functions, type hints present, docstrings present.

---

## Task 2: Create CLI entry point

**Description:** Create `src/myapp/cli.py` with argparse-based CLI. Accept `<operation> <a> <b>` arguments where operation is one of add, subtract, multiply, divide. Print result to stdout.

**Acceptance:** AC-1, AC-2

**Evidence:** `python -m myapp.cli add 3 4` prints `7.0`.

---

## Task 3: Add error handling

**Description:** Handle division by zero with a clear error message. Invalid inputs should produce non-zero exit codes. CLI prints errors to stderr.

**Acceptance:** AC-3

**Evidence:** `python -m myapp.cli divide 1 0` prints error to stderr and exits with code 1.

---

## Task 4: Write unit tests

**Description:** Create `tests/` directory with test file for calculator module. Test all four operations including edge cases (zero operands, negative numbers).

**Acceptance:** AC-4

**Evidence:** All tests pass via `python -m pytest`.

---

## Task 5: Create capability spec

**Description:** Write `openspec/specs/calculator.md` documenting the full API surface, requirements, and usage examples.

**Acceptance:** AC-5

**Evidence:** Spec file exists with API table, requirements list, and usage examples.
