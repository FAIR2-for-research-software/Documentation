# CLAUDE.md

## Purpose

Carpentries Workbench lesson site for Research Software Documentation,
part of the FAIR² course at the University of Sheffield.
Published at <https://fair2-for-research-software.github.io/Documentation/>.

## Repository layout

- `config.yaml` — lesson metadata and episode order
- `episodes/` — primary content files (order defined in `config.yaml`)
- `learners/`, `instructors/`, `profiles/` — supplementary pages
- `links.md` — shared link definitions used across episodes
- `site/` — auto-generated; do not edit

## Running commands

Use `pixi` to run general utility commands — it manages the project's
conda environment and exposes tasks defined in `pixi.toml`.

```bash
pixi run lint                       # pre-commit run --all-files
pixi run spellcheck                 # codespell
pixi run build                      # sandpaper::build_lesson()
pixi run serve                      # sandpaper::serve()
pixi run check                      # sandpaper::check_lesson()
```

For ad-hoc commands not defined as tasks, use `pixi run <command>`
(e.g. `pixi run pre-commit run markdownlint-cli2 --all-files`).

Markdownlint runs with `fix: true` — it auto-corrects on pre-commit.

## Carpentries callout syntax

Episodes use fenced div callouts — see any existing episode for examples.
Types: `keypoints`, `objectives`, `challenge`, `solution`, `callout`, `prereq`, `discussion`.

## CI/CD

Workflow files in `.github/workflows/` are managed by `update-workflows.yaml` — do not edit manually.
