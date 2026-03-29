# Contributing to TON SBT CLI

Thank you for contributing.

This project is open source and maintained for practical operator use on the TON blockchain. The goal is to keep the repository clear, reproducible, and safe for public collaboration.

## Use vs Contribute

If you only want to use the project locally:

```powershell
git clone https://github.com/followdragons/ton-sbt-cli.git
cd ton-sbt-cli
.\scripts\setup.ps1
```

If you want to contribute changes:

1. Fork the repository on GitHub.
2. Clone your fork.
3. Add the main repository as `upstream`.

```powershell
git clone https://github.com/<your-user>/ton-sbt-cli.git
cd ton-sbt-cli
git remote add upstream https://github.com/followdragons/ton-sbt-cli.git
.\scripts\setup.ps1
```

## Development Workflow

Create a branch for your work:

```powershell
git checkout -b feature/my-change
```

Run the test suite before committing:

```powershell
.\scripts\test.ps1
```

If you are working with live testnet settings and want to run the optional manual integration checks:

```powershell
$env:TON_SBT_RUN_INTEGRATION=1
.\scripts\test.ps1 tests\test_integration_manual.py -q
```

Commit your work:

```powershell
git add .
git commit -m "Describe the change"
```

Push the branch to your fork:

```powershell
git push origin feature/my-change
```

Then open a Pull Request from your fork into:

- base repository: `followdragons/ton-sbt-cli`
- base branch: `main`

## Expectations

- Keep all user-facing documentation and comments in English.
- Do not commit `.env`, `wallets.txt`, generated wallets, or secrets.
- Keep changes focused and reviewable.
- Preserve the documented CLI behavior unless the change intentionally updates the public interface.
- Update tests and documentation when behavior changes.

## Environment Notes

- Use `.env.example` as the safe configuration template.
- Use `wallets.txt.example` as the safe recipient file template.
- Keep real mnemonic phrases and real recipient lists local only.

## Syncing Your Fork

To sync your fork with the main repository:

```powershell
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

## Reporting Issues

If you are not submitting code, use GitHub Issues for:

- bug reports
- documentation problems
- feature requests
- integration questions
