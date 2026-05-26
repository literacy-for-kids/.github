# Contributing to Literacy for Kids

Thanks for your interest in contributing. This is an open-source curriculum project — built by educators, parents, and developers who think kids deserve better explanations of the world they're already living in.

---

## Who this project is for

These curricula are written for facilitators: parents at the kitchen table, classroom teachers, homeschool families, after-school program leaders, librarians. Contributions that make the lessons clearer, more accurate, or easier to run are always welcome.

You don't need to be a subject-matter expert to contribute. If something confused you when you read it, it probably confuses learners too — that's a good starting point.

---

## What's welcome

- **Typo and grammar fixes** — open a PR directly
- **Lesson clarity improvements** — rewording, tightening, removing jargon
- **New activities or discussion questions** — additions that fit the existing week's scope
- **Factual corrections** — with a source if the change is substantive
- **Site code improvements** — Docusaurus config, component fixes, CSS, accessibility
- **Translation** — open an issue first to coordinate before translating a full curriculum

---

## What's out of scope (open an issue first)

- **Changing the core pedagogical approach** — the project has a deliberate framework (systems thinking, discussion over memorization, age-appropriate depth). If you think something about that framework is wrong, open an issue to discuss it before making changes.
- **Adding an entirely new curriculum topic** — new topics require planning, scoping, and a full 18-week structure. Open an issue using the *New Curriculum Idea* template so we can discuss fit before any writing starts.

If you're not sure whether your idea is in scope, open an issue and ask. It's faster than guessing.

---

## Repository structure

Each curriculum lives in its own repository. All lesson content is Markdown files under `website/docs/`:

```
{curriculum}_literacy_for_kids/
  website/
    docs/            ← lesson content lives here (edit these)
    src/             ← React page components
    static/img/      ← logos, hero images, favicons
    docusaurus.config.js
    sidebars.js
```

The hub site (`literacy_for_kids`) is the exception — its docs live at the repo root under `docs/` with no `website/` subdirectory.

The shared theme and ecosystem data (navbar links, footer, curriculum metadata) live in `literacy_site_template`. Changes there affect all nine curriculum sites.

---

## How to run a site locally

```bash
git clone https://github.com/literacy-for-kids/{repo-name}.git
cd {repo-name}/website      # omit /website for the hub repo
npm install
npm run start
```

The site opens at `http://localhost:3000`. Live-reload is on by default, so edits to Markdown files appear immediately.

To check for broken links before submitting:

```bash
npm run build
```

A successful build with no errors means the site is clean.

---

## Workflow

1. **Fork** the relevant repo on GitHub
2. **Create a branch** off `main` — see naming conventions below
3. **Make your changes** in `website/docs/` (or wherever appropriate)
4. **Run the site locally** to verify your changes look right
5. **Open a pull request** against `main` — fill in the PR template

For small fixes (typos, one-line corrections), you can use GitHub's web editor directly without cloning.

---

## Branch naming

```
content/short-description     ← lesson content changes
fix/short-description          ← bug fixes, broken links, site errors
docs/short-description         ← README or documentation updates
chore/short-description        ← dependency updates, config housekeeping
```

Keep it lowercase, use hyphens, keep it under 40 characters.

---

## Commit message style

Follow the pattern already in use across the repos:

```
type(scope): short description in lowercase
```

**Types:** `fix`, `content`, `docs`, `chore`, `feat`, `refactor`

**Scope:** the file, component, or topic being changed — e.g., `navbar`, `week-03`, `sidebar`, `readme`, `deps`

**Examples:**
```
fix: correct broken link in week 7
content(week-03): clarify barter activity instructions
docs(readme): update local setup instructions
chore(deps): update literacy-site-theme lockfile
feat(sidebar): add glossary link to Financial sidebar
```

First line under 72 characters. Add a blank line and a body paragraph if the change needs more explanation.

---

## Pull request expectations

A good PR:

- Has a title that describes what changed (not "Update week 3.md")
- Fills in the PR template — a sentence or two is fine for small changes
- Doesn't bundle unrelated changes in the same PR
- Passes the build (`npm run build`) with no errors

For content changes, note the curriculum and week number in the PR title or description so reviewers can find it quickly.

---

## Questions

Open an issue or start a discussion. This is a small project — there's no bureaucracy, just a maintainer who reads GitHub notifications.
