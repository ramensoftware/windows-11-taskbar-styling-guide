# Squircle theme for Windows 11 Taskbar Styler

**Author**: [AsvnDG](https://github.com/AsvnDG)

This theme was originally [shared on
Reddit](https://www.reddit.com/r/desktops/comments/1dna90y/comment/la4vxw1/).

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
  "controlStyles[0].styles[0]": "Fill:=Transparent",
  "controlStyles[1].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[1].styles[0]": "CornerRadius=5",
  "controlStyles[2].target": "Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[2].styles[0]": "CornerRadius=5",
  "controlStyles[3].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[3].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[3].styles[1]": "CornerRadius=5",
  "controlStyles[3].styles[2]": "Margin=0,5,14,5",
  "controlStyles[3].styles[3]": "Padding=10,0,0,0",
  "controlStyles[4].target": "TextBlock#TimeInnerTextBlock",
  "controlStyles[4].styles[0]": "Foreground=White",
  "controlStyles[5].target": "TextBlock#DateInnerTextBlock",
  "controlStyles[5].styles[0]": "Foreground=White",
  "controlStyles[6].target": "SystemTray.TextIconContent > Grid > SystemTray.AdaptiveTextBlock#Base > TextBlock",
  "controlStyles[6].styles[0]": "Foreground=White",
  "controlStyles[7].target": "Taskbar.TaskListLabeledButtonPanel > TextBlock#LabelControl",
  "controlStyles[7].styles[0]": "Margin=4,0,0,0",
  "controlStyles[7].styles[1]": "Foreground=White",
  "controlStyles[8].target": "Taskbar.SearchBoxButton",
  "controlStyles[8].styles[0]": "Margin=0,0,-12,0",
  "controlStyles[9].target": "TextBlock#SearchBoxTextBlock",
  "controlStyles[9].styles[0]": "Foreground=White",
  "controlStyles[10].target": "Rectangle#BackgroundStroke",
  "controlStyles[10].styles[0]": "Fill=Transparent",
  "controlStyles[11].target": "SystemTray.Stack#ShowDesktopStack",
  "controlStyles[11].styles[0]": "Visibility=Collapsed",
  "controlStyles[9].styles[1]": "FontSize=12",
  "controlStyles[1].styles[1]": "Background@InactivePointerOver:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[1].styles[2]": "Background@ActivePointerOver=Transparent",
  "controlStyles[1].styles[3]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.2\" />",
  "controlStyles[2].styles[1]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[1].styles[4]": "Background@ActivePressed:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[1].styles[5]": "Background@InactivePressed:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[1].styles[6]": "Background@ActiveNormal:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[2].styles[2]": "Background@InactivePointerOver:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[2].styles[3]": "Background@ActivePointerOver:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[2].styles[4]": "Background@ActiveNormal=:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[2].styles[5]": "Background@InactivePressed:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[2].styles[6]": "Background@ActivePressed:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[12].target": "Rectangle#RunningIndicator",
  "controlStyles[12].styles[0]": "Fill:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[12].styles[1]": "Width=40",
  "controlStyles[12].styles[2]": "Height=38",
  "controlStyles[12].styles[3]": "RadiusX=5",
  "controlStyles[12].styles[4]": "RadiusY=5",
  "controlStyles[13].target": "Taskbar.ExperienceToggleButton",
  "controlStyles[13].styles[0]": "Margin=0,0,-12,0",
  "controlStyles[14].target": "",
  "controlStyles[14].styles[0]": ""
}
```
</details>
