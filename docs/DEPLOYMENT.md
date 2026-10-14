# GitHub Pages Deployment

## Overview

TutorX is a static site. The root `index.html` is the entry point, so there is no package install or build step. A GitHub Actions workflow can publish the repository as a GitHub Pages site.

## First-time setup

1. Open the repository: https://github.com/renuah1142/tutorx
2. Ensure the changes containing `index.html`, the documentation and `.github/workflows/pages.yml` are merged into the `main` branch.
3. Open **Settings → Pages** in the repository.
4. Under **Build and deployment**, select **GitHub Actions** as the source if it is not already selected.
5. Open **Actions** and verify the Pages deployment workflow completes successfully.
6. Open the Pages URL shown in **Settings → Pages**. For a project site, the expected form is `https://renuah1142.github.io/tutorx/`, provided Pages is enabled and the deployment succeeds.

## Automatic deployment

The workflow runs on pushes to `main` and can be started manually from the Actions tab. It uploads the repository root as a Pages artifact and deploys it using the official GitHub Pages actions.

## Local preview

Because the app is static, you can open `index.html` directly in a modern browser. For a more representative local web preview, run a static server from the repository root, for example:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Troubleshooting

- **404 page:** confirm Pages is enabled, the workflow succeeded, and `index.html` is at the deployed root.
- **Workflow permission error:** check repository Actions permissions and the workflow's `pages: write` and `id-token: write` permissions.
- **No deployment environment:** choose GitHub Actions as the Pages source in repository settings and rerun the workflow.
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

GitHub Pages deployment settings may require a one-time repository owner action. A workflow file alone does not prove that the site is already published.