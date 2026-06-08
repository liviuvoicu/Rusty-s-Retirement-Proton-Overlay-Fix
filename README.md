# Rusty's Retirement Proton Overlay Fix

A compatibility mod for **Rusty's Retirement** running under **Proton/Wine on Linux**.

This mod fixes the black-screen issue caused by the game's Windows transparency modes and provides optional window positioning and always-on-top behavior.

---

## Features

- Fixes the Linux/Proton black-screen issue
- Forces a working window mode under Proton
- Optional automatic window positioning
- Optional always-on-top behavior
- Supports multi-monitor setups
- Works with horizontal and vertical farms

---

## Requirements

- Rusty's Retirement
- Steam
- Proton Experimental (recommended)
- BepInEx 5 (Windows x64 version)

---

## Installation

### 1. Install This Mod

Download the latest release.

Extract the archive directly into your Rusty's Retirement game folder.

Allow files to merge if prompted.

### 2. Configure Steam Launch Options

Open:

```text
Steam
→ Library
→ Rusty's Retirement
→ Properties
→ Launch Options
```

Add:

```bash
WINEDLLOVERRIDES="winhttp=n,b" %command%
```

### 3. Launch The Game

The configuration file will be generated automatically on first launch.

---

## Configuration

The config file is located at:

```text
BepInEx/config/mrrp.rustys.protonoverlayfix.cfg
```

### Default Configuration

```ini
[Fixes]
ForceTransparencyMode = true
ForcedTransparencyMode = 3

[Window]
MoveWindowOnStartup = true
ForceAlwaysOnTop = true
Anchor = BottomCenter
OffsetX = 0
OffsetY = 0
```

---

## Transparency Modes

| Mode | Description |
|--------|--------|
| 0 | Black color-key transparency |
| 1 | Alpha transparency |
| 2 | Green color-key transparency |
| 3 | Plain/Cropped Window |

### Recommended

```ini
ForcedTransparencyMode = 3
```

### Notes

Mode 3 is currently the only reliable option on Linux.

---

## Moving The Window

Rusty's Retirement uses a frameless window.

Most Linux desktop environments provide a shortcut for moving frameless windows.

### KDE Plasma

```text
Super + Left Mouse Drag
```

### GNOME

```text
Alt + Left Mouse Drag
```

### XFCE

```text
Alt + Left Mouse Drag
```

### Cinnamon

```text
Alt + Left Mouse Drag
```

### MATE

```text
Alt + Left Mouse Drag
```

### LXQt

```text
Alt + Left Mouse Drag
```

### Hyprland

```text
Super + Left Mouse Drag
```

If these shortcuts don't work, check your window manager settings.

---

## Known Limitations

### Desktop Transparency

The original Windows transparency effects are currently not functional under Proton.

### Always-On-Top Behavior

Always-on-top support may vary depending on:

- Desktop Environment
- Window Manager
- Wayland vs X11
- Proton version

---

## Tested On

- Garuda Linux
- KDE Plasma
- Wayland
- Proton Experimental

---

## Credits

- Mister Morris Games
- BepInEx Team
- Harmony Team
- Wine Developers
- Proton Developers

---

## Disclaimer

This is an unofficial fan-made compatibility mod and is not affiliated with Mister Morris Games.
