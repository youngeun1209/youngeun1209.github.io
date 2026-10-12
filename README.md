# youngeun1209.github.io

Personal academic website of **Young-Eun Lee**, Postdoctoral Researcher at Stanford University (brain-computer interfaces and neural decoding).

Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme.

## Editing the content

| What | File |
| --- | --- |
| Intro / bio / profile photo position | `_pages/about.md` |
| Publications | `_bibliography/papers.bib` |
| Patents | `_pages/patents.md` |
| CV (education, experience, skills, service) | `_data/cv.yml` |
| Social links (email, Scholar, GitHub, LinkedIn) | `_data/socials.yml` |
| Site-wide settings (name, navbar, theme) | `_config.yml` |
| Profile photo | `assets/img/prof_pic.jpg` |
| Shared profile and page tabs | `_includes/profile-sidebar.liquid`, `_includes/page-tabs.liquid` |
| Shared page layout / About layout | `_layouts/default.liquid`, `_layouts/about.liquid` |
| Layout, responsive styling, accent | `assets/css/main.scss` |
| Design decisions | `DESIGN.md` |

## Deploy

Pushing to `main` triggers the **Deploy site** GitHub Action, which builds the site and publishes it to the `gh-pages` branch. In the repository settings, GitHub Pages must be configured to serve from the `gh-pages` branch.

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.
