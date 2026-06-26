# Proposal: Add Calculator Module

## Summary

Add a calculator module (`myapp.calculator`) with basic arithmetic operations
(add, subtract, multiply, divide) and a CLI entry point.

## Motivation

The project needs a foundational utility that demonstrates the OpenSpec workflow.
A calculator is simple enough to understand quickly while exercising all phases:
proposal → design → tasks → implementation → spec creation.

## Scope

### In scope

- Core math functions in `src/myapp/calculator.py`
- CLI interface via `argparse` in `src/myapp/cli.py`
- Unit tests for calculator functions
- Capability spec at `openspec/specs/calculator.md`

### Non-goals

- GUI or web interface
- History / memory of previous calculations
- Support for more than two operands
- Complex expressions (e.g., `3 + 4 * 2`)
- Configuration files or environment variables
- Documentation beyond docstrings

## Spec Changes

| Capability    | Change                              |
|---------------|-------------------------------------|
| calculator    | New capability spec                 |
