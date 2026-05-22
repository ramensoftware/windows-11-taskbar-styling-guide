# TranslucentTaskbar theme for Windows 11 Taskbar Styler

**Author**: [Undisputed00x](https://github.com/Undisputed00x)

![Screenshot](screenshot.png)

## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - CommonBgBrush=<WindhawkBlur BlurAmount="18" TintColor="#25323232"/>
controlStyles:
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=$CommonBgBrush
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=$CommonBgBrush
  - target: Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: MenuFlyoutPresenter > Border
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=14
      - Padding=3,4,3,4
  - target: Border#OverflowFlyoutBackgroundBorder
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=15
      - Margin=-2,-2,-2,-2
  - target: Grid#ConfirmatorMainGrid
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid
    styles:
      - Background:=<WindhawkBlur BlurAmount="25" TintColor="#25323232"/>
      - BorderThickness=0
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
```
</details>
