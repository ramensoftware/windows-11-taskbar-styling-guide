# RosePine theme for Windows 11 Taskbar Styler

This theme was originally [shared on
Reddit](https://www.reddit.com/r/desktops/comments/1e0o08e/windows_11_rose_pine_been_messing_with_windhawk_a/).

**Author**: [asev](https://github.com/lunar-os)

![Screenshot](screenshot.png)

## Notes

* This theme is intended to be used with the following mods and settings.
  Install each mod, go to the "Advanced" tab, copy the settings to the text box
  under "Mod settings" and click "Save".
  * [Taskbar height and icon size](https://windhawk.net/mods/taskbar-icon-size):
    [Settings](https://github.com/lunar-os/windowsdesktop/blob/main/WindhawkConfigs/Taskbar%20height%20and%20icon%20size).
  * [Taskbar Clock
    Customization](https://windhawk.net/mods/taskbar-clock-customization):
    [Settings](https://github.com/lunar-os/windowsdesktop/blob/main/WindhawkConfigs/Taskbar%20Clock%20Customization).
  * [Taskbar Labels for Windows 11](https://windhawk.net/mods/taskbar-labels):
    [Settings](https://github.com/lunar-os/windowsdesktop/blob/main/WindhawkConfigs/Taskbar%20Labels).
* The theme is based off of [RosePine Theme](https://rosepinetheme.com/).
* It removes the start button and the network icon. If you need these, add them
  using the
  [guide](https://github.com/ramensoftware/windows-11-taskbar-styling-guide).
* Font used is [JetBrainsMono Nerd
  Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/JetBrainsMono.zip).

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
controlStyles:
  - target: Taskbar.TaskListButton
    styles:
      - CornerRadius=3
  - target: SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock
    styles:
      - FontSize=16
  - target: SystemTray.NotifyIconView#NotifyItemIcon
    styles:
      - MinWidth=25
  - target: SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[1] > SystemTray.IconView > Grid > Grid
    styles:
      - Visibility=Collapsed
  - target: SystemTray.TextIconContent > Grid#ContainerGrid
    styles:
      - Padding=2
  - target: SystemTray.ChevronIconView
    styles:
      - MinWidth=27
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskListLabeledButtonPanel > Border#BackgroundElement
    styles:
      - Background:=#302d47
      - CornerRadius=6
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Background:=#302d47
      - CornerRadius=6
      - Margin=0,5,4,4
      - Padding=3,0,-8,0
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Rectangle#RunningIndicator
    styles:
      - Height=27
      - RadiusX=5
      - RadiusY=5
      - StrokeThickness=2
      - Stroke@InactivePointerOver=#ebbcba
      - Stroke@InactivePressed=#ebbcba
      - Stroke@ActiveNormal=#ebbcba
      - Stroke@ActivePointerOver=#ebbcba
      - Stroke@ActivePressed=#ebbcba
      - Fill=Transparent
      - Width=37
      - VerticalAlignment=1
      - Canvas.ZIndex=1
  - target: SystemTray.ImageIconContent > Grid#ContainerGrid > Image
    styles:
      - Width=13
  - target: SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock
    styles:
      - FontSize=14
  - target: TextBlock#LabelControl
    styles:
      - FontFamily=JetBrainsMono NF
      - Foreground=#e0def4
      - Padding=2,0,8,0
  - target: Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton]
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill=Transparent
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill
    styles:
      - Fill=#302d47
  - target: Rectangle#BackgroundStroke
    styles:
      - Fill=Transparent
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement
    styles:
      - Background=#302d47
  - target: TextBlock#DateInnerTextBlock
    styles:
      - Margin=0,0,0,-2
  - target: Grid#OverflowRootGrid > Border
    styles:
      - Background=#302d47
```
</details>
