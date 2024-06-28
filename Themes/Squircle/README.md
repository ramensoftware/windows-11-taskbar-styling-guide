# Squircle theme for Windows 11 Taskbar Styler

This theme was originally [shared on reddit](https://www.reddit.com/r/desktops/comments/1dna90y/comment/la4vxw1/).

![Screenshot](screenshot.png)

## Theme selection

The theme is integrated into the mod, and can be simply selected from the mod's
settings:

* Open the Windows 11 Start Menu Styler mod in Windhawk.
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
  "theme": "",
  "controlStyles[0].target": "Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill=Transparent",
  "controlStyles[1].target": "Taskbar.TaskListLabeledButtonPanel > Border#BackgroundElement@RunningIndicatorStates",
  "controlStyles[1].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.6\" />",
  "controlStyles[1].styles[1]": "CornerRadius=5",
  "controlStyles[1].styles[2]": "Background@NoRunningIndicator:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.15\" />",
  "controlStyles[2].target": "Taskbar.TaskListButtonPanel > Border#BackgroundElement@CommonStates",
  "controlStyles[2].styles[0]": "CornerRadius=5",
  "controlStyles[2].styles[1]": "Background@ActivePointerOver=#B4202020",
  "controlStyles[2].styles[2]": "Background@InactivePointerOver=#B4202020",
  "controlStyles[2].styles[3]": "Background@ActivePressed=#B4101010",
  "controlStyles[2].styles[4]": "Background@InactivePressed=#B4101010",
  "controlStyles[2].styles[5]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.6\" />",
  "controlStyles[3].target": "Grid#SystemTrayFrameGrid[1]",
  "controlStyles[3].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.6\" />",
  "controlStyles[3].styles[1]": "CornerRadius=5",
  "controlStyles[3].styles[2]": "Margin=0,5,14,5",
  "controlStyles[3].styles[3]": "Padding=10,0,0,0",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Rectangle#RunningIndicator",
  "controlStyles[4].styles[0]": "Width=Auto",
  "controlStyles[4].styles[1]": "Height=39",
  "controlStyles[4].styles[2]": "Stroke@InactivePointerOver=#75A8E6",
  "controlStyles[4].styles[3]": "Stroke@InactivePressed=#7CB1F2",
  "controlStyles[4].styles[4]": "Stroke@ActiveNormal=#5F87B9",
  "controlStyles[4].styles[5]": "Stroke@ActivePointerOver=#75A8E6",
  "controlStyles[4].styles[6]": "Stroke@ActivePressed=#7CB1F2",
  "controlStyles[4].styles[7]": "Fill=Transparent",
  "controlStyles[4].styles[8]": "RadiusX=5",
  "controlStyles[4].styles[9]": "RadiusY=5",
  "controlStyles[4].styles[10]": "StrokeThickness=3",
  "controlStyles[5].target": "Taskbar.TaskListLabeledButtonPanel > TextBlock#LabelControl",
  "controlStyles[5].styles[0]": "Margin=4,0,0,0",
  "controlStyles[6].target": "Taskbar.SearchBoxButton",
  "controlStyles[6].styles[0]": "Margin=0,-4,0,-4",
  "controlStyles[7].target": "TextBlock#SearchBoxTextBlock",
  "controlStyles[8].target": "Rectangle#BackgroundStroke",
  "controlStyles[8].styles[0]": "Visibility=Collapsed",
  "controlStyles[9].target": "SystemTray.Stack#ShowDesktopStack",
  "controlStyles[7].styles[0]": "FontSize=12.5",
  "controlStyles[9].styles[0]": "//Visibility=Collapsed",
  "controlStyles[10].target": "Grid",
  "controlStyles[10].styles[0]": "RequestedTheme=2",
  "controlStyles[11].target": "Windows.UI.Xaml.Controls.Grid#DynamicSearchBoxGleamContainer",
  "controlStyles[11].styles[0]": "Margin=6",
  "controlStyles[12].target": "Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement",
  "controlStyles[12].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.4\" />",
  "controlStyles[13].target": "Taskbar.TaskListButton#TaskListButton[AutomationProperties.Name=Copilot] > Taskbar.TaskListLabeledButtonPanel#IconPanel > Border#BackgroundElement",
  "controlStyles[13].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.6\" />",
  "controlStyles[14].target": "Border#BackgroundBorder",
  "controlStyles[14].styles[0]": "Margin=0,3,0,3",
  "controlStyles[14].styles[1]": "CornerRadius=5",
  "controlStyles[15].target": "//Windows.UI.Xaml.Shapes.Rectangle#ShowDesktopPipe",
  "controlStyles[15].styles[0]": "Height=40",
  "controlStyles[15].styles[1]": "Width=8",
  "controlStyles[15].styles[2]": "Fill:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.5\" />",
  "controlStyles[15].styles[3]": "Margin=2,0,0,0",
  "controlStyles[16].target": "Taskbar.TaskListButton#TaskListButton > Taskbar.TaskListLabeledButtonPanel#IconPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[16].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.6\" />",
  "controlStyles[16].styles[1]": "Background@InactivePointerOver:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.7\" />",
  "controlStyles[16].styles[2]": "Background@ActivePointerOver:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.7\" />",
  "controlStyles[17].target": "Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton",
  "controlStyles[17].styles[0]": "Margin=0,0,-6,-0.5",
  "controlStyles[18].target": "Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement@CommonStates",
  "controlStyles[18].styles[0]": "Background@InactivePointerOver:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0\" />",
  "controlStyles[18].styles[1]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.4\" />",
  "controlStyles[19].target": "Border#MultiWindowElement",
  "controlStyles[19].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.6\" />"
}
```
</details>
