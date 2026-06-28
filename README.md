# ARCK — Lo-fi Investor Wireframe

A single, self-contained HTML page. **No build step, no dependencies** — Vercel serves
`index.html` directly. This version is **flat**: `index.html` is at the root, so it shows
up at your project's main URL (no `/arck/lofi` path needed).

## Deploy — works at the root URL

**GitHub → Vercel:** push these files to a repo, then in Vercel **Add New → Project →
Import** it. Framework preset: **Other**. Deploy.

**Or the CLI:**
```bash
npm i -g vercel
vercel --prod
```

Either way the page lives at your project root:
**https://<your-project>.vercel.app/**

## If you want it at `client.studiosalt.co/arck/lofi`

That path comes from the **folder path inside the repo** — not from anything in the file.
To serve it at `/arck/lofi`, drop this `index.html` into the repo that already powers
`client.studiosalt.co` (your existing client project) at:

```
arck/lofi/index.html
```

…then commit and push. Vercel will serve it at `client.studiosalt.co/arck/lofi`.

> Don't attach the whole `client.studiosalt.co` domain to a separate one-page project —
> a domain can live on only one Vercel project, and the rest of the site would 404.
> For a quick shareable preview, just use the `*.vercel.app` URL this flat deploy gives you.

## Files

```
index.html    the wireframe (at root → serves at /)
README.md
.gitignore
```
