# Voltmx Design Specs — Starter
A minimal Jekyll site + GitHub workflow for managing design specs.

## Quick Start
1. Copy this folder into a new GitHub repo.
2. Enable **Pages** → Build from `main` (root).
3. Use the homepage buttons to open Issue Forms.

## Structure
- `_specs/<family>/<version>/` — one folder per version (e.g., `flutter-sdk/v2`)
- `index.html` — homepage with tabs, search, and “show all versions” toggle
- `_layouts/spec.html` — spec page with left sidebar + status banner
- `.github/workflows/validate-specs.yml` — CI guardrails
- Issue forms in `.github/ISSUE_TEMPLATE/`

## Rules
- Only one **active** version per family (CI-enforced).
- Deprecated specs require `deprecated_at` & `deprecation_reason`.
- Updates should bump `updated_at` and add a `changelog` entry.
