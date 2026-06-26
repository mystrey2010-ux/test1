# myapp

Example CLI calculator application demonstrating the OpenSpec (spec-driven development) workflow.

## Setup

```bash
conda create -n test1 python=3.12
conda activate test1
pip install -e .
```

## Usage

```bash
myapp add 3 4        # → 7.0
myapp subtract 10 5  # → 5.0
myapp multiply 3 6   # → 18.0
myapp divide 10 3    # → 3.333...
```

## OpenSpec Workflow

This project uses OpenSpec for spec-driven development:

- **proposal** → `openspec/changes/add-calculator/proposal.md`
- **design** → `openspec/changes/add-calculator/design.md`
- **tasks** → `openspec/changes/add-calculator/tasks.md`
- **spec** → `openspec/specs/calculator.md`

See [OpenSpec documentation](https://github.com/yong-wei/openspec-buddy) for the workflow details.
