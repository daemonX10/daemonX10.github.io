# Deployment Guide (GitHub Pages)

## 1. Prerequisites
- Node.js 20+
- GitHub Pages enabled for the repository
- Repository pushed to GitHub

## 2. Local validation
Run these commands from the project root:

```powershell
npm install
npm run lint
npm run build
npm run start -- --port 3001
```

Open http://localhost:3001 and verify:
- hero + proof snapshot render
- project filters work
- contact/social links open correctly
- resume view/download links work

## 3. Deploy to GitHub Pages
1. Push the repository to the default branch.
2. Enable GitHub Pages using GitHub Actions in the repository settings.
3. The workflow builds the static export from `npm run build` and publishes the `out` folder.
4. Wait for the Pages deployment to complete, then open the custom domain.

## 4. Domain setup (optional)
1. Keep the `CNAME` file set to `damodar.me`.
2. Point the domain DNS to GitHub Pages as required by your registrar.
3. Wait for SSL certificate issuance after the Pages deployment finishes.

## 5. Post-deploy checks
- Open production URL and check all sections.
- Verify Open Graph preview by sharing the URL.
- Verify mobile navigation and section highlighting.
- Verify the exported site root opens the portfolio homepage.
- Verify the resume download link opens the Google Drive download URL.

## 6. Recommended ongoing updates
- Keep `src/data/portfolio.ts` as source of truth for content.
- Replace placeholder project art in `public/projects` with real screenshots over time.
- Update experience and proof metrics whenever new achievements are available.
