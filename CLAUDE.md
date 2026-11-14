# Literature repo — working context for Claude Code

This repo holds **writing projects**, not code. Each work lives in its own
top-level folder. Everything is plain markdown. There is nothing to build, lint
or test.

## Works

| Folder | Work | Context file |
|---|---|---|
| `mirrorface/` | The Mirror Face — psychological drama, trilogy/series potential | `mirrorface/CLAUDE.md` |

When working on a piece, read that folder's `CLAUDE.md` first. It holds the
premise, the craft notes, the guardrails and the open decisions for that work,
and it takes precedence over this file for anything inside its folder.

## Adding a new work

- One top-level folder per work, lowercase, no spaces (e.g. `mirrorface/`).
- Give it a `README.md` (short human-facing overview and status) and a
  `CLAUDE.md` (premise, what's decided, what's open, what to protect).
- Add a row to the table above and to the root `README.md`.
- Usual subfolders, created as needed: `outlines/`, `treatments/`, `drafts/`,
  `notes/`.

## Working rules (all works)

- **Existing outlines, treatments and drafts are the author's source text.**
  Don't rewrite or "improve" them in place unless asked. New work goes in new
  files.
- **Keep works separate.** Don't carry characters, devices or decisions from
  one work into another unless asked.
- **Don't reconstruct missing material from summaries.** If a document is
  referenced but not in the repo, ask for the source text.
- **Don't treat open decisions as settled.** Say which assumption a draft
  rests on.
- **Give honest evaluation.** Flag cliché, saturation and anything that breaks
  a work's own guardrails. Don't praise by default.
- **One change per commit, prefixed with the work's folder name, with a
  message that says what moved in the story** (e.g. "mirrorface: V3 add fourth
  ending beat sheet"), so the history reads as a development log.
- **Use branches for alternatives** (a different ending, a different POV
  scheme) rather than overwriting, so versions can be compared with a diff.
