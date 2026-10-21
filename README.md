# Focusima — Web Build

A prebuilt Unity WebGL game wrapped in a custom, portrait-oriented browser player.

## Play locally

Serve the repository root over HTTP:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Open `http://localhost:8000` in a browser with WebGL and WebAssembly support. Wait for the Unity data download; the build is substantially larger than a typical static page.

## Repository contents

- `index.html` — responsive player shell, loading UI and Unity startup.
- `Build/` — generated Unity loader, framework, WebAssembly and data files.
- `TemplateData/` — player assets.

## Development scope

This repository distributes a browser build. It does not include the Unity `Assets/`, `Packages/` and `ProjectSettings/` directories needed to edit or rebuild the game. Player-shell changes can be made here; gameplay changes require the original Unity project.

If a host reports compression or MIME errors for `.unityweb` assets, configure it for the Unity export's compression settings. Gameplay and hosting compatibility have not been verified by the documentation review.
