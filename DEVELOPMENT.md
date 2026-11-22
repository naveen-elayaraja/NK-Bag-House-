# Development Setup

## Prerequisites

- Node.js (use a supported LTS release for the installed Next.js version)
- npm
- Git

## Frontend

The Next.js application is maintained in the `frontend/` directory.

To run it locally:

```bash
cd frontend
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

Before opening a pull request, run the checks available in the frontend package:

```bash
npm run lint
npm run build
```

If a script is not present in the current package configuration, do not assume it has run; inspect `frontend/package.json` and use the configured equivalent.

## Project Direction

Read these documents before making customer-facing changes:

- [Architecture](docs/ARCHITECTURE.md)
- [UX direction](docs/UX_DIRECTION.md)
- [Design system](docs/DESIGN_SYSTEM.md)
- [Requirements checklist](docs/REQUIREMENTS_CHECKLIST.md)
- [Content and media guidelines](docs/CONTENT_AND_MEDIA_GUIDELINES.md)

The customer-facing interface should feel polished and premium without becoming cluttered. Use approved NK Bag House assets and verified product information. Do not copy another brand's protected visual identity.

## Environment and secrets

- Keep local secrets in environment files that are excluded by `.gitignore`.
- Never commit production credentials, API keys, tokens, private keys, or customer enquiry data.
- Document required variable names in an example file without including real secret values.
- Validate customer-submitted data on the server when backend services are introduced.

## Git workflow

The default branch is `main`. Keep it stable and use a feature branch for development.

```bash
git switch main
git pull --ff-only origin main
git switch -c feat/short-description
# make and test focused changes
git status
git add <reviewed-files>
git commit -m "feat: describe the change"
git push -u origin feat/short-description
```

Open a pull request for review before merging. Use descriptive commit messages and keep each commit focused.

**Do not force-push to `main` or rewrite shared history.** If local and remote history diverge, stop and inspect the log/status before choosing a safe merge or rebase strategy. Do not discard uncommitted work to make a pull succeed.

## Current Scope

The frontend foundation and project documentation are in place. The actual UI build should begin after the customer reference design, product catalogue, approved content, and enquiry requirements have been reviewed.

Backend services, database integration, storage, and deployment configuration will be documented when those decisions are finalized.
