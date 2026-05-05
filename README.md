# kelvinfernandes.me — Personal Portfolio
Personal portfolio website built with **Astro** , automatically deployed via **GitHub Actions** to `kelvinfernandes.me`.
## Tech Stack
| Layer | Tool |
|---|---|
| Framework | [Astro](https://astro.build) |
| Styling | CSS Custom Properties (dark theme) |
| Deployment | GitHub Pages + GitHub Actions |
| Containerization | Docker / Docker Compose |
## Quick Start
```bash
# Install dependencies
npm install
# Development server (localhost:4321)
npm run dev
# Production build
npm run build
# Preview production build
npm run preview
Docker
Build and run the production site locally:
# Production build served via nginx (localhost:8080)
docker compose up prod
# Development with hot-reload (localhost:4321)
docker compose up dev
CI/CD
Every push to main triggers a GitHub Actions workflow that:
1. Installs dependencies
2. Runs astro build
3. Uploads the dist/ folder as a Pages artifact
4. Deploys to GitHub Pages
The workflow file is at .github/workflows/deploy.yml.
Adding Projects
Open src/components/Projects.astro and edit the projects array:
{
  title: "Your Project",
  status: "Done", // or "Coming Soon"
  description: "Brief description",
  icon: "🚀",
  tags: ["Tech1", "Tech2"],
}
License
MIT
