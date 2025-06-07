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
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#00000000\" Offset=\"0.3\" /><GradientStop Color=\"#AA000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[1].target": "Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill",
  "controlStyles[1].styles[0]": "Fill:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#ee000000\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[2].target": "Taskbar.TaskListLabeledButtonPanel > Rectangle#RunningIndicator",
  "controlStyles[2].styles[0]": "Fill=Transparent",
  "controlStyles[3].target": "Rectangle#BackgroundStroke",
  "controlStyles[3].styles[0]": "Visibility=Collapsed",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Border#BackgroundElement",
  "controlStyles[4].styles[0]": "CornerRadius=15",
  "controlStyles[4].styles[1]": "Background@InactiveRunningIndicator:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#3300290c\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[4].styles[2]": "Margin@ActiveRunningIndicator=-4",
  "controlStyles[4].styles[3]": "Margin=0,-1,0,-1",
  "controlStyles[4].styles[4]": "CornerRadius@ActiveRunningIndicator=2",
  "controlStyles[4].styles[5]": "CornerRadius@InactiveRunningIndicator=0",
  "controlStyles[4].styles[6]": "Margin@InactiveRunningIndicator=-4,-5,-4,-5",
  "controlStyles[4].styles[7]": "Margin@RequestingAttentionRunningIndicator=0,-4,0,-4",
  "controlStyles[4].styles[8]": "CornerRadius@RequestingAttentionRunningIndicator=2",
  "controlStyles[5].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > TextBlock#LabelControl",
  "controlStyles[5].styles[0]": "Foreground@ActiveNormal=Black",
  "controlStyles[5].styles[1]": "Foreground@ActivePointerOver=Black",
  "controlStyles[5].styles[2]": "Margin=0,0,3,0",
  "controlStyles[5].styles[3]": "Foreground@ActivePressed=#BFBFBF",
  "controlStyles[6].styles[1]": "Margin=0,0,0,2",
  "controlStyles[6].styles[2]": "CornerRadius=0",
  "controlStyles[6].target": "SystemTray.SystemTrayFrame > Grid",
  "controlStyles[6].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#50000000\" Offset=\"0.3\" /><GradientStop Color=\"#EE000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[7].target": "SystemTray.ChevronIconView",
  "controlStyles[7].styles[0]": "Padding=20",
  "controlStyles[8].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[8].styles[0]": "Padding=2",
  "controlStyles[9].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel",
  "controlStyles[9].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#80000000\" Offset=\"0.0\" /><GradientStop Color=\"#FF000000\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[9].styles[1]": "Padding=0",
  "controlStyles[9].styles[2]": "CornerRadius=0",
  "controlStyles[9].styles[3]": "Margin=0",
  "controlStyles[10].target": "Grid",
  "controlStyles[10].styles[0]": "RequestedTheme=2",
  "controlStyles[11].target": "Grid#OverflowRootGrid > Border",
  "controlStyles[11].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#ee000000\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[12].target": "Taskbar.AugmentedEntryPointButton",
  "controlStyles[12].styles[0]": "Margin=12,0,0,0",
  "controlStyles[13].styles[0]": "BorderThickness=0",
  "controlStyles[13].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates",
  "controlStyles[13].styles[1]": "Background@ActiveNormal:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight3}\"/>",
  "controlStyles[13].styles[2]": "Background@ActivePointerOver:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight2}\"/>",
  "controlStyles[13].styles[3]": "Background@InactivePointerOver=#EBEBEB",
  "controlStyles[13].styles[4]": "Background@InactivePressed=#BBBBBB",
  "controlStyles[13].styles[5]": "Background@ActivePressed:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\"/>",
  "controlStyles[13].styles[6]": "Background@RequestingAttention=#FFE9AFAA",
  "controlStyles[13].styles[7]": "Background@RequestingAttentionPointerOver=#FFF8E7E5",
  "controlStyles[13].styles[8]": "Background@RequestingAttentionPressed=#FFFEEEF0",
  "controlStyles[14].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Border",
  "controlStyles[14].styles[0]": "BorderThickness=0",
  "controlStyles[14].styles[1]": "Margin=-2,-4,-2,-4",
  "controlStyles[14].styles[2]": "CornerRadius=0"
}
```
</details>

### Light Bar
<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#00000000\" Offset=\"0.3\" /><GradientStop Color=\"#AA000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[1].target": "Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill",
  "controlStyles[1].styles[0]": "Fill:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#ee000000\" Offset=\"0.1\" /><GradientStop Color=\"#EBEBEB\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[2].target": "Taskbar.TaskListLabeledButtonPanel > Rectangle#RunningIndicator",
  "controlStyles[2].styles[0]": "Fill=Transparent",
  "controlStyles[3].target": "Rectangle#BackgroundStroke",
  "controlStyles[3].styles[0]": "Visibility=Collapsed",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Border#BackgroundElement",
  "controlStyles[4].styles[0]": "CornerRadius=15",
  "controlStyles[4].styles[1]": "Background@InactiveRunningIndicator:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#3300290c\" Offset=\"0.1\" /><GradientStop Color=\"{ThemeResource SystemAccentColorDark2}\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[4].styles[2]": "Margin@ActiveRunningIndicator=-4",
  "controlStyles[4].styles[3]": "Margin=0,-1,0,-1",
  "controlStyles[4].styles[4]": "CornerRadius@ActiveRunningIndicator=2",
  "controlStyles[4].styles[5]": "CornerRadius@InactiveRunningIndicator=0",
  "controlStyles[4].styles[6]": "Margin@InactiveRunningIndicator=-4",
  "controlStyles[4].styles[7]": "Margin@RequestingAttentionRunningIndicator=0,-4,0,-4",
  "controlStyles[4].styles[8]": "CornerRadius@RequestingAttentionRunningIndicator=2",
  "controlStyles[5].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > TextBlock#LabelControl",
  "controlStyles[5].styles[0]": "Foreground@ActiveNormal=Black",
  "controlStyles[5].styles[1]": "Foreground@ActivePointerOver=Black",
  "controlStyles[5].styles[2]": "Margin=0,0,3,0",
  "controlStyles[5].styles[3]": "Foreground@ActivePressed=#424242",
  "controlStyles[6].styles[1]": "Margin=0,0,0,2",
  "controlStyles[6].styles[2]": "CornerRadius=0",
  "controlStyles[6].target": "SystemTray.SystemTrayFrame > Grid",
  "controlStyles[6].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#50000000\" Offset=\"0.3\" /><GradientStop Color=\"#EE000000\" Offset=\"0.9\" /></LinearGradientBrush>",
  "controlStyles[7].target": "SystemTray.ChevronIconView",
  "controlStyles[7].styles[0]": "Padding=20",
  "controlStyles[8].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[8].styles[0]": "Padding=2",
  "controlStyles[9].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel",
  "controlStyles[9].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"0,1\"><GradientStop Color=\"#80000000\" Offset=\"0.0\" /><GradientStop Color=\"#FF000000\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[9].styles[1]": "Padding=0",
  "controlStyles[9].styles[2]": "CornerRadius=0",
  "controlStyles[9].styles[3]": "Margin=0",
  "controlStyles[10].target": "Grid",
  "controlStyles[10].styles[0]": "RequestedTheme=2",
  "controlStyles[11].target": "Grid#OverflowRootGrid > Border",
  "controlStyles[11].styles[0]": "Background:=<LinearGradientBrush StartPoint=\"0,0.5\" EndPoint=\"0,1\"><GradientStop Color=\"#ee000000\" Offset=\"0.1\" /><GradientStop Color=\"#EBEBEB\" Offset=\"0.9\" /><GradientStop Color=\"#AAFFFFFF\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[12].target": "Taskbar.AugmentedEntryPointButton",
  "controlStyles[12].styles[0]": "Margin=12,0,0,0",
  "controlStyles[13].styles[0]": "BorderThickness=0",
  "controlStyles[13].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates",
  "controlStyles[13].styles[1]": "Background@ActiveNormal:=#FCFCFC",
  "controlStyles[13].styles[2]": "Background@ActivePointerOver:=#BBBBBB",
  "controlStyles[13].styles[3]": "Background@InactivePointerOver=#EBEBEB",
  "controlStyles[13].styles[4]": "Background@InactivePressed=#BBBBBB",
  "controlStyles[13].styles[5]": "Background@ActivePressed=#BBBBBB",
  "controlStyles[13].styles[6]": "Background@RequestingAttention=#FFE9AFAA",
  "controlStyles[13].styles[7]": "Background@RequestingAttentionPointerOver=#FFF8E7E5",
  "controlStyles[13].styles[8]": "Background@RequestingAttentionPressed=#FFFEEEF0",
  "controlStyles[14].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Border",
  "controlStyles[14].styles[0]": "BorderThickness=0",
  "controlStyles[14].styles[1]": "Margin=-2,-4,-2,-4",
  "controlStyles[14].styles[2]": "CornerRadius=0"
}
```
</details>
