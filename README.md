<p align="center"> <img src="https://cdn.modrinth.com/data/r7pO04ED/images/0fc3204da18066142c38383080d7b542f594092b.png" alt="Rex Shaders" width="100%"> </p> <p align="center"> <b>A lightweight, FPS-friendly shader pack for Minecraft with a warm, nostalgic look.</b><br> Soft shadows · Reflective water · Dynamic sky · Atmospheric fog · Waving plants </p> <p align="center"> <a href="https://modrinth.com/shader/rexshader">Modrinth</a> · <a href="../../issues">Report a bug</a> · <a href="https://craftrank.org/">CraftRank</a> </p>

## ✨ Features

- **Soft shadows**: adjustable resolution, distance and filtering, with slope-aware bias against shadow acne
- **Reflective water**: animated waves, sky reflections, sun glare and screen-space reflections (SSR)
- **Dynamic sky**: warm sunrises and sunsets, deep blue nights, darker skies in rain
- **Atmospheric fog**: distance haze that thickens during rain and hides chunk borders
- **Waving plants**: leaves, grass, flowers, crops and tall plants sway in the wind
- **Glowing light sources**: lava, lanterns, glowstone, froglights and more, with soft bloom
- **Underwater, lava and powder snow fog**
- **Nether and End support**: custom lighting with the shadow pass disabled for extra FPS
- **Depth of field (optional)**: for cinematic screenshots

## ⚡ Performance Presets

| Preset | Shadow map | Shadow distance | Reflections | Bloom | DOF | Best for |
|---|---|---|---|---|---|---|
| **Low** | 512 | 64 | Off | Off | Off | Laptops / integrated graphics |
| **Medium** *(default)* | 1024 | 96 | 12 steps | On | Off | Most systems |
| **High** | 2048 | 128 | 16 steps | On | Off | Dedicated GPUs |
| **Ultra** | 3072 | 160 | 24 steps | On | On | High-end PCs / screenshots |

Need more FPS? Lower **Shadow Quality** and **Shadow Distance**, or turn off **Water Reflections** first. These three settings have the biggest impact.

## 📦 Requirements

- Minecraft **1.21.x**
- **[OptiFine](https://optifine.net/downloads)** (latest version for your Minecraft version)

> Iris compatibility has not been tested yet.

## 🔧 Installation

1. Install OptiFine and launch the game with the OptiFine profile.
2. Open **Options → Video Settings → Shaders → Shaders Folder**.
3. Put the `.zip` file into that folder. Don't extract it.
4. Select **Rex Shaders** from the list.

To install from source, copy the `shaders` folder into a new folder inside `shaderpacks`, or zip it so the `shaders` folder is at the root of the zip.

## 🎛️ Settings

All options are available in-game under **Shader Options**, grouped into:

- **Shadows**: quality, distance, softness, sun angle
- **Lighting**: sun, ambient and torch brightness, exposure
- **Water**: waves, wave speed, transparency, reflections, reflection quality
- **Atmosphere**: fog density, waving plants, wind strength
- **Effects**: bloom, depth of field, saturation, vignette

Option names are available in **English** and **Turkish**.

## 🗂️ Project Structure

```
shaders/
├── lib/                 # Shared code (settings, lighting, shadows, sky, water, waving)
├── program/             # Actual shader programs
├── world-1/             # Nether overrides (no shadows, warm lighting)
├── world1/              # End overrides (no shadows, purple lighting)
├── lang/                # en_us / tr_tr option names
├── *.vsh / *.fsh        # Overworld entry points (include files from program/)
├── block.properties     # Block IDs for waving plants, water and emissive blocks
└── shaders.properties   # Presets, menu layout and sliders
```

Entry files are thin wrappers: each one sets dimension or program defines (`NETHER`, `END`, `ENTITY`, `HAND`, `NO_SHADOW`) and includes the shared program from `program/`.

## 🐛 Bug Reports

Found a visual glitch? [Open an issue](../../issues) and include:

- A screenshot of the problem
- Minecraft and OptiFine version
- Your GPU (e.g. GTX 1060, RX 6600, Intel UHD)
- The preset you were using

## 📝 Changelog

### 1.1.0
- First public release
- Fixed striped shadow artifacts (shadow acne) at low sun angles
- Reduced the yellow color tint, more natural sunlight
- Fixed white blocky artifacts in water reflections

## 📄 License

See [LICENSE](LICENSE).

---

<p align="center">
  Rex Shaders is an original shader pack written from scratch.<br>
  Looking for a server to try it on? Find one on <a href="https://craftrank.org">CraftRank</a>.
</p>
