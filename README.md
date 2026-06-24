# spatialMemory_Concept

Concept canvas for **Spatial Memory** — navigable asynchronous communication for shared physical workspaces.

## Four tabs (one site, header navigation)

Each tab is a **standalone HTML page** sharing `style.css`. One person owns each page, so two of us can work at the same time without git conflicts.

| Tab | File | Owner | What |
|-----|------|-------|------|
| Full Doc | [`design_doc.html`](./design_doc.html) | both | Complete design document (concept, why-not-Slack, full scenario, system, study plan) — the thing to read in full |
| Concept | [`concept.html`](./concept.html) | Chenfeng | One-screen condensed concept |
| Plan | [`plan.html`](./plan.html) | Chenfeng | Timeline + condensed study plan |
| Storyboard | [`storyboard.html`](./storyboard.html) | YY | Scenario drawn as panels |

`scenario_7day.html` — legacy pre-pivot 7-day scenario (superseded).

## How to work on it (read before editing)

1. `git pull` first.
2. Edit **only your own tab's file**. Never two people in the same file at once.
3. Shared look lives in `style.css` — edit sparingly (it affects every tab).
4. **To add a new tab:** create `newtab.html` (copy an existing page), then add one `<a>` to the `.tabs` nav **in every page** (the nav is duplicated per page so each can mark its own tab active).
5. `git commit` + `git push` when done.

No build step — pages open directly (double-click works) and render on GitHub Pages.

## Live

`https://worning77.github.io/spatialMemory_Concept/`

To enable: **Settings → Pages → Source: `main` / root**. The root resolves to `design_doc.html` via `index.html`.
**To let a collaborator push:** repo **Settings → Collaborators → Add people**.
