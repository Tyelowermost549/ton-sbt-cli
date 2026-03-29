# AGENTS.md

Operational rules for coding agents working in this repository.

## Project Summary

TON SBT CLI is a Python CLI application for deploying TON SBT collections and batch-minting SBTs.

The repository supports two main workflows:

- testnet validation
- mainnet operator use

## Read First

Read these files before changing code or behavior:

1. `README.md`
2. `.env.example`
3. `scripts/setup.ps1`
4. `scripts/test.ps1`
5. `CONTRIBUTING.md`

## Repository Layout

Key paths:

- `README.md`: operator-facing documentation
- `CONTRIBUTING.md`: contributor workflow
- `.env.example`: safe configuration template
- `wallets.txt.example`: safe recipient file template
- `scripts/setup.ps1`: environment setup
- `scripts/run.ps1`: main CLI wrapper
- `scripts/test.ps1`: test runner
- `src/ton_sbt_tool/`: application code
- `tests/`: unit tests and optional integration smoke tests

## Local Setup

Preferred setup on Windows PowerShell:

```powershell
.\scripts\setup.ps1
```

This creates `.venv` and installs the project in editable mode with dev dependencies.

## Run and Test

Use the PowerShell wrappers as the default interface for setup, run, and test.
Do not replace them with ad hoc commands unless the task explicitly requires it.

Main CLI:

```powershell
.\scripts\run.ps1 --help
```

Run tests:

```powershell
.\scripts\test.ps1
```

Optional manual integration checks:

```powershell
$env:TON_SBT_RUN_INTEGRATION=1
.\scripts\test.ps1 tests\test_integration_manual.py -q
```

## Safety Rules

- Never commit `.env`, `wallets.txt`, `generated_wallets/`, or secrets.
- Treat `generated_wallets/` as local-only sensitive output.
- Do not add real mnemonic phrases, recipient lists, or API keys to tracked files.
- Prefer testnet for validation.
- Do not run deploy, mint, or other chain-writing flows unless the task explicitly requires an on-chain action.
- Do not assume testnet and mainnet balances are interchangeable.

## Configuration Rules

The runtime config is driven by `.env`.

Important fields:

- `MNEMONIC`
- `WALLET_VERSION`
- `COLLECTION_ADDRESS`
- `IS_TESTNET`
- `COLLECTION_METADATA_URL`
- `ITEMS_BASE_URL`

Metadata behavior:

- if `ITEMS_BASE_URL` is a prefix ending like `.../metadata/`, item metadata resolves by suffix
- if `ITEMS_BASE_URL` is a concrete file like `.../metadata/176.json`, every item points to that exact file
- `ITEM_METADATA_SUFFIX` is only used in prefix mode

Do not change config semantics without updating `README.md`, `.env.example`, and related tests.

## Editing Expectations

- Keep all user-facing docs and comments in English.
- Preserve the documented CLI behavior unless intentionally changing the public interface.
- Update tests and docs when behavior changes.
- Keep changes focused and reviewable.
- Use the existing PowerShell wrappers and current project structure unless the task explicitly requires changing them.

## Change Discipline

- Prefer minimal diffs.
- Do not rename commands, flags, env vars, or output fields unless required by the task.
- Avoid broad refactors unrelated to the requested change.
- Preserve backward-compatible behavior unless the task explicitly requires a breaking change.

## Git and Contribution Expectations

- The default branch is `main`.
- Contributors are expected to fork, branch, test, and open PRs.
- See `CONTRIBUTING.md` for the expected contribution flow.

## Change Checklist

When behavior, commands, or config changes:

1. update code
2. update tests
3. update `README.md`
4. update `.env.example` and `wallets.txt.example` if needed
5. update `CONTRIBUTING.md` if contributor workflow changed
6. update this file if agent instructions changed
