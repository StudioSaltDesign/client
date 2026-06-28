# ARCK — Lo-fi Investor Wireframe

A single, self-contained HTML wireframe (dark, investor-facing) for ARCK Energy.
**No build step, no dependencies, no npm install** — Vercel serves it as a static file.

**Target URL:** `client.studiosalt.co/arck/lofi`
The path is case-sensitive — all lowercase (`arck/lofi`). The folder path in this repo *is* the URL path.

## What's inside

```
arck/lofi/index.html   the page  (folder path = URL path)
vercel.json            clean URLs, no trailing slash
README.md              this file
.gitignore
```

## Deploy

### Option A — GitHub → Vercel  (recommended · auto-deploys on every push)

**If `client.studiosalt.co` is already a Vercel project** — most likely, since the URL is path-based (`/client/deliverable`):

1. Copy the `arck/` folder into the root of that project's repo.
   (If `arck/` already exists, just add the `lofi/` folder inside it.)
2. Don't overwrite the repo's existing `vercel.json` — delete the one in this package if the repo already has its own.
3. Commit and push:
   ```bash
   git add .
   git commit -m "Add ARCK lo-fi wireframe"
   git push
   ```
4. Vercel auto-builds and deploys → **client.studiosalt.co/arck/lofi**

**Standalone repo for just this deliverable:**

1. Create an empty repo on GitHub, then from this folder:
   ```bash
   git init
   git add .
   git commit -m "ARCK lo-fi wireframe"
   git branch -M main
   git remote add origin git@github.com:<you>/<repo>.git
   git push -u origin main
   ```
2. In Vercel: **Add New → Project → Import** this repo. Framework preset: **Other** (static). Deploy.
3. (Optional) **Settings → Domains** → add `client.studiosalt.co`.
   A domain can belong to only one Vercel project, so only do this if the subdomain isn't already used elsewhere — otherwise use Option A.
   With the nested folder the page lives at `…/arck/lofi`; to serve it at the domain root instead, move `index.html` up to the repo root.

### Option B — Vercel CLI  (no GitHub)

```bash
npm i -g vercel
vercel          # first run links/creates the project
vercel --prod   # deploy to production
```

## Update later

Replace `arck/lofi/index.html` and push (Option A) or re-run `vercel --prod` (Option B).
