<div align="center">

# Pixel Doraemon for Codex

**[简体中文](./README.md) · English**

A retro pixel-art Doraemon companion with his bell and four-dimensional pocket.

<img src="./doraemon/previews/idle.gif" width="192" alt="Pixel Doraemon" />

</div>

## Quick Install

Send this instruction to Codex:

```text
Install and enable this pixel Doraemon pet: https://github.com/ChenFu0604/codex-pet-doraemon . Use doraemon/pet.json and doraemon/spritesheet.webp from the repository and install them in my Codex custom pets folder.
```

## Animation Preview

<div align="center">

<table>
  <tr>
    <td align="center"><strong>Idle</strong><br /><img src="./doraemon/previews/idle.gif" width="160" alt="Doraemon Idle" /><br /><code>idle</code> · 6 frames</td>
    <td align="center"><strong>Wave</strong><br /><img src="./doraemon/previews/waving.gif" width="160" alt="Doraemon Wave" /><br /><code>waving</code> · 4 frames</td>
    <td align="center"><strong>Jump</strong><br /><img src="./doraemon/previews/jumping.gif" width="160" alt="Doraemon Jump" /><br /><code>jumping</code> · 5 frames</td>
  </tr>
  <tr>
    <td align="center"><strong>Move left</strong><br /><img src="./doraemon/previews/running-left.gif" width="160" alt="Doraemon Move left" /><br /><code>running-left</code> · 8 frames</td>
    <td align="center"><strong>Working</strong><br /><img src="./doraemon/previews/running.gif" width="160" alt="Doraemon Working" /><br /><code>running</code> · 6 frames</td>
    <td align="center"><strong>Move right</strong><br /><img src="./doraemon/previews/running-right.gif" width="160" alt="Doraemon Move right" /><br /><code>running-right</code> · 8 frames</td>
  </tr>
  <tr>
    <td align="center"><strong>Needs input</strong><br /><img src="./doraemon/previews/waiting.gif" width="160" alt="Doraemon Needs input" /><br /><code>waiting</code> · 6 frames</td>
    <td align="center"><strong>Ready to review</strong><br /><img src="./doraemon/previews/review.gif" width="160" alt="Doraemon Ready to review" /><br /><code>review</code> · 6 frames</td>
    <td align="center"><strong>Failed or blocked</strong><br /><img src="./doraemon/previews/failed.gif" width="160" alt="Doraemon Failed or blocked" /><br /><code>failed</code> · 8 frames</td>
  </tr>
</table>

</div>

### Look Directions

<p align="center">
  <img src="./doraemon/previews/look-loop.gif" width="192" alt="Doraemon looking in sixteen directions" /><br />
  <code>look directions</code> · 16 directions
</p>

[All-state GIF](./doraemon/previews/all-states.gif) · [MP4 preview](./doraemon/previews/all-states.mp4) · [Idle → jump → idle](./doraemon/previews/idle-jump-idle.gif) · [Contact sheet](./doraemon/previews/contact-sheet.png)

## Manual Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/ChenFu0604/codex-pet-doraemon.git
   ```

2. In the Codex App, open **Settings → Pets → Custom pets → Open folder**.
3. Copy the repository's `doraemon` folder into that directory.
4. Return to the Codex App, click **Refresh**, then select 「哆啦A梦」.

### macOS / Linux

```bash
git clone https://github.com/ChenFu0604/codex-pet-doraemon.git
pet_codex_root="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$pet_codex_root/pets/doraemon"
cp -R codex-pet-doraemon/doraemon/. "$pet_codex_root/pets/doraemon/"
```

### Windows PowerShell

```powershell
git clone https://github.com/ChenFu0604/codex-pet-doraemon.git
$petCodexRoot = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME ".codex" }
$petInstallDir = Join-Path $petCodexRoot "pets\doraemon"
New-Item -ItemType Directory -Force $petInstallDir | Out-Null
Copy-Item ".\codex-pet-doraemon\doraemon\*" $petInstallDir -Recurse -Force
```

## Web Asset

Desktop and web custom pets are managed separately. [`doraemon/web-spritesheet.png`](./doraemon/web-spritesheet.png) provides the `1536 × 1872` nine-row layout for upload interfaces that require it. Choose the file according to the upload interface's format requirements.

The desktop `spritesheet.webp` uses the `1536 × 2288` v2 layout, with nine animation states and sixteen look directions.

## Files

```text
doraemon/
├── pet.json
├── spritesheet.webp
├── web-spritesheet.png
└── previews/
    ├── idle.gif
    ├── waving.gif
    ├── jumping.gif
    ├── running-left.gif
    ├── running-right.gif
    ├── waiting.gif
    ├── running.gif
    ├── review.gif
    ├── failed.gif
    ├── look-loop.gif
    ├── all-states.gif
    ├── all-states.mp4
    ├── idle-jump-idle.gif
    ├── motion-stills.png
    ├── contact-sheet.png
    └── directions.png
```

- `pet.json`: desktop pet metadata.
- `spritesheet.webp`: transparent lossless WebP; an 8 × 11 grid of `192 × 208` cells, with 73 populated frames.
- `web-spritesheet.png`: transparent PNG; an 8 × 9 grid with 57 populated frames.
- `previews/`: previews rendered from the final spritesheet; not required at runtime.

## Credits and Artwork

- Repository structure and presentation inspired by [timerring/codex-pet-naiwa](https://github.com/timerring/codex-pet-naiwa).
- Pixel sprites generated with OpenAI image tools, with eye, animation, and look-direction corrections.
- Doraemon is a third-party character. This is an unofficial fan project.

## License

Original documentation and metadata use the [MIT License](./LICENSE). This license does not grant third-party rights in the Doraemon character, associated trademarks, or artwork.
