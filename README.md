# padstack

Minimal notes REST API built with Flask

Built for my own use; public in case it helps someone.

## What it does

- pytest coverage for the happy paths
- Request validation and consistent error shape
- CRUD endpoints for notes
- SQLite storage via sqlite3 stdlib

## Examples

```bash
curl -X POST localhost:5000/notes \
  -H 'content-type: application/json' \
  -d '{"title": "first", "body": "hello"}'
```

## Install

```bash
pip install -r requirements.txt
flask --app app run --debug
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   └── roadmap.md
├── tests/
│   └── test_api.py
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── app.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```
