# Entwicklung — Anleitung

**Voraussetzungen:** Node.js (empfohlen Version 16+) und `npm`.

Lokalen Dev‑Server starten (Vite, empfohlen):

```bash
npm install
npm run dev
# Öffnen: http://localhost:5173
```

Build und Vorschau:

```bash
npm run build
npm run preview --port=5173
# Vorschau: http://localhost:5173
```

Alternativ (kein Node, sehr einfach):

```bash
python3 -m http.server 8000
# Öffnen: http://localhost:8000
```

Deployment — GitHub Pages (automatisch):

- Ein Workflow (`.github/workflows/deploy-pages.yml`) ist bereits enthalten; **Push** zu `main` löst ein Deployment aus.
- Falls Deploy fehlschlägt wegen fehlender Schreibrechte, können Sie:
  - Repo → Settings → Actions → General → **Allow GitHub Actions to write** aktivieren, ODER
  - ein Personal Access Token (PAT) erstellen und als Repository Secret `GH_PAGES_TOKEN` anlegen (empfohlen, wenn Sie feingranulare Kontrolle brauchen).

PAT / Secret erstellen (kurzanleitung):
1. Erstellen Sie ein Personal Access Token unter https://github.com/settings/tokens (Scopes: `repo` oder mindestens `repo:status, repo_deployment, public_repo` für öffentliche Repos).
2. Im Repository: Settings → Secrets and variables → Actions → New repository secret → Name: `GH_PAGES_TOKEN`, Value: Ihr PAT → Add secret.
3. Danach triggern Sie einen neuen Commit (oder ich triggere einen Testlauf) — ich prüfe dann die Action‑Runs.

Tipps:
- Sicherheitsprüfung: `npm audit` / `npm audit fix` (oder `--force` wenn Sie breaking changes akzeptieren).
- Vite bietet HMR (Hot Module Replacement) für schnelle Entwicklung.

Viel Erfolg beim Entwickeln! ✨