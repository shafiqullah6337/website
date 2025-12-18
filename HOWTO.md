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
- Prüfen: Repository → Settings → Pages oder Actions → Deploy.

Tipps:
- Sicherheitsprüfung: `npm audit` / `npm audit fix` (oder `--force` wenn Sie breaking changes akzeptieren).
- Vite bietet HMR (Hot Module Replacement) für schnelle Entwicklung.

Viel Erfolg beim Entwickeln! ✨