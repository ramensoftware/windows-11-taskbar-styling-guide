# SimplyTransparent theme for Windows 11 Taskbar Styler

**Author**: [Osprey00](https://github.com/Osprey00)

Makes the taskbar background transparent. For users who want that and no other customizations.

![Screenshot](screenshot.png)

## Theme selection

The theme is integrated into the mod and can simply be selected from the mod's
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
  "controlStyles[0].target":"Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]":"Fill=Transparent",
  "controlStyles[1].target":"Rectangle#BackgroundStroke",
  "controlStyles[1].styles[0]":"Fill=Transparent",
  "controlStyles[2].target":"Border#OverflowFlyoutBackgroundBorder",
  "controlStyles[2].styles[0]":"Background=Transparent"
}
```
</details>
