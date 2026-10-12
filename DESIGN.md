# Design

## Source of truth
- Status: Active
- Last refreshed: 2026-10-11
- Primary product surfaces: About, Projects, Publications, Patents, Software & Datasets, CV, and project details.
- Evidence reviewed: `_pages/`, `_data/socials.yml`, `assets/css/main.scss`, `_config.yml`, the installed al_folio_core 1.0.11 layouts, and https://jaemin-shin.github.io/.
- Reference scope: borrow the persistent left identity column and generous right reading column only; retain this site's identity, content, links, and page routes. No pixel matching or copied reference assets.

## Brand
- Personality: clear, approachable, research-focused.
- Trust signals: existing portrait, Stanford affiliation, linked publications and public profiles.
- Avoid: marketing slogans, invented achievements, large decorative cards, unnecessary animation.

## Product goals
- Keep identity and key links available across pages and desktop scrolling.
- Make existing sections easy to navigate using a consistent row of page links.
- Success signals: one profile per page, correct active navigation, readable content, no overlap or horizontal page overflow.
- Non-goals: content rewrite, framework migration, new hosting provider.

## Personas and jobs
- Research collaborators and hiring teams: understand the research, inspect work and publications, find the CV and contact links.
- Context: desktop deep reading and quick mobile browsing.

## Information architecture
- Primary navigation: About, Projects, Publications, Patents, Software & Datasets, CV.
- Core routes: `/`, `/projects/`, `/publications/`, `/patents/`, `/open-source/`, `/cv/`.
- Persistent identity: portrait, name, role/affiliation, email, Google Scholar, GitHub, LinkedIn.
- Hierarchy: profile beside page navigation and title, followed by original page content.

## Design principles
- Identity stays in a shared layout; content stays in existing pages/data.
- Favor an open reading surface, restrained rules, and typographic hierarchy.
- A mobile profile stacks above content so it does not consume a permanent column.

## Visual language
- Color: existing burgundy #8a1a2f, theme text/background/divider variables.
- Typography: existing theme family, readable body copy, clear page titles and small profile metadata.
- Spacing: approximately 240px profile, 48–64px gutter, flexible reading column within a 1200px shell.
- Shape/elevation: gently rounded portrait, flat page tabs, minimal shadow.
- Motion: no new animation; honor reduced-motion preferences.
- Imagery: existing `assets/img/prof_pic.jpg` and project/publication assets only.

## Components
- Reuse theme head, scripts, figures, bibliography, CV renderer, search, and existing enabled theme controls.
- Local overrides: default/about layouts, profile-sidebar and page-tabs includes, scoped styles in main.scss.
- Tabs are ordinary route links; current page gets `aria-current="page"`. Project details keep Projects active.
- Token ownership stays in main.scss and the existing theme variables.

## Accessibility
- Target: WCAG 2.2 AA interaction and readable contrast.
- Visible keyboard focus, skip-to-content link, meaningful portrait alt text, semantic navigation and main region.
- Link labels remain readable without icon fonts; no content depends on animation or hover.

## Responsive behavior
- Desktop/tablet above 767px: two columns, sticky profile with a viewport-bounded scroll area on short screens.
- Mobile at 767px and below: compact portrait/profile at top, visible contact links, wrapping page navigation.
- Project cards: one column on small screens, two within the desktop content column.
- Validate around 390px, 768px, and desktop widths.

## Interaction states
- Loading: static HTML and eager profile image; no new loading state required.
- Empty: preserve theme/content behavior.
- Error: existing 404 page uses the same navigation.
- Success: selected page is reflected in URL, content, and active underline.
- Disabled: no disabled navigation items.
- Offline/slow network: route links and text labels work without new JavaScript; external resources retain existing behavior.

## Content voice
- Existing English academic content; user-facing development communication in Korean.
- Keep factual claims unchanged. Label links plainly and avoid implementation instructions in public copy.

## Implementation constraints
- Jekyll + al_folio_core 1.0.11; local Liquid overrides and existing Sass imports.
- No new dependencies or hosting migration.
- Preserve bibliography/CV plugins, site routes, and public profile data.
- Validate production build, rendered routes/assets, keyboard navigation, sticky behavior, and mobile screenshots.

## Open questions
- None blocking. Publication to GitHub Pages is a separate deployment action.
