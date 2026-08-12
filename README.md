# Dinosaur 3D Field Guide

A standalone 3D dinosaur education demo for classroom-style visual learning. It includes a neon sci-fi interface, a central interactive 3D viewer, dinosaur video cards, and switchable skin/skeleton modes.

## Live Demo

This repository is designed to run as a static site on GitHub Pages.

## Features

- Standalone `index.html` demo.
- Interactive Three.js dinosaur viewer with drag rotation and wheel zoom.
- Skin / skeleton view switching.
- Dinosaur media and profile panel.
- Optimized MP4/WebP assets for smoother loading.
- Procedural model fallback when real GLB files are not included.

## Run Locally

```bash
python3 -m http.server 5175
```

Open:

```text
http://127.0.0.1:5175/
```

A local server is recommended because browser `file://` mode can block model loading.

## Asset Notes

This open-source package intentionally uses compressed videos and WebP posters to keep the repository lightweight. The original heavy GLB dinosaur files are not included in this release package. If you want to restore real GLB models, put them back at the paths referenced by `assets/dino-demo-runtime.js`, for example:

- `assets/tyrannosaurus/tyrannosaurus rex 3d model.glb`
- `assets/tyrannosaurus/tyrannosaurus skeleton 3d model.glb`
- `assets/triceratops/triceratops.glb`
- `assets/triceratops/triceratops-skeleton.glb`
- `assets/pterosaur/pterosaur.glb`
- `assets/pterosaur/pterosaur-skeleton.glb`
- `assets/velociraptor/velociraptor.glb`
- `assets/velociraptor/velociraptor-skeleton.glb`

When those files are missing, the app falls back to procedural demo models instead of breaking.

## Project Structure

```text
index.html
assets/
  dino-demo-runtime.js
  ui/
  tyrannosaurus/
  triceratops/
  pterosaur/
  velociraptor/
```

## License

MIT
