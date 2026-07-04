# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **GitHub profile README** repo (`davidktx/davidktx`). Its only
"product" is `README.md`, which GitHub renders on the owner's profile page. There is
**no application code, no build step, no automated tests, and no lint config** here —
just `README.md` and `.vscode/settings.json`.

### Previewing the README (the closest thing to "running" this repo)

The README uses GitHub-Flavored Markdown (headings, rules, an embedded
`github-readme-stats` image). To preview it exactly as GitHub renders it, use
[`grip`](https://github.com/joeyespo/grip) (a Python tool installed by the update
script into `~/.local/bin`):

```bash
export PATH="$HOME/.local/bin:$PATH"   # grip installs here (not on PATH by default)
grip README.md 0.0.0.0:6419           # serve at http://localhost:6419/
```

Caveats:
- `grip` renders by calling GitHub's Markdown API. Without a token it works for light
  use but is rate-limited; set `GRIP_ACCESS_TOKEN` (or pass `--user`/`--pass`) if you
  hit HTTP 403 rate limits.
- The embedded `github-readme-stats.vercel.app` image only loads when the preview has
  outbound network access; offline it will show a broken image, which is expected.

### Editing guidance

- Keep changes limited to `README.md` content unless explicitly asked otherwise.
- There is nothing to lint/test/build — validation = visually confirming the rendered
  Markdown in `grip`.
