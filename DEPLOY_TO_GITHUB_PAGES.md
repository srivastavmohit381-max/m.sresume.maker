# Deploying this site to GitHub Pages

This repository contains a static site (single-page `index.html`). The included GitHub Actions workflow (`.github/workflows/gh-pages.yml`) will publish the repository root to a `gh-pages` branch whenever you push to `main`.

Steps to publish from your machine:

1. Ensure your local repo is connected to `https://github.com/srivastavmohit381-max/m.sresume.maker.git` and you have a `main` branch.

```bash
git remote add origin https://github.com/srivastavmohit381-max/m.sresume.maker.git
git branch -M main
git add .
git commit -m "Add site and GitHub Pages workflow"
git push -u origin main
```

2. After pushing, open the Actions tab on GitHub for this repository and confirm the `Deploy to GitHub Pages` workflow runs successfully. It will create/update the `gh-pages` branch.

3. Enable GitHub Pages (if not already enabled):

- Go to the repository Settings → Pages. GitHub will usually detect the site served from the `gh-pages` branch automatically.

Notes:
- The workflow publishes the repository root. If you want Pages to serve from `docs/` on `main` instead, I can update the workflow to copy files into `docs/` and publish from `main`.
- If your repository uses a different branch name than `main`, tell me and I’ll adjust the workflow.
