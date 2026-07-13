# Battlefield Editor v1.0 - 3D Engine 2026

> **A single-file, data-first 3D battlefield simulator built with Three.js for modeling historical engagements through configurable terrain, multiple factions, and live editing tools.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/noahio94/battlefield-sim-editor?style=flat-square)](https://github.com/noahio94/battlefield-sim-editor)

---

<p align="center">
  <a href="https://noahio94.github.io/battlefield-sim-editor/">
    <img src="https://img.shields.io/badge/Download-Battlefield%20Editor%20Latest-brightgreen?style=for-the-badge" alt="Download Battlefield Editor">
  </a>
</p>

> **[Download Battlefield Editor v1.0](https://noahio94.github.io/battlefield-sim-editor/)**

---

[Download Latest Build](https://noahio94.github.io/battlefield-sim-editor/)

---

## Overview

Battlefield Editor is a compact, browser-run 3D engine aimed at historians, strategy fans, and AI practitioners who want to study or rebuild battlefield scenes from the past. Because everything lives inside one HTML file, it is easy to move, copy, and open without extra setup. Each scenario is delivered as its own data bundle, with supported examples including the Battle of Red Cliffs, Guandu, Gaixia, and Feishui.

Its core strength is the data-driven design. Rather than embedding terrain logic or unit rules directly in code, the engine consumes a six-layer schema that describes analog terrain, declarative effects, audio vocabulary, and faction setup. That makes it straightforward to switch scenarios by loading another package, and the AI authoring loop supports generating and refining new ones through repeated iteration.

---

## Capabilities

- **Single-file, data-driven 3D engine** - Runs the full battlefield simulation from one HTML file, with no server-side dependency
- **Parameterized analog terrain** - Shape elevation, vegetation, and obstacles through layered data instead of hand-built models
- **Declarative effects and audio vocabulary** - Configure weather, explosions, and ambient soundscapes with simple definitions
- **Multi-faction support** - Set up rival armies, their units, and their behaviors separately
- **Replaceable models (glTF)** - Use custom 3D assets in the standard glTF format
- **Editor mode with real-time editing** - Adjust battle values live and see the result immediately
- **Six-layer data schema** - Organized model covering terrain, units, effects, audio, factions, and metadata
- **AI authoring loop** - Create and iterate on battle scenarios with AI-assisted refinement

---

## Setup

1. Clone the repository or download the single HTML file:
   ```bash
   git clone https://github.com/noahio94/battlefield-sim-editor.git
   ```
2. Open `index.html` directly in any modern web browser (Chrome, Firefox, Edge, Safari)
3. No build tools, package managers, or server required

---

## How to Use

1. **Open the editor** - Launch `index.html` in your browser
2. **Load a battle package** - Pick one of the included examples (Red Cliffs, Guandu, Gaixia, Feishui) or import your own
3. **Inspect the battlefield** - Use mouse controls to orbit, pan, and zoom around the 3D scene
4. **Edit live** - Turn on editor mode to change terrain parameters, unit placement, or effect settings
5. **Export your scenario** - Save the updated battle as a new package for sharing

Example workflow:
```bash
# Open the editor
open index.html

# In the interface:
# 1. Click "Load Package" -> Select "chibi.json" (Red Cliffs)
# 2. Use editor panel to adjust terrain roughness
# 3. Click "Export" to save your custom version
```

---

## Configuration

Every setting is stored inside the battle package files in JSON format. The engine interprets a six-layer schema:

- **Terrain layer** - Elevation map, ground textures, obstacles
- **Unit layer** - Faction assignments, unit types, formations
- **Effects layer** - Weather, fire, smoke, particle systems
- **Audio layer** - Ambient sounds, battle cries, impact effects
- **Faction layer** - Army colors, banners, AI behavior parameters
- **Metadata layer** - Battle name, historical context, version info

To change default behavior, edit the matching JSON fields in your battle package or use the built-in editor interface.

---

## Requirements

- **Platform**: Any modern web browser (Chrome 90+, Firefox 88+, Edge 90+, Safari 14+)
- **Runtime**: No server required - runs entirely client-side
- **Storage**: ~5 MB for the engine file; battle packages range from 50 KB to 2 MB each
- **Hardware**: WebGL-capable GPU recommended for smooth 3D rendering
- **Network**: Internet connection only needed for loading external glTF models

---

## FAQ

**How do I update the engine?**  
Download the newest HTML file from the repository. Existing battle packages should continue to work across versions.

**Can I add my own 3D models?**  
Yes. glTF is supported. Put the model files next to the HTML file and point to them from your battle package configuration.

**Does it work offline?**  
Yes. After downloading, the single HTML file operates fully offline and does not contact a server.

**How do I create a new battle scenario?**  
Use editor mode to build the battlefield and export the package, or author a JSON file by hand using the six-layer schema.

**What if I encounter a visual glitch?**  
Try turning off hardware acceleration in the browser or updating your graphics drivers. Most problems come from WebGL compatibility.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
