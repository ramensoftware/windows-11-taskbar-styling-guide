# CleanSlate theme for Windows 11 Taskbar Styler

**Author**: [Xerios](https://github.com/Xerios)

![Screenshot of taskbar](screenshot.png) \
![Screenshot of taskbar](screenshot-light.png)

## Notes

A nice clean theme that works nicely with dynamic windows themes using accent colors, mostly tuned for dark.

### Suggested Windows settings

- Set taskbar alignment to left
- Use full-width settings for Taskbar Labels for Windows 11 (see config below)
- Hide the widgets button

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
* Do the same for "Taskbar Labels for Windows 11".

<details>
<summary>Content to import (click to expand)</summary>

## Theme

```json
{
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[1].target": "Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[1].styles[0]": "CornerRadius=100",
  "controlStyles[1].styles[1]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[1].styles[2]": "Background@InactivePointerOver:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\"/>",
  "controlStyles[1].styles[3]": "Background@ActivePointerOver:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[1].styles[4]": "Background@ActiveNormal:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\"/>",
  "controlStyles[1].styles[5]": "Background@InactivePressed:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[1].styles[6]": "Background@ActivePressed:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[2].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[2].styles[0]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.5\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[2].styles[1]": "CornerRadius=5",
  "controlStyles[2].styles[2]": "Margin=0,5,5,5",
  "controlStyles[2].styles[3]": "Padding=1,0,-10,0",
  "controlStyles[3].target": "Rectangle#RunningIndicator",
  "controlStyles[3].styles[0]": "Fill=Transparent",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel > TextBlock#LabelControl",
  "controlStyles[4].styles[0]": "Margin=8,0,0,0",
  "controlStyles[4].styles[1]": "Foreground=White",
  "controlStyles[5].target": "Taskbar.SearchBoxButton ",
  "controlStyles[5].styles[0]": "Padding=8",
  "controlStyles[5].styles[1]": "Margin=4,0,4,0",
  "controlStyles[6].target": "TextBlock#SearchBoxTextBlock",
  "controlStyles[6].styles[0]": "FontSize=12",
  "controlStyles[7].target": "Rectangle#BackgroundStroke",
  "controlStyles[7].styles[0]": "Fill=Transparent",
  "controlStyles[8].target": "SystemTray.AdaptiveTextBlock",
  "controlStyles[8].styles[0]": "Foreground=White",
  "controlStyles[9].target": "Taskbar.TaskListButton#TaskListButton[AutomationProperties.Name=Copilot] > Taskbar.TaskListLabeledButtonPanel#IconPanel > Border#BackgroundElement",
  "controlStyles[9].styles[0]": "Background:=<AcrylicBrush TintColor=\"Black\" TintOpacity=\"0.8\" />",
  "controlStyles[10].target": "SystemTray.NotifyIconView > Grid > Border#BackgroundBorder",
  "controlStyles[10].styles[0]": "Margin=0,3,0,3",
  "controlStyles[11].target": "Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement@CommonStates",
  "controlStyles[11].styles[0]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[11].styles[1]": "CornerRadius=20",
  "controlStyles[11].styles[2]": "Margin=0,1,0,1",
  "controlStyles[12].target": "TextBlock#TimeInnerTextBlock",
  "controlStyles[12].styles[0]": "Foreground=White",
  "controlStyles[13].target": "TextBlock#DateInnerTextBlock",
  "controlStyles[13].styles[0]": "Foreground=White",
  "controlStyles[14].target": "SystemTray.TextIconContent > Grid > SystemTray.AdaptiveTextBlock#Base > TextBlock",
  "controlStyles[14].styles[0]": "Foreground=White",
  "controlStyles[15].target": "Border#BackgroundElement",
  "controlStyles[15].styles[0]": "BorderThickness=0",
  "controlStyles[16].styles[0]": "Background@InactiveRunningIndicator:=<SolidColorBrush Color=\"Black\" Opacity=\"0.4\" />",
  "controlStyles[16].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Border#BackgroundElement",
  "controlStyles[16].styles[1]": "Background@InactiveRunningIndicator:=<SolidColorBrush Color=\"Black\" Opacity=\"0.4\" />",
  "controlStyles[16].styles[2]": "Background@ActiveRunningIndicator:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorDark2}\" Opacity=\"0.4\" />",
  "controlStyles[16].styles[3]": "Background@RequestingAttentionRunningIndicator:=<SolidColorBrush Color=\"#ffdf5e\" Opacity=\"0.4\" />",
  "controlStyles[17].target": "Rectangle#ShowDesktopPipe",
  "controlStyles[17].styles[0]": "Width=12",
  "controlStyles[17].styles[1]": "Height=38",
  "controlStyles[17].styles[2]": "Margin=-6,0,0,0",
  "controlStyles[18].target": "SystemTray.Stack#ShowDesktopStack",
  "controlStyles[18].styles[0]": "Width=12",
  "controlStyles[19].target": "Taskbar.TaskListButtonPanel",
  "controlStyles[19].styles[0]": "Margin=-3,0,0,0",
  "controlStyles[20].target": "Grid#OverflowRootGrid > Border",
  "controlStyles[20].styles[0]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[20].styles[1]": "BorderBrush:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColor}\" />",
  "controlStyles[21].target": "Taskbar.TaskItemThumbnailView > Grid > Border",
  "controlStyles[21].styles[0]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark3}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[21].styles[1]": "BorderBrush:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColor}\" />",
  "controlStyles[21].styles[2]": "BorderThickness=1",
  "controlStyles[21].styles[3]": "CornerRadius=5",
  "controlStyles[22].target": "Border#ProgressBarRoot > Border > Grid > Rectangle",
  "controlStyles[22].styles[0]": "Fill:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\" />",
  "controlStyles[23].target": "Border#ProgressBarRoot > Border > Grid > Rectangle#ProgressBarTrack",
  "controlStyles[23].styles[0]": "Fill:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorDark3} />",
  "controlStyles[24].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[24].styles[0]": "BorderBrush@InactivePointerOver:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\"  />",
  "controlStyles[24].styles[1]": "BorderBrush@ActiveNormal:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight2}\" />",
  "controlStyles[24].styles[2]": "BorderBrush@ActivePointerOver:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\"  />",
  "controlStyles[24].styles[6]": "BorderThickness@MultiWindowActive=2",
  "controlStyles[24].styles[7]": "BorderThickness@MultiWindowNormal=2",
  "controlStyles[24].styles[3]": "BorderBrush@MultiWindowPointerOver:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\"  />",
  "controlStyles[24].styles[4]": "BorderThickness@ActiveNormal=1",
  "controlStyles[24].styles[5]": "BorderThickness@ActivePointerOver=1",
  "controlStyles[24].styles[8]": "BorderThickness@MultiWindowPointerOver=2.5",
  "controlStyles[24].styles[9]": "BorderBrush@MultiWindowActive:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\"  />",
  "controlStyles[24].styles[10]": "BorderBrush@MultiWindowNormal:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\"  />",
  "controlStyles[24].styles[11]": "Margin@MultiWindowNormal=0",
  "controlStyles[24].styles[12]": "Margin@MultiWindowPointerOver=0",
  "controlStyles[24].styles[13]": "Margin@MultiWindowPressed=0",
  "controlStyles[25].target": "ToolTip",
  "controlStyles[25].styles[0]": "Background:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorDark2}\"  />",
  "controlStyles[25].styles[1]": "Foreground=White",
  "controlStyles[26].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#MultiWindowElement",
  "controlStyles[26].styles[0]": "Background=Transparent",
  "controlStyles[26].styles[1]": "BorderThickness=0",
  "controlStyles[27].target": "Taskbar.SearchBoxButton > Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[27].styles[0]": "CornerRadius=5",
  "controlStyles[27].styles[1]": "CornerRadius@InactiveNormal_SearchIcon=100",
  "controlStyles[27].styles[2]": "CornerRadius@InactivePointerOver_SearchIcon=100",
  "controlStyles[27].styles[3]": "CornerRadius@InactivePressed_SearchIcon=100",
  "controlStyles[27].styles[4]": "CornerRadius@ActiveNormal_SearchIcon=100",
  "controlStyles[27].styles[5]": "CornerRadius@ActivePointerOver_SearchIcon=100",
  "controlStyles[27].styles[6]": "CornerRadius@ActivePressed_SearchIcon=100",
  "controlStyles[27].styles[7]": "Background@InactiveNormal_SearchIcon:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[27].styles[8]": "Background@InactivePointerOver_SearchIcon:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[27].styles[9]": "Background@InactivePressed_SearchIcon:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[27].styles[10]": "Background@ActiveNormal_SearchIcon:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[27].styles[11]": "Background@ActivePointerOver_SearchIcon:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[27].styles[12]": "Background@ActivePressed_SearchIcon:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[28].target": "Taskbar.OverflowToggleButton",
  "controlStyles[28].styles[0]": "Margin=8,0,8,0",
  "controlStyles[28].styles[1]": "Background:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorDark2}\"  />",
  "controlStyles[29].target": "Rectangle#RightOverflowButtonDivider",
  "controlStyles[29].styles[0]": "Fill:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight2}\"  />",
  "controlStyles[29].styles[1]": "Margin=8,4,-8,4",
  "controlStyles[30].target": "Taskbar.OverflowToggleButton > Taskbar.TaskListButtonPanel@CommonStates > Border",
  "controlStyles[30].styles[0]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark2}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
  "controlStyles[30].styles[1]": "Background@InactivePointerOver:=<AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.4\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[31].target": "Taskbar.TaskListLabeledButtonPanel",
  "controlStyles[31].styles[0]": "Margin=0"
}
```

## Taskbar Labels for Windows 11

```json
{
  "taskbarItemWidth": 170,
  "minimumTaskbarItemWidth": 0,
  "maximumTaskbarItemWidth": 200,
  "runningIndicatorStyle": "fullWidth",
  "progressIndicatorStyle": "sameAsRunningIndicatorStyle",
  "fontSize": 12,
  "leftAndRightPaddingSize": 12,
  "spaceBetweenIconAndLabel": 8,
  "labelForSingleItem": "%name%",
  "labelForMultipleItems": "[%amount%] %name%"
}
```
</details>
