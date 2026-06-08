# Deploying the Learning Wiki to GitHub Pages (free)

Your wiki source lives in `docs/` (the student-facing pages) and `mkdocs.yml` (config). A GitHub Action builds and publishes it automatically every time you push. Follow these once.

## One-time setup

### 1. Put the project on GitHub
From this project folder (`pk-study-blocker`), in a terminal:

```powershell
git init
git add .
git commit -m "Add learning wiki"
git branch -M main
```

Then create a repo and push. Easiest with the GitHub CLI (`gh`):

```powershell
gh repo create learning-wiki --public --source=. --push
```

**No `gh`?** Create an empty repo at <https://github.com/new> (Public, don't add a README), then:

```powershell
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

### 2. Turn on GitHub Pages
On GitHub: **your repo → Settings → Pages → Build and deployment → Source: → "GitHub Actions"**. That's it — no branch to pick.

### 3. Wait for the build
Go to the **Actions** tab. The "Deploy learning wiki" workflow runs (~1 min). When it's green, your site is live at:

```
https://YOUR-USERNAME.github.io/YOUR-REPO/
```

That's the link you give students. Done. 🎉

## Editing the wiki later

1. Edit or add markdown files in `docs/`.
2. To add a new page to the sidebar, add it under `nav:` in `mkdocs.yml`.
3. Commit and push:
   ```powershell
   git add .
   git commit -m "Update wiki"
   git push
   ```
4. The Action redeploys automatically in ~1 minute.

## Preview locally before pushing (optional)

Requires Python:

```powershell
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000> — it live-reloads as you edit. `Ctrl+C` to stop.

## Notes

- The site is built **only** from `docs/` + `mkdocs.yml`. Your `knowledge-base/` research files and `poker-routine.html` stay in the repo but aren't part of the published site (they're harmless extras).
- Content is **public** (anyone with the link can read it; search engines may index it).
- Free forever on the GitHub Pages free tier. A custom domain (e.g. `wiki.yourbrand.com`) is the only optional cost (~$12/yr) — set it under Settings → Pages → Custom domain.
- Optional: set `site_url:` in `mkdocs.yml` to your final URL (improves the sitemap; not required).
