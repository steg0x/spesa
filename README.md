# Spesa App

App web statica per la gestione della lista della spesa a partire da un file CSV.

## Avvio in locale

```bash
python3 -m http.server 4173
```

Apri poi `http://localhost:4173`.

## Pubblicazione online con GitHub Pages

Questa repo include una GitHub Action che pubblica automaticamente il sito statico su GitHub Pages.

### 1) Pusha il repository su GitHub

```bash
git remote add origin https://github.com/<tuo-username>/<nome-repo>.git
git push -u origin <nome-branch>
```

### 2) Abilita GitHub Pages

1. Vai su **Settings → Pages**.
2. In **Build and deployment**, seleziona **Source: GitHub Actions**.

### 3) Deploy automatico

A ogni push su `main`, il workflow `.github/workflows/deploy-pages.yml` farà deploy del sito.

URL finale (dopo il primo deploy):

`https://<tuo-username>.github.io/<nome-repo>/`

## Note

- L'app è completamente client-side: non serve backend.
- Se vuoi usare un branch diverso da `main`, aggiorna il workflow.
