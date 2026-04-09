# KI-OS Status Page

Live: **[status.ki-os.org](https://status.ki-os.org)**

Powered by [Upptime](https://upptime.js.org) — GitHub Actions, keine Server, kostenlos.

## Deployment (einmalig)

### 1. Neues GitHub Repo anlegen

`KI-OS-org/status` — **public**, mit diesem Inhalt befüllen.

### 2. GitHub Personal Access Token

In GitHub: Settings → Developer Settings → Personal Access Tokens → Fine-grained token  
Berechtigungen: `repo` (vollständig), `workflow`

Token als Secret hinterlegen:  
`KI-OS-org/status` → Settings → Secrets → Actions → `GH_PAT`

### 3. GitHub Pages aktivieren

Repo → Settings → Pages → Source: `gh-pages` Branch

### 4. DNS-Eintrag

Bei deinem DNS-Provider (z. B. Cloudflare):

```
CNAME   status   KI-OS-org.github.io
```

### 5. Ersten Lauf manuell triggern

Actions → "Uptime CI" → "Run workflow"

Nach ~2 Minuten ist `status.ki-os.org` live.

## Was wird überwacht

| Service | URL | Check |
|---|---|---|
| ki-os.org | https://ki-os.org | HTTP 200 |
| Community Edition | https://github.com/KI-OS-org/ki-os | HTTP 200 |
| updates.ki-os.org | https://updates.ki-os.org/community/ping | POST → 200 |
