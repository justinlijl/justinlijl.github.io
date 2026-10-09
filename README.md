# Justin Li — personal site

A single-page static portfolio built from your CV. No build tools, no frameworks — open `index.html` in any browser and it works.

## What to drag to GitHub

When uploading to a new GitHub repo, drag these three files together into the upload area:

- `index.html` — the website itself
- `.nojekyll` — tells GitHub Pages not to run Jekyll processing on it
- `README.md` — this file (helps future-you remember what the repo is)

## Deploy via GitHub Pages (no command line)

1. On github.com, click the **+** in the top-right → **New repository**.
2. Name it anything (e.g. `justin-li.github.io` if you want it on your root user domain, or `personal-site` for a project-page URL).
3. Visibility: **Public**. Skip all the "initialize" checkboxes — leave the repo empty.
4. Once the repo is created, you'll land on its main page. Click **Add file → Upload files** (top-right, above the file list).
5. Finder: open the `cv-website/` folder on your Mac. Press **Cmd + Shift + .** to show hidden files (so you can see `.nojekyll`). Select all three files and drag them into the upload box on GitHub.
6. Click **Commit changes** (green button, bottom of the page).
7. Go to **Settings → Pages** in the repo's left sidebar. Under *Build and deployment*:
   - **Source:** Deploy from a branch
   - **Branch:** `main`, folder **`/ (root)`**
8. Save. Wait about a minute. GitHub will show a green banner with your live URL.

Your site will be live at one of:
- `https://<your-github-username>.github.io/<repo-name>` — if you used a regular repo name
- `https://<your-github-username>.github.io` — if the repo is named exactly `<your-github-username>.github.io`

## Editing your site later

Every text edit is a normal change to `index.html`. To publish a change:

1. Edit `index.html` locally and save.
2. Open the repo on github.com → click the `index.html` row → the pencil icon to edit, **or** upload a new version via **Add file → Upload files**.
3. Commit. GitHub Pages rebuilds automatically in ~30 seconds.

To swap in a real photo: find `<div class="photo" aria-hidden="true">LM</div>` near the top of `index.html` and replace it with `<img src="photo.jpg" alt="Justin Li" class="photo" />`. Then drop `photo.jpg` into the same folder on the repo (via drag-and-drop).

The accent colour (the warm brown stripe and the bullet markers) is the value `#BA7517` in two spots at the top of the `<style>` block. Change it once and it updates everywhere.

## Local preview

Double-click `index.html` to open it in your browser, or run a tiny local server from the folder:

```
python3 -m http.server 8000
```

then visit <http://localhost:8000>.

## Custom domain

Once GitHub Pages is live, attach your own domain (e.g. `justin-li.com`) by following GitHub's official custom-domain guide — it adds a `CNAME` file to the repo and you set a CNAME record with your DNS provider. GitHub will provision HTTPS automatically.
