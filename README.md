# NovelAI Image Static

Pure static NovelAI image generation page.

## Run Locally

```bash
python3 -m http.server 8080
```

Open:

```text
http://localhost:8080/
```

## Deploy

Upload this directory to GitHub Pages. The app uses relative paths, so it can run from a repository subpath.

## Token Storage

- By default, the NovelAI token is saved only in `sessionStorage`.
- If `記住 Token` is checked, the token is saved in `localStorage`.
- The token is not written to image metadata, exported settings, URLs, or repo files.

## Local Data

- Settings draft, prompt snippets, and local defaults are stored in `localStorage`.
- Generated image history is stored in IndexedDB.
- Bundled defaults are loaded from `defaults/novelai-defaults.json`.
- `保存預設` saves the current defaults to this browser.
- `啟用預設` applies this browser's saved defaults first, then falls back to bundled defaults.
- `下載預設` exports a defaults JSON file.
- `注入預設` imports a defaults JSON file, saves it to this browser, and applies it.
- Image downloads can be saved with prompt metadata or as a pure image.

Before publishing a public repository, review `defaults/novelai-defaults.json` and remove any private prompt content.
