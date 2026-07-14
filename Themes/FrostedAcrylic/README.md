# Frosted Acrylic Sheet (Taskbar Theme)

**Author:** Evan (@EvanYFWong)  
**License:** MIT

## Overview
This is a Frosted Acrylic appearance theme for the Windows 11 Taskbar Styler. It gives the taskbar and system tray a unified, semi‑transparent frosted acrylic look while keeping a clean icon‑only layout. The theme prefers WindhawkBlur for blur rendering and falls back to an AcrylicBrush when WindhawkBlur is not available.

## Included files
- `theme.txt` — the theme definition (YAML) placed under `Themes/FrostedAcrylic/`.  
- `README.md` — this file.  
- `assets/` — example screenshots (e.g., `screenshot-1920x1080.png`).

## Tested resolutions & scaling
This theme has been tested and verified under the following display configurations:
- 1920×1080 @ 125%
- 1920×1080 @ 100%
- 1366×768 @ 125%
- 1680×1050 @ 125%

## Installation (for end users)
1. Install Windhawk and the Windows 11 Taskbar Styler mod (or another tool that reads these theme files).  
2. Copy `Themes/FrostedAcrylic/theme.txt` into the theme folder required by your tool, or import the theme through the tool’s UI.  
3. Optional (recommended for matching the screenshots): enable the "Taskbar Height & Icon Size" mod, or apply the settings shown below to match the sample visuals. The theme will still work without this pairing, but spacing and proportions may differ.

## Taskbar Height & Icon Size (recommended pairing)
Use these settings with your height/icon size mod to reproduce the example visuals exactly:
TaskbarHeight: 60 
IconSize: 40 
TaskbarButtonWidth: 48 
IconSizeSmall: 25 
TaskbarButtonWidthSmall: 30


You can save the above as `Themes/TaskbarHeightAndIconSize/settings.txt` (optional) or paste them into your height/icon size mod’s configuration.

## Compatibility & fallback behavior
- Primary blur: WindhawkBlur (preferred for smooth blur).  
- Fallback: AcrylicBrush (used when WindhawkBlur is unavailable).  
- If the host system does not support blur at all, the theme will degrade to semi‑transparent or solid fallback styles; visual fidelity will vary.

## Screenshots
Example images are included in Themes/FrostedAcrylic/assets/. In the repository README these are referenced with relative paths for preview:
![Preview](https://raw.githubusercontent.com/EvanYFWong/windows-11-taskbar-styling-guide/EvanYFWong-patch-1/Themes/FrostedAcrylic/assets/screenshot-1920x1080.png)

Customization tips
To change the bar’s maximum width, gutters, or button sizing, edit the constants in theme.txt (for example: TaskbarFrameWidth, SideMargin, TrayRightMargin, TaskbarButtonWidth).
If you want the theme to automatically adapt to screen width (e.g., a percentage of the screen), generate theme.txt with a small pre‑processing script that calculates values based on the current display resolution before applying the theme.
Contributing and feedback
Pull requests are welcome. If you encounter issues on a specific Windows/Explorer version or scaling value, please open an issue and include:

Windows build/version
display resolution and scaling (DPI%)
a screenshot of the taskbar showing the problem
Contributions that improve compatibility across scaling/DPI, add presets, or include additional screenshots are appreciated.

Maintainer notes
Recommended placement: Themes/FrostedAcrylic/ with theme.txt, README.md, and assets/ containing screenshots.
If you prefer a different filename or directory layout, tell me and I will update the branch.
Contact
GitHub: @EvanYFWong
