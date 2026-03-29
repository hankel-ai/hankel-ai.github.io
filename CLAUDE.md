# hankel.ai - Portfolio Site

## Tech Stack
- **Static site generator:** Hugo (Extended)
- **Theme:** hugo-profile (git submodule at `themes/hugo-profile`)
- **Hosting:** GitHub Pages via GitHub Actions

## Build & Run

```bash
# Local dev server
hugo server --buildDrafts

# Production build
hugo --gc --minify
```

## Project Structure
```
├── hugo.yaml              # Main site config (ALL content is here for hugo-profile theme)
├── static/
│   └── images/            # Hero image, project screenshots, profile photo
├── .github/workflows/
│   └── hugo.yml           # GitHub Actions deployment workflow
├── themes/hugo-profile/   # Theme (git submodule -- do not edit directly)
└── content/               # Additional pages (if needed beyond hugo.yaml config)
```

## Key Files
- `hugo.yaml` -- All site content (hero, about, projects, skills, contact) lives in this single file under `params:`
- `.github/workflows/hugo.yml` -- Deploys to GitHub Pages on push to main

## Conventions
- Dark mode is the default theme
- Project images go in `static/images/projects/`
- Profile photo goes at `static/images/me.png`
