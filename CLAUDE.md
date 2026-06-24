# spatialMemory_Concept — Claude configuration

This repo is the **design-doc canvas** for the Spatial Memory paper (sibling repo:
`~/Documents/Papers/spatialMemory`). It is a static site on GitHub Pages
(`worning77/spatialMemory_Concept`, `main` branch, root). No build step, no framework.

## Structure: four tabs, one page each

The site is a tabbed canvas. The header nav (`.tabs`) is the same on every page; each
page is a **standalone HTML file** that marks its own tab active. This is deliberate:
one person owns each file, so two collaborators edit concurrently without git conflicts.

| Tab | File | Owner | Purpose |
|-----|------|-------|---------|
| Full Doc | `design_doc.html` | both | Complete design document (full text) |
| Concept | `concept.html` | Chenfeng | Condensed concept (one screen) |
| Plan | `plan.html` | Chenfeng | Timeline + condensed study plan |
| Storyboard | `storyboard.html` | YY | Scenario as panels |

- `style.css` — shared stylesheet for ALL tabs (extracted from the original inline CSS
  in `design_doc.html`, plus `.tabs` nav styles). Edit sparingly; it affects every tab.
- `index.html` — redirect to `design_doc.html`.
- `scenario_7day.html` — legacy, superseded.

## Rules when working here

1. **Edit one tab's file only** for a given piece of content. Never split one tab across files.
2. **Shared changes** (look/feel) go in `style.css`. Touch it only when a change should apply to all tabs.
3. **Adding a tab:** copy an existing page to `newtab.html`, change its `<title>`/`<h1>`/active
   link, then add one `<a>` to the `.tabs` block **in every page** (nav is duplicated per page).
   Update the table above + `README.md`.
4. **Condensing from the full doc:** the source of truth for content is `design_doc.html`
   (and the paper repo's `Docs/`). Condensed tabs paraphrase it; keep section ids stable.
5. `git pull` before editing, `git commit` + `git push` (branch `main`) after.

## Pages / collaborators

- GitHub Pages: Settings → Pages → `main` / root → resolves to `design_doc.html` via redirect.
- Collaborator push access: Settings → Collaborators → Add people.
