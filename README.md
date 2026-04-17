# Damodar Yadav Portfolio

Personal portfolio site built with Next.js and exported as a static site for GitHub Pages.

## Live

- https://damodar.me

## Local development

```bash
npm install
npm run dev
```

## Production build

```bash
npm run build
```

## Deployment

The repository uses a GitHub Actions workflow to build and deploy static output to GitHub Pages.

- Workflow file: `.github/workflows/deploy.yml`
- Domain file: `CNAME`
- Source of content: `src/data/portfolio.ts`
