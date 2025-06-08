# Bubbles theme for Windows 11 Taskbar Styler

This theme was created as a showcase in response to [this question on
Reddit](https://www.reddit.com/r/windows/comments/1c7522o/anyone_know_if_this_taskbar_is_possible_to_get_on/).

**Author**: [m417z](https://github.com/m417z)

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
  "controlStyles[0].styles[0]": "Fill:=<SolidColorBrush x:Name=\"SystemChromeLow\" Color=\"{ThemeResource SystemChromeLowColor}\" />",
  "controlStyles[1].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Border#BackgroundElement",
  "controlStyles[1].styles[0]": "CornerRadius=20",
  "controlStyles[1].styles[1]": "Background@NoRunningIndicator=#40303030",
  "controlStyles[1].styles[2]": "Background:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.5\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[2].target": "Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[2].styles[0]": "Background:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.5\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[2].styles[1]": "CornerRadius=20",
  "controlStyles[2].styles[2]": "Background@ActivePointerOver:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.8\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[2].styles[6]": "BorderThickness@InactivePressed=3",
  "controlStyles[2].styles[7]": "BorderBrush@InactivePressed:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.8\" Color=\"{ThemeResource SystemAccentColor}\" />",
  "controlStyles[2].styles[3]": "Background@InactivePointerOver:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.8\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[2].styles[4]": "Background@ActivePressed:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"1\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[2].styles[5]": "Background@InactivePressed:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"1\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[3].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[3].styles[0]": "Background:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.5\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[3].styles[1]": "CornerRadius=20",
  "controlStyles[3].styles[2]": "Margin=0,5,4,5",
  "controlStyles[3].styles[3]": "Padding=10,0,0,0",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Rectangle#RunningIndicator",
  "controlStyles[4].styles[0]": "Width=40",
  "controlStyles[4].styles[1]": "Height=40",
  "controlStyles[4].styles[2]": "Stroke@InactivePointerOver=#75A8E6",
  "controlStyles[4].styles[3]": "Stroke@InactivePressed=#7CB1F2",
  "controlStyles[4].styles[4]": "Stroke@ActiveNormal=#5F87B9",
  "controlStyles[4].styles[5]": "Stroke@ActivePointerOver=#75A8E6",
  "controlStyles[4].styles[6]": "Stroke@ActivePressed=#7CB1F2",
  "controlStyles[4].styles[7]": "Fill=Transparent",
  "controlStyles[4].styles[8]": "RadiusX=20",
  "controlStyles[4].styles[9]": "RadiusY=20",
  "controlStyles[4].styles[10]": "StrokeThickness=3",
  "controlStyles[4].styles[11]": "Stroke@MultiWindowPointerOver=#CCCCDD",
  "controlStyles[4].styles[12]": "Stroke@MultiWindowPressed=White",
  "controlStyles[4].styles[13]": "Stroke@MultiWindowActive=#BBBBCC",
  "controlStyles[4].styles[14]": "Fill@MultiWindowNormal=#88AAAABB",
  "controlStyles[4].styles[15]": "Fill@MultiWindowPointerOver=#88AAAABB",
  "controlStyles[4].styles[16]": "Fill@MultiWindowActive=#88AAAABB",
  "controlStyles[4].styles[17]": "Fill@MultiWindowPressed=#88AAAABB",
  "controlStyles[4].styles[18]": "VerticalAlignment=2",
  "controlStyles[4].styles[19]": "Margin=0",
  "controlStyles[4].styles[20]": "Stroke@RequestingAttention=Crimson",
  "controlStyles[4].styles[21]": "Stroke@RequestingAttentionPointerOver=Red",
  "controlStyles[4].styles[22]": "Fill@RequestingAttention=DarkOrange",
  "controlStyles[4].styles[23]": "Fill@RequestingAttentionPointerOver=Orange",
  "controlStyles[4].styles[24]": "StrokeThickness@RequestingAttention=2",
  "controlStyles[4].styles[25]": "StrokeThickness@RequestingAttentionPointerOver=2",
  "controlStyles[5].target": "Taskbar.TaskListLabeledButtonPanel > TextBlock#LabelControl",
  "controlStyles[5].styles[0]": "Margin=4,0,0,0",
  "controlStyles[5].styles[1]": "Foreground=White",
  "controlStyles[6].target": "Taskbar.SearchBoxButton",
  "controlStyles[6].styles[0]": "Height=48",
  "controlStyles[6].styles[1]": "Margin=0,-2,0,0",
  "controlStyles[7].target": "Border#MultiWindowElement",
  "controlStyles[7].styles[0]": "Height=0",
  "controlStyles[8].target": "Grid#OverflowRootGrid > Border",
  "controlStyles[8].styles[0]": "Background=#EE080810",
  "controlStyles[8].styles[1]": "BorderBrush=#303030",
  "controlStyles[8].styles[2]": "BorderThickness=2.5",
  "controlStyles[9].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel > Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer#Icon",
  "controlStyles[9].styles[0]": "Margin=1,0,0,0",
  "controlStyles[10].target": "SystemTray.Stack#ShowDesktopStack",
  "controlStyles[10].styles[0]": "Padding=5,0,5,0",
  "controlStyles[10].styles[1]": "Margin=2,0,10,0",
  "controlStyles[11].target": "Windows.UI.Xaml.Shapes.Rectangle#ShowDesktopPipe",
  "controlStyles[11].styles[0]": "MinWidth=4",
  "controlStyles[11].styles[1]": "RadiusX=2",
  "controlStyles[11].styles[2]": "RadiusY=2",
  "controlStyles[12].target": "SystemTray.Stack#NotifyIconStack > Windows.UI.Xaml.Controls.Grid > SystemTray.StackListView > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.ContentPresenter > SystemTray.ChevronIconView > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[12].styles[0]": "CornerRadius=16,5,5,16",
  "controlStyles[12].styles[1]": "Margin=-3,4,0,4",
  "controlStyles[13].target": "TextBlock#InnerTextBlock",
  "controlStyles[13].styles[0]": "Foreground:=<SolidColorBrush x:Name=\"SearchBoxTextBlock\" Color=\"{ThemeResource SearchPillButtonForeground}\" />",
  "controlStyles[14].target": "TextBlock#LabelControl",
  "controlStyles[14].styles[0]": "Foreground:=<SolidColorBrush x:Name=\"SearchBoxTextBlock\" Color=\"{ThemeResource SearchPillButtonForeground}\" />",
  "controlStyles[15].target": "TextBlock#TimeInnerTextBlock",
  "controlStyles[15].styles[0]": "Foreground:=<SolidColorBrush x:Name=\"SearchBoxTextBlock\" Color=\"{ThemeResource SearchPillButtonForeground}\" />",
  "controlStyles[15].styles[1]": "Margin=3,2,0,0",
  "controlStyles[16].target": "TextBlock#DateInnerTextBlock",
  "controlStyles[16].styles[0]": "Foreground:=<SolidColorBrush x:Name=\"SearchBoxTextBlock\" Color=\"{ThemeResource SearchPillButtonForeground}\" />",
  "controlStyles[16].styles[1]": "Margin=0,0,2,2",
  "controlStyles[17].target": "Grid#ContainerGrid@ > Border#BackgroundBorder",
  "controlStyles[17].styles[0]": "Background@PointerOver:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.5\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[17].styles[1]": "CornerRadius=20",
  "controlStyles[17].styles[2]": "Width=24",
  "controlStyles[17].styles[3]": "Height=24",
  "controlStyles[17].styles[4]": "Margin=2",
  "controlStyles[18].target": "SystemTray.IconView > Grid#ContainerGrid@ > Border#BackgroundBorder",
  "controlStyles[18].styles[0]": "Background@PointerOver:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.5\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[18].styles[1]": "CornerRadius=20",
  "controlStyles[18].styles[2]": "Width=34",
  "controlStyles[18].styles[3]": "Height=34",
  "controlStyles[18].styles[4]": "Margin=0",
  "controlStyles[19].target": "SystemTray.OmniButton#NotificationCenterButton > Grid@CommonStates > Border#BackgroundBorder",
  "controlStyles[19].styles[0]": "Background@PointerOver:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.5\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[19].styles[1]": "CornerRadius=20",
  "controlStyles[19].styles[2]": "Width=82",
  "controlStyles[19].styles[3]": "Height=34",
  "controlStyles[19].styles[4]": "Margin=1,2,-1,2",
  "controlStyles[20].target": "SystemTray.OmniButton#ControlCenterButton > Grid@CommonStates > Border#BackgroundBorder",
  "controlStyles[20].styles[0]": "Background@PointerOver:=<SolidColorBrush x:Name=\"SystemChromeHigh\" Opacity=\"0.5\" Color=\"{ThemeResource SystemChromeHighColor}\" />",
  "controlStyles[20].styles[1]": "CornerRadius=20",
  "controlStyles[20].styles[2]": "Height=34",
  "controlStyles[20].styles[3]": "Margin=2"
}
```
</details>
