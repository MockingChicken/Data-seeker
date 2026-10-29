# Data Seeker – how this project fits together

Read this before changing the app. The owner asks Claude for changes in plain words; keep every copy in step.

## The pieces
1. **This repo / website:** https://mockingchicken.github.io/Data-seeker/ (capital D – Pages paths are case-sensitive).
   - `index.html` is the whole app and the source of truth for its code. Edit it directly.
2. **claude.ai page:** https://claude.ai/artifact/6auTHpvk5ZVbJvBEy2aKgy – a preview copy of the same file (capability: `downloads`). The claude.ai viewer blocks requests to NCBI, ENCODE and EBI, so searching only works on the website or a downloaded copy.
3. **claude.ai project "Data seeker":** keeps `claude/data-seeker.html`, another copy of the same file.

## Rules when changing the app
- Follow the Roberts Lab app house style (the `roberts-lab-app-style` skill): header, numbered tabs (Search, Download list, About), About page, workspace save/load, and the multiple-tabs storage rules.
- Keep the browser storage keys backwards compatible, or people lose their saved work: workspaces under `dataseeker.doc.<id>`, the tab's workspace id in sessionStorage `dataseeker.tabdoc`, shared preferences in `dataseeker.prefs`, file handles in IndexedDB `dataseeker`. Older `ds.*` keys are migrated on first run.
- Bump `ABOUT.version` and add a Version history entry with every change.
- Test before pushing: page loads with no console errors in light and dark themes and at phone width; a search against mocked GEO/ENCODE/ArrayExpress responses fills the results; star, Saved panel, download list panel and file list export work; two tabs keep separate workspaces after a reload.
- After pushing, republish the claude.ai page and update the project copy with the same file.
- Commit as Claude <noreply@anthropic.com> so commits show as verified on GitHub.
