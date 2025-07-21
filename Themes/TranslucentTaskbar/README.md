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
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill=$CommonBgBrush",
  "controlStyles[1].target": "Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill",
  "controlStyles[1].styles[0]": "Fill=$CommonBgBrush",
  "controlStyles[2].target": "Rectangle#BackgroundStroke",
  "controlStyles[2].styles[0]": "Visibility=Collapsed",
  "controlStyles[3].target": "MenuFlyoutPresenter > Border",
  "controlStyles[3].styles[0]": "Background=$CommonBgBrush",
  "controlStyles[3].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[3].styles[2]": "CornerRadius=14",
  "controlStyles[3].styles[3]": "Padding=3,4,3,4",
  "controlStyles[4].target": "Border#OverflowFlyoutBackgroundBorder",
  "controlStyles[4].styles[0]": "Background=$CommonBgBrush",
  "controlStyles[4].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[4].styles[2]": "CornerRadius=15",
  "controlStyles[4].styles[3]": "Margin=-2,-2,-2,-2",
  "controlStyles[5].target": "Grid#ConfirmatorMainGrid",
  "controlStyles[5].styles[0]": "Background=$CommonBgBrush",
  "controlStyles[6].target": "Grid#ConfirmatorMainGrid",
  "controlStyles[6].styles[0]": "BorderThickness=0",
  "controlStyles[7].target": "WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid",
  "controlStyles[7].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"25\" TintColor=\"#25323232\"/>",
  "controlStyles[7].styles[1]": "BorderThickness=0",
  "controlStyles[8].target": "WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid",
  "controlStyles[8].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "styleConstants[0]": "CommonBgBrush=<WindhawkBlur BlurAmount=\"18\" TintColor=\"#25323232\"/>"
}
```
</details>
