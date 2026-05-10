# Recruiter portfolio (static site)

Professional single-page site for **full-time DevOps** conversations—separate from the freelance-focused site at [afterhours-builds](https://whitedevilml.github.io/afterhours-builds/).

## Before you publish

1. **LinkedIn:** In `index.html`, replace the placeholder LinkedIn `href` (currently `https://www.linkedin.com/`) with your profile URL.
2. **Email:** The page uses `lokeshmlaute@gmail.com` (from your public portfolio). Change the `mailto:` and footer if you use a different address for recruiting.

## Deploy on GitHub Pages

### Option A — New repository (recommended)

1. Create a new GitHub repository, for example `devops-portfolio` or `lokesh-devops`.
2. Copy the contents of this `portfolio-site` folder to the **root** of that repository (so `index.html` is at the repo root).
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
4. Choose branch `main` and folder `/ (root)`, then save.
5. Your site will be available at:

   `https://whitedevilml.github.io/<repository-name>/`

   Example: `https://whitedevilml.github.io/devops-portfolio/`

6. Optional: add a custom domain later under Pages settings.

### Option B — User site (only one allowed per account)

If you ever use `whitedevilml.github.io` without a path, that repo must be named **`whitedevilml.github.io`**. Your existing `afterhours-builds` project uses a **project** URL, so Option A keeps this recruiter site on its own path without breaking the old one.

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

> Portfolio (DevOps): `https://whitedevilml.github.io/<your-repo-name>/`
