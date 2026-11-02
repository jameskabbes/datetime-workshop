# Datetime Workshop

This repo contains two notebooks:

- `its_about_time_datetime_workshop.ipynb`: Python datetime fundamentals and timezone concepts.
- `conus_datetime_parsing_workshop.ipynb`: Real-world datetime parsing and analytics with U.S. electricity demand data.

## Requirements

- Python 3.11+ (recommended: 3.13)
- VS Code with Python and Jupyter extensions

## Quick Start (uv - recommended)

`uv` gives reproducible, fast local and Codespaces setup.

1. Install uv:
   - https://docs.astral.sh/uv/getting-started/installation/
2. Create and sync environment:

```bash
uv venv
uv sync
```

3. Select `.venv` as the Python interpreter in VS Code.
4. Open either notebook and run cells top to bottom.

## Alternative Setup (pip)

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Then select `.venv` in VS Code and run the notebooks.

## Dependency Files

- `pyproject.toml`: canonical project metadata and dependencies (used by uv)
- `requirements.txt`: pip-compatible dependency list
- `.python-version`: recommended Python version for tools like pyenv/uv

## Data Files

- `conus_hourly_demand.csv` is expected in the repository root for the CONUS notebook.

## Reproducibility Notes

- Timestamps in the workshop data are parsed as UTC first, then converted to local timezones for calendar features.
- Keep timezone conversion explicit (`tz_convert`) to avoid ambiguous local-time handling.

## Troubleshooting

- If notebook imports fail, confirm the selected VS Code interpreter is `.venv`.
- If plotting does not render, re-run the setup cell and restart the kernel.
