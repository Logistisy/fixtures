# Fixtures

Test fixtures for the Logisticy project. This repository stores PDF reports and their expected JSON output, serving as the source of truth for our parsing and extraction tests.

## Structure

```
fixtures/
    <bescheidnummer.pdf> # Original VEMAGS Permit
    <bescheidnummer.json> # Expected parsed JSON output
```

## Why a dedicated repo?

Although storing binary files in git is generally discouraged, these fixtures are the core of our testing strategy. Having them versioned ensures:

- **Reproducibility** -- any commit in any consuming repo can reference a specific set of fixtures.
- **Safety** -- accidental deletions or modifications are caught by version control.
- **Traceability** -- changes to expected outputs are reviewed in PRs just like code changes.
