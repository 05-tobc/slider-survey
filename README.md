# SCS Survey Demo UI

This project is a small static demo site that recreates a survey interface inspired by the provided design reference.

The goal is to present a clean, modern, and intuitive questionnaire experience with a strong focus on visual polish, smooth interaction, and universal accessibility.

The page is intended to feel lightweight and calm, with clear visual hierarchy, generous spacing, and responsive behavior across desktop and mobile screen sizes. The interface should support accessible navigation, readable typography, sufficient contrast, keyboard usability, and screen-reader-friendly structure so the experience works well for a broad range of users.

## Scope

This is a deliberately small front-end project:

- A single statically served page
- No backend or database
- No authentication or account flows
- No complex application state

Its purpose is to demonstrate thoughtful UI design, accessible form interaction, and a refined front-end presentation in a simple local setup.

## Design Goals

- Clean and modern visual language
- Smooth and intuitive survey flow
- Strong readability and clear layout hierarchy
- Responsive behavior across devices
- Accessibility-first interaction patterns

## Accessibility Priorities

- Semantic HTML structure
- Keyboard-accessible controls
- Clear focus states
- Good color contrast
- Legible typography
- Screen-reader-friendly labels and grouping

## Local Use

This project is designed to run locally as a static page. Open or serve `index.html` in a local browser environment to view the demo.

## Deployment

The `main` branch is published via GitHub Pages at https://05-tobc.github.io/slider-survey/. Pages deploys from the repo root, so any push to `main` automatically republishes the site (typically within ~30–60 seconds). No build step or workflow file is involved — `index.html` is served as-is.

## Current Direction

The prototype has moved away from a generic SaaS look toward an **editorial, paper-and-ink aesthetic**:

- Type pairing: Fraunces (variable serif) for display, IBM Plex Sans for body, IBM Plex Mono for labels and metadata.
- Palette: warm paper (`--paper`, `--page`) with ink text and a single clay accent (`--accent: #b8501f`), supported by ochre, moss, slate, and plum used sparingly per-driver.
- Hero: paper disc with three satellites budding from its edge and hairline spokes to center — no orbiting separate rings.
- Driver cards: each of the 12 drivers is its own card with header band (icon + name + definition) and two sliders (Own/Individual, Others/Communal) with a mood-icon column.
- Scenario card with tab switcher: "General" vs. "Bridge closure" — answers persist independently per scenario.
- Topbar language switcher (EN · NO), segmented pill, 42px to match neighboring controls; Norwegian (Bokmål) is fully translated and persists via localStorage.

### Design constraints (durable)

- Make **small, targeted refinements**, not wholesale redesigns.
- **Keep the mood-icon column** next to each slider — it's load-bearing for the interaction.
- Translations must be native-quality Bokmål, not literal.

## Working with the `frontend-design` skill

This repo uses the `frontend-design` plugin skill (`plugin:frontend-design:frontend-design`) for visual passes. When invoking it:

- Frame the ask as a **refinement** of the current editorial direction, not a fresh aesthetic exploration — otherwise the skill will pull toward maximalist or generic AI-design defaults.
- Pass concrete constraints in the prompt: keep structure, keep mood-icon column, keep the paper/ink/clay palette, keep Fraunces + Plex pairing.
- Good targets for the skill: hero composition, driver-card hierarchy, comparison-section polish, micro-interactions on sliders. Bad targets: anything that would restructure the survey flow or replace the type system.
