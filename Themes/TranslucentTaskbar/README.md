# TranslucentTaskbar theme for Windows 11 Taskbar Styler

**Author**: [Undisputed00x](https://github.com/Undisputed00x)

![Screenshot](screenshot.png)

## Theme selection

The theme is integrated into the mod, and can be simply selected from the mod's
settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Advanced" tab.
* Copy the content below to the text box under "Mod settings" and click "Save".

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=<AcrylicBrush TintColor=\"Transparent\" TintOpacity=\"0\" TintLuminosityOpacity=\"0\" Opacity=\"1\" FallbackColor=\"{ThemeResource SystemAccentColor}\"/>",
  "controlStyles[1].target": "Rectangle#BackgroundStroke",
  "controlStyles[1].styles[0]": "Visibility=Collapsed",
  "controlStyles[2].target": "MenuFlyoutPresenter",
  "controlStyles[2].styles[0]": "Background:=<AcrylicBrush TintColor=\"Transparent\" TintOpacity=\"0\" TintLuminosityOpacity=\"0\" Opacity=\"1\" FallbackColor=\"{ThemeResource SystemAccentColor}\"/>",
  "controlStyles[2].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[2].styles[2]": "CornerRadius=14",
  "controlStyles[2].styles[3]": "Padding=3,4,3,4",
  "controlStyles[3].target": "Border#OverflowFlyoutBackgroundBorder",
  "controlStyles[3].styles[0]": "Background:=<AcrylicBrush TintColor=\"Transparent\" TintOpacity=\"0\" TintLuminosityOpacity=\"0\" Opacity=\"1\" FallbackColor=\"{ThemeResource SystemAccentColor}\"/>",
  "controlStyles[3].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[3].styles[2]": "CornerRadius=15",
  "controlStyles[3].styles[3]": "Margin=-2,-2,-2,-2"
}
```
</details>
