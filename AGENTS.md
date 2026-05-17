# Repository Guidelines

## Project Structure & Module Organization

This repository documents and builds a PaySim mobile money fraud analysis workflow. The current tracked structure is small:

- `README.md` describes the project, dataset source, roadmap, and setup flow.
- `data/schema.md` contains the profiled PaySim schema and column notes.
- `data/*.csv` and `data/*.zip` are intentionally ignored because the raw dataset is large.
- `notebooks/` is the intended location for future EDA, feature engineering, and modeling notebooks.

Keep generated data artifacts under `data/` and do not commit raw Kaggle downloads.

## Build, Test, and Development Commands

There is no build system or automated test suite configured yet. Useful local commands:

```bash
pip install -r requirements.txt
```

Installs the Python analysis dependencies once `requirements.txt` is present.

```bash
kaggle datasets download -d ealaxi/paysim1 --unzip -p data/
```

Downloads the PaySim CSV into `data/`.

```bash
jupyter lab
```

Starts the notebook environment for exploratory work once notebooks are added.

## Coding Style & Naming Conventions

Use Python for analysis code and notebooks. Prefer clear, descriptive names for feature columns, for example `origin_balance_delta` or `is_transfer_cashout_pair`. Use `snake_case` for Python variables, functions, notebook filenames, and derived dataset columns. Keep Markdown concise and factual; preserve dataset column names exactly as provided, such as `oldbalanceOrg` and `isFlaggedFraud`.

## Testing Guidelines

No testing framework is configured yet. When adding reusable Python modules, add `pytest` tests under `tests/` with files named `test_*.py`. For notebooks, include lightweight validation cells that check row counts, fraud prevalence, missing values, and expected transaction types before modeling.

## Commit & Pull Request Guidelines

Recent commits use short imperative summaries such as `Create README.md` and `Add schema profiler, README, gitignore CSV data`. Continue that style: start with a verb, keep the subject focused, and mention the main artifact changed.

Pull requests should include a short purpose statement, changed files or notebooks, how results were validated, and any dataset assumptions. Include screenshots or exported figures when changing visual analysis. Do not include raw CSVs, ZIPs, `.env`, virtual environments, or notebook checkpoints.

## Security & Configuration Tips

Keep Kaggle credentials outside the repository. Store secrets in local environment files or the standard Kaggle config location, and rely on `.gitignore` to keep `.env` and large data files untracked.
