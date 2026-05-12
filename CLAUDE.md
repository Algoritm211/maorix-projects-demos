# Maorix — Projects Demo Portfolio

Static site hosted on GitHub Pages at https://algoritm211.github.io/maorix-projects-demos/

## Structure

```
projects-demos/
├── index.html          ← catalog page (list of all demos)
├── <project-slug>/
│   └── index.html      ← self-contained demo, no build step needed
└── ...
```

Each demo is a standalone `index.html` — no frameworks, no dependencies, no build step.

## Adding a project

Use the `/add-project` skill, or do it manually:

1. Drop a folder with `index.html` into the repo root (e.g. `my-feature/index.html`)
2. Add a card to `index.html` inside `.grid` — follow the existing card pattern:
   - `card-index`: next sequential number (e.g. `04`)
   - `card-title`: display name
   - `card-desc`: one-sentence description
   - `card-tag`: category label
   - `href`: `./my-feature/`
3. Commit and push — GitHub Pages deploys in ~1 min

## Brand

Company: **Maorix**. Colors defined in `index.html` `:root`:
- `--purple: #9d87c9` — primary accent
- `--purple-dim: #6d5d99` — dimmed accent / tags
- `--bg: #111111` — page background
- `--bg-card: #181818` — card background

Keep all new UI consistent with these tokens.

## Deploy

```bash
git add .
git commit -m "add: <project-name>"
git push
```

Remote: `https://github.com/Algoritm211/maorix-projects-demos`
