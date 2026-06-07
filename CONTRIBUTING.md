# Contribution and Release Rules

This repository uses a two-branch workflow:

```text
develop -> development and testing
main    -> production release
```

## Branch Roles

### `develop`

Use `develop` for daily development, UI changes, content workflow changes, and preview testing.

Rules:

- New work starts from `develop`.
- Feature branches should branch from `develop`.
- Merge feature work back into `develop` first.
- Use `develop` to verify page rendering, issue data display, language switching, SEO tags, and widget integration before production.
- Do not treat `develop` as production.

### `main`

Use `main` only for production.

Rules:

- `main` should only receive changes that are already tested on `develop`.
- Production deployment happens from `main`.
- Avoid direct commits to `main` except for emergency hotfixes.
- Prefer merging `develop` into `main` through a pull request.

## Recommended Workflow

```text
git checkout develop
git pull origin develop

git checkout -b feature/your-change
# make changes
# verify locally

git checkout develop
git merge feature/your-change
git push origin develop

# after verification
open PR: develop -> main
merge PR
```

## Production Release Checklist

Before merging `develop` into `main`:

- Homepage loads correctly.
- English page loads correctly.
- Issue data renders correctly.
- Language switching works.
- SEO tags and sitemap are still valid.
- Widget script still loads from `https://api.swep.top/verify.js`.
- No local-only URLs are introduced into production pages.

## Deployment Rules

- Vercel production should deploy from `main`.
- Vercel preview deployments may use `develop`.
- Production domain is `https://ideas.swep.top`.
- GitHub Actions may update `docs/data.json` from issue sync. Treat those commits as data sync commits, not feature releases.

## Emergency Hotfix

For urgent production fixes:

```text
main -> hotfix branch -> main
main -> merge/cherry-pick back into develop
```

Every hotfix merged into `main` must also be applied back to `develop` so the branches do not drift.
