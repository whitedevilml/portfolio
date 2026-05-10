# Recruiter portfolio (static site)

Professional single-page site for **full-time DevOps** conversations—separate from the freelance-focused site at [afterhours-builds](https://whitedevilml.github.io/afterhours-builds/).

**Repository:** [github.com/whitedevilml/portfolio](https://github.com/whitedevilml/portfolio)

**Live site (after you enable Pages, Part B):** [https://whitedevilml.github.io/portfolio/](https://whitedevilml.github.io/portfolio/)

---

## Part A — Already done if you followed the first push

From the folder that contains `index.html` (this repo root):

```powershell
git init
git branch -M main
git remote add origin https://github.com/whitedevilml/portfolio.git
git add -A
git commit -m "Initial commit: recruiter DevOps portfolio for GitHub Pages"
git push -u origin main
```

For future edits:

```powershell
git add -A
git commit -m "Describe your change"
git push
```

---

## Part B — Enable GitHub Pages (do this in the browser)

1. Open [github.com/whitedevilml/portfolio/settings/pages](https://github.com/whitedevilml/portfolio/settings/pages).
2. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.
3. Under **Branch**, select **`main`** and folder **`/ (root)`**, then click **Save**.
4. Wait one to three minutes. Refresh the page until **Visit site** appears, or open [https://whitedevilml.github.io/portfolio/](https://whitedevilml.github.io/portfolio/) directly.
5. If you see **404** at first, wait another minute and hard-refresh (`Ctrl+F5`). First deploys can be slow.

Optional: on the repo main page, click **Settings** → **General** → **Features** → enable **Discussions** only if you want them (not required).

---

## Before you publish

1. **LinkedIn:** In `index.html`, replace `YOUR-HANDLE` in the LinkedIn URL with your public profile slug.
2. **Email:** The page uses `lokeshmlaute@gmail.com` (from your public portfolio). Change the `mailto:` and footer if you use a different address for recruiting.

## Deploy notes

This repository **is** the `portfolio` project site. Hosting steps are in **Part B** above. The site URL is `https://whitedevilml.github.io/portfolio/`. A different repo name would change only the last path segment. A **user** site (`https://whitedevilml.github.io/` with no extra path) would require a separate repository named `whitedevilml.github.io`.

## Local preview

Open `index.html` in a browser, or from this directory:

```bash
npx --yes serve .
```

Then visit the URL printed in the terminal (often `http://localhost:3000`).

## Files

| File        | Purpose                          |
|------------|-----------------------------------|
| `index.html` | Content and structure            |
| `styles.css` | Layout and theme               |
| `.nojekyll` | Tells GitHub Pages not to use Jekyll (safe for static assets) |

## Sending to recruiters

Use the live **GitHub Pages URL** in your email signature and LinkedIn featured section, for example:

> Portfolio (DevOps): `https://whitedevilml.github.io/portfolio/`
