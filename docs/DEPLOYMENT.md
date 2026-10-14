# GitHub Pages Deployment

## Overview

TutorX is a static site. The root `index.html` is the entry point, so there is no package install or build step. GitHub Actions uploads the repository as a Pages artifact and publishes it.

## First-time setup

**Important:** GitHub Actions cannot enable Pages for this repository with the current integration permissions. The repository owner must enable Pages once in Settings before the workflow can deploy. The earlier failed runs stopped at `Configure GitHub Pages` because Pages had not yet been created; the workflow no longer attempts to create it automatically.

1. Open [TutorX Pages settings](https://github.com/renuah1142/tutorx/settings/pages).
2. Under **Build and deployment**, set **Source** to **GitHub Actions**. This selection enables the Pages site and gives the workflow a deployment target.
3. Open the [Deploy TutorX to GitHub Pages workflow](https://github.com/renuah1142/tutorx/actions/workflows/pages.yml).
4. Choose **Run workflow**, select the `main` branch, and run it. A push to `main` will also trigger deployment automatically.
5. Wait for the run to finish successfully, then open [https://renuah1142.github.io/tutorx/](https://renuah1142.github.io/tutorx/).

If the Settings page does not show a **GitHub Actions** source option or does not let you save it, check that GitHub Pages is available for this repository and that you are signed in as the repository owner.

## Automatic deployment

After the one-time setup, the workflow runs on pushes to `main` and can be started manually from the Actions tab. It uploads the repository root as a Pages artifact and deploys it using the official GitHub Pages actions. The workflow intentionally does not try to enable Pages through the Actions token because GitHub rejects that administrative request.

## Local preview

Because the app is static, you can open `index.html` directly in a modern browser. For a more representative local web preview, run a static server from the repository root, for example:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Troubleshooting

- **Configure GitHub Pages says `Not Found`:** Pages has not been enabled for the repository yet. Follow the first-time setup above and set the source to **GitHub Actions**.
- **`Resource not accessible by integration`:** the workflow token cannot create the Pages site. Do not add `enablement: true`; enable Pages once in repository Settings instead.
- **Deploy job says Pages is not enabled:** verify Settings → Pages → Build and deployment → Source is **GitHub Actions**, then rerun the workflow.
- **404 page after a successful deployment:** confirm the workflow succeeded and `index.html` is at the deployed root.
- **Workflow permission error after Pages is enabled:** verify Actions are enabled and the workflow retains `pages: write` and `id-token: write`.
- **Old content appears:** inspect the latest workflow run and hard-refresh the browser after a successful deployment.
- **Relative paths break:** prefer relative paths for repository assets; do not assume the site is hosted at the domain root.
- **Workflow does not run:** confirm the workflow file is merged into `main` and Actions are enabled for the repository.

## Safe release process

1. Make changes on a feature branch.
2. Preview and test the app locally.
3. Review the diff and documentation.
4. Merge to `main` when ready.
5. Confirm the Pages workflow succeeded.
6. Smoke-test dashboard, lesson, quiz, flashcards, subnetting, progress export and mobile layout.

A workflow file alone does not prove that the site is already published. Confirm a successful Actions run and open the live Pages URL.
