# deskhud theme

The top bar of [deskhud-suite](https://github.com/BigJonGoodwin/deskhud): GlazeWM tiling, this YASB bar,
and deskhud (the bar's left island, hotkeys, wallpaper colours). YASB's adaptive style: a black rail
fused to the screen bezel with islands hanging off it, glows coloured from the wallpaper.

| File | What it is |
|---|---|
| `config.yaml` | Widgets and clicks. The left side is empty because deskhud draws that island. |
| `styles.css` | The look. Imports `deskhud_colors.css`. |
| `deskhud_colors.css` | A default palette. deskhud rewrites it from the current wallpaper as soon as it runs. |

## Install

deskhud-suite's `install.ps1` copies these files to `%USERPROFILE%\.config\yasb\` (backing up what is
there). By hand: copy the three files there and restart YASB.

## Requirements

- YASB with the adaptive bar style and the audio visualizer widget: the preview build, or 2.0.8 and
  later. The stable 2.0.7 release drops the bar style and the visualizer.
- A Nerd Font (the icons are `nf-md-*` glyphs, written as `\uXXXX` surrogate-pair escapes; keep them
  escaped when editing).
- deskhud at `%LOCALAPPDATA%\Programs\deskhud-suite\bin\deskhud.exe` (the wallpaper, weather and
  cheatsheet buttons call it there) and its state folder `%LOCALAPPDATA%\deskhud\` (the ticker reads
  `ticker.json` from it).
- GlazeWM for the tray menu's Start / Stop / Reload entries; Start runs the `\deskhud-suite\GlazeWM`
  logon task.

Without deskhud, put a `glazewm.workspaces.GlazewmWorkspacesWidget` in `widgets.left` (an example is in
the comments at the top of `config.yaml`) and drop the wallpaper, cheatsheet and ticker widgets.
