# Lucent theme for Windows 11 Taskbar Styler

A dark theme with gradients and colorful glows that use your theme color.

**Author**: [twistthoseknobs](https://github.com/twistthoseknobs)

![Screenshot](screenshot.png) \
![Screenshot](screenshot_red.png)

Alternate Light Bar Style: \
![Screenshot](screenshot_light.png)

## Suggested Windows settings

* Left-aligned taskbar.
* Combine taskbar buttons set to "When taskbar is full".
* Dark wallpaper with matching accent color.

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

### Accented Bar
<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#00000000\" Offset=\"0.3\" /><GradientStop Color=\"#AA000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[1].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Rectangle#RunningIndicator",
  "controlStyles[1].styles[0]": "Fill=Transparent",
  "controlStyles[2].target": "Rectangle#BackgroundStroke",
  "controlStyles[2].styles[0]": "Visibility=Collapsed",
  "controlStyles[3].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Border#BackgroundElement",
  "controlStyles[3].styles[0]": "CornerRadius=15",
  "controlStyles[3].styles[1]": "Background@ActiveRunningIndicator:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight3}\"/>",
  "controlStyles[3].styles[2]": "Background@InactiveRunningIndicator:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#3300290c\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[3].styles[3]": "Margin@ActiveRunningIndicator=-4",
  "controlStyles[3].styles[4]": "Margin=0,-1,0,-1",
  "controlStyles[3].styles[5]": "CornerRadius@ActiveRunningIndicator=2",
  "controlStyles[3].styles[6]": "CornerRadius@InactiveRunningIndicator=0",
  "controlStyles[3].styles[7]": "Margin@InactiveRunningIndicator=-4",
  "controlStyles[3].styles[8]": "Margin@RequestingAttentionRunningIndicator=0,-4,0,-4",
  "controlStyles[3].styles[9]": "CornerRadius@RequestingAttentionRunningIndicator=2",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > TextBlock#LabelControl",
  "controlStyles[4].styles[0]": "Foreground@ActiveNormal=Black",
  "controlStyles[4].styles[1]": "Foreground@ActivePointerOver=Black",
  "controlStyles[4].styles[3]": "Margin=0,0,3,0",
  "controlStyles[5].styles[1]": "Margin=0,0,0,2",
  "controlStyles[5].styles[2]": "CornerRadius=0",
  "controlStyles[5].target": "SystemTray.SystemTrayFrame > Grid",
  "controlStyles[5].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#95000000\" Offset=\"0.3\" /><GradientStop Color=\"#EE000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[6].target": "SystemTray.ChevronIconView",
  "controlStyles[6].styles[0]": "Padding=20",
  "controlStyles[7].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[7].styles[0]": "Padding=2",
  "controlStyles[8].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel",
  "controlStyles[8].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#80000000\" Offset=\"0.0\" /><GradientStop Color=\"#FF000000\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[8].styles[1]": "Padding=0",
  "controlStyles[8].styles[2]": "CornerRadius=0",
  "controlStyles[8].styles[3]": "Margin=0",
  "controlStyles[9].target": "Grid",
  "controlStyles[9].styles[0]": "RequestedTheme=2",
  "controlStyles[10].target": "Grid#OverflowRootGrid > Border",
  "controlStyles[10].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#3300290c\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>"
}
```
</details>

### Light Bar
<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#00000000\" Offset=\"0.3\" /><GradientStop Color=\"#AA000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[1].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Rectangle#RunningIndicator",
  "controlStyles[1].styles[0]": "Fill=Transparent",
  "controlStyles[2].target": "Rectangle#BackgroundStroke",
  "controlStyles[2].styles[0]": "Visibility=Collapsed",
  "controlStyles[3].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Border#BackgroundElement",
  "controlStyles[3].styles[0]": "CornerRadius=15",
  "controlStyles[3].styles[1]": "Background@ActiveRunningIndicator:=#FCFCFC",
  "controlStyles[3].styles[2]": "Background@InactiveRunningIndicator:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#3300290c\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[3].styles[3]": "Margin@ActiveRunningIndicator=-4",
  "controlStyles[3].styles[4]": "Margin=0,-1,0,-1",
  "controlStyles[3].styles[5]": "CornerRadius@ActiveRunningIndicator=2",
  "controlStyles[3].styles[6]": "CornerRadius@InactiveRunningIndicator=0",
  "controlStyles[3].styles[7]": "Margin@InactiveRunningIndicator=-4",
  "controlStyles[3].styles[8]": "Margin@RequestingAttentionRunningIndicator=0,-4,0,-4",
  "controlStyles[3].styles[9]": "CornerRadius@RequestingAttentionRunningIndicator=2",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > TextBlock#LabelControl",
  "controlStyles[4].styles[0]": "Foreground@ActiveNormal=Black",
  "controlStyles[4].styles[1]": "Foreground@ActivePointerOver=Black",
  "controlStyles[4].styles[3]": "Margin=0,0,3,0",
  "controlStyles[5].styles[1]": "Margin=0,0,0,2",
  "controlStyles[5].styles[2]": "CornerRadius=0",
  "controlStyles[5].target": "SystemTray.SystemTrayFrame > Grid",
  "controlStyles[5].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#95000000\" Offset=\"0.3\" /><GradientStop Color=\"#EE000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[6].target": "SystemTray.ChevronIconView",
  "controlStyles[6].styles[0]": "Padding=20",
  "controlStyles[7].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[7].styles[0]": "Padding=2",
  "controlStyles[8].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel",
  "controlStyles[8].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#80000000\" Offset=\"0.0\" /><GradientStop Color=\"#FF000000\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[8].styles[1]": "Padding=0",
  "controlStyles[8].styles[2]": "CornerRadius=0",
  "controlStyles[8].styles[3]": "Margin=0",
  "controlStyles[9].target": "Grid",
  "controlStyles[9].styles[0]": "RequestedTheme=2",
  "controlStyles[10].target": "Grid#OverflowRootGrid > Border",
  "controlStyles[10].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#3300290c\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>"
}
```
</details>
