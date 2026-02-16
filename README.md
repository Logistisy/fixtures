# Fixtures

Test fixtures for the Logisticy project. This repository stores PDF reports and their expected JSON output, serving as the source of truth for our parsing and extraction tests.

## Structure

```
fixtures/
  femax/
    <fixture-name>/
      input.pdf          # Original Femax PDF report
      expected-output.json # Expected parsed JSON output
```

Each fixture is a directory containing a PDF input and the corresponding expected JSON output. This makes it easy to add new test cases: just drop in a new directory with the PDF and its expected output.

## Why a dedicated repo?

Although storing binary files in git is generally discouraged, these fixtures are the core of our testing strategy. Having them versioned ensures:

- **Reproducibility** -- any commit in any consuming repo can reference a specific set of fixtures.
- **Safety** -- accidental deletions or modifications are caught by version control.
- **Traceability** -- changes to expected outputs are reviewed in PRs just like code changes.
