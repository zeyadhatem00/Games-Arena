# Games Arena

Games Arena is a single-page gaming and esports landing page built as a static HTML, CSS, and JavaScript project. It presents a dark, neon-accented visual experience for a fictional gaming brand, with sections for featured games, capabilities, sponsors, team members, contact details, and footer navigation.

## Highlights

- Responsive fixed navigation with smooth section links for Home, Our Games, What We Do, Our Team, and Contact Us.
- Hero section with gaming artwork, call-to-action controls, and a decorative active-player statistic.
- Bootstrap carousel showcasing nine named game cards across three slides, including genre labels and artwork.
- “What We Do” grid covering PC, mobile, AR/VR, PlayStation, and 3D-focused offerings.
- Animated sponsor-logo marquees and responsive team-member cards.
- Contact panel with displayed location, phone, and email information plus a styled message form.
- Local Font Awesome icons, Bootstrap assets, and bundled font files; the page does not depend on a package registry at runtime.

> **Scope:** This repository currently implements the front-end presentation only. There is no application backend, API client, database, authentication flow, or form-processing endpoint in the source tree.

## Technology

- Semantic HTML5 in [`index.html`](index.html)
- CSS3 in [`css/style.css`](css/style.css) and [`css/media.css`](css/media.css)
- Bootstrap **5.3.8** styles and JavaScript, vendored in [`css/bootstrap.min.css`](css/bootstrap.min.css) and [`Js/bootstrap.bundle.min.js`](Js/bootstrap.bundle.min.js)
- Font Awesome **7.2.0** styles and local WOFF2 fonts in [`css/all.min.css`](css/all.min.css) and [`webfonts/`](webfonts/)
- Local `ChakraPetch` and `DaysOne` font files in [`Fonts/`](Fonts/)
- No `package.json`, lockfile, build configuration, environment file, or project-specific dependency install is present.

## Run locally

Because this is a static site, any static HTTP server is sufficient. A local server is recommended so that asset paths behave consistently in the browser.

```bash
git clone --depth 1 https://github.com/zeyadhatem00/Games-Arena.git
cd Games-Arena
python3 -m http.server 8000
```

Open <http://localhost:8000> in a browser. To stop the server, press `Ctrl+C`.

You can also open [`index.html`](index.html) directly, but a local server is the more reliable option for browser testing. There is no project-specific build or test command to run.

## Site map

| Section | Purpose |
| --- | --- |
| Home | Brand introduction, hero artwork, and entry-point controls. |
| Our Games | Carousel of static game cards such as Alien Companions, Cyber Run 2099, and Aetheria Chronicles. |
| What We Do | Static capability cards and supporting artwork. |
| Sponsors | Horizontally animated logo strips using repository images. |
| Our Team | Static member portraits, names, and role labels. |
| Contact Us | Display-only contact cards and a front-end message form. |
| Footer | Brand copy, generic social-platform links, and placeholder navigation links. |

## Project structure

```text
.
├── index.html                 # Single-page markup and all displayed content
├── css/
│   ├── style.css              # Base theme and component styling
│   ├── media.css               # Responsive rules for smaller screens
│   ├── bootstrap.min.css       # Vendored Bootstrap CSS 5.3.8
│   └── all.min.css             # Vendored Font Awesome CSS 7.2.0
├── Js/
│   └── bootstrap.bundle.min.js # Vendored Bootstrap interactions
├── Images/                    # Hero, game, sponsor, avatar, and icon assets
├── Fonts/                     # Chakra Petch and Days One font files
├── webfonts/                  # Font Awesome WOFF2 files
└── .github/workflows/
    └── static.yml             # GitHub Pages workflow for the main branch
```

## Development notes

- Edit page content and structure in [`index.html`](index.html).
- Adjust the visual theme in [`css/style.css`](css/style.css); responsive overrides live in [`css/media.css`](css/media.css).
- Keep asset paths relative to the repository root when adding images, fonts, or stylesheets.
- The Bootstrap carousel and mobile navigation are powered by the bundled Bootstrap script. No custom JavaScript file is included.
- The repository includes a GitHub Actions workflow that uploads the repository root to GitHub Pages on pushes to `main` or via manual dispatch. A live Pages URL is not documented here because none is verified in the repository metadata.

## Current limitations

- The sign-in, tournament, “Start Gaming Now,” “Watch Tournaments,” and “View All Games” controls are presentational controls without application handlers or destination routes.
- The contact form has no `action` attribute or JavaScript submission handler, so it does not send messages from this repository.
- Social icons point to generic platform homepages, while several footer entries and policy links use `#` placeholders.
- Contact details, sponsor artwork, game catalogue entries, statistics, and team information are static content in the page; they are not loaded from an external service.
