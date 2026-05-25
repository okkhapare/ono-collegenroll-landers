# CollegEnroll Landers

Static CollegEnroll landing pages prepared for GitHub and Cloudflare Pages.

## Pages

- `/degree-match/` - Degree match quiz
- `/CollegEnroll-index.html` - Saved CollegEnroll homepage reference

The root `index.html` redirects visitors to `/degree-match/` so the Pages apex does not return a 404.

## Local Preview

```powershell
node dev-static-server.js
```

Then open `http://localhost:4174/degree-match/`.

## GitHub Sync

After creating a GitHub repository, add the remote and push:

```powershell
git remote add origin https://github.com/<your-github-user>/<repo-name>.git
git branch -M main
git push -u origin main
```

## Cloudflare Pages

Use Cloudflare Pages' Static HTML setup:

- Production branch: `main`
- Build command: `exit 0`
- Build output directory: `/` or `.`
- Root directory: `/`

Cloudflare can then deploy automatically from GitHub on every push.
