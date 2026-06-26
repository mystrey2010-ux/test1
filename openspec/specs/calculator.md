# Capability: Calculator

## Purpose

Provide basic arithmetic operations (add, subtract, multiply, divide) via a
CLI interface and a reusable Python library.

## Requirements

- Support floating-point numbers for all operations.
- Division by zero must raise a clear error message.
- Invalid input must be handled gracefully with a non-zero exit code.
- CLI must accept arguments in the form: `myapp <op> <a> <b>` where `<op>` is
  one of `add`, `subtract`, `multiply`, `divide`.

## API Surface

### Functions (module: `myapp.calculator`)

| Function   | Signature              | Description                  |
|------------|------------------------|------------------------------|
| `add`      | `(a: float, b: float) -> float` | Return the sum of a and b  |
| `subtract` | `(a: float, b: float) -> float` | Return the difference       |
| `multiply` | `(a: float, b: float) -> float` | Return the product          |
| `divide`   | `(a: float, b: float) -> float` | Return quotient, raises if b=0 |

### CLI (module: `myapp.cli`)

| Command             | Description                     |
|---------------------|---------------------------------|
| `myapp add <a> <b>`  | Print a + b                    |
| `myapp subtract <a> <b>` | Print a - b                 |
| `myapp multiply <a> <b>` | Print a * b                 |
| `myapp divide <a> <b>`   | Print a / b (error on div by 0) |
