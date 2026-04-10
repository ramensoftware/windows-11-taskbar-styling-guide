# TaskbarToStatusbar theme for Windows 11 Taskbar Styler

**Author**: [HTImen](https://github.com/HTImen)

![Screenshot](screenshot.png)

This theme turns the taskbar into a true single-line statusbar. Get an experience similar to Windows Phone or Android (Holo UI).

* Click the left corner of the statusbar to show the Start menu.
* Click the area to the left of the tray to show the task view.
* Click the area to the right of the tray to show the desktop.

> [!NOTE]
> You can enable or disable activation areas in the standard Windows taskbar settings if you need access to the taskbar context menu with the task manager.
![Screenshot](Screenshot1.png)

## More details

* I tested the theme for 3 months on Windows 11 25H2 (24H2). There are no known issues. All pop-ups and keyboard shortcuts work.
* Compatible with both light and dark mode.
* Compatible with both left and center alignment of the Start menu.

![Screenshot](Screenshot2.png) \
![Screenshot](Screenshot3.png) \
![Screenshot](Screenshot4.png)

## Suggested additional mods

* [Taskbar height and icon size](https://windhawk.net/mods/taskbar-icon-size) - to customize the height of the statusbar.
* [Taskbar on top for Windows 11](https://windhawk.net/mods/taskbar-on-top) - to move the statusbar to the top of the screen.

## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
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

```yaml
controlStyles:
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Width=Auto
      - HorizontalAlignment=Left
  - target: Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=TaskViewButton] > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Width=3840
      - Margin=0,0,-3840,0
  - target: Taskbar.ExperienceToggleButton#LaunchListButton > Taskbar.TaskListButtonPanel > Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer#Icon
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - Visibility=Collapsed
  - target: Taskbar.SearchBoxButton#SearchBoxButton[AutomationProperties.AutomationId=SearchButton] > Taskbar.TaskListButtonPanel
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarExtensionElement
    styles:
      - Visibility=Collapsed
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskListLabeledButtonPanel#IconPanel
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskListButtonPanel#OverflowToggleButtonRootPanel
    styles:
      - Visibility=Collapsed
  - target: SystemTray.SystemTrayFrame
    styles:
      - HorizontalAlignment=Center
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Width=1920
      - Margin=0,0,-1920,0
  - target: SystemTray.StackListView#IconStack[AutomationProperties.AutomationId=ShowDesktop] > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon
    styles:
      - Width=1920
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid@ > Rectangle#ShowDesktopPipe
    styles:
      - Fill=Transparent
  - target: SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid
    styles:
      - Padding=4,0,4,0
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid
    styles:
      - Padding=4,0,4,0
  - target: SystemTray.AdaptiveTextBlock#LanguageInnerTextBlock > Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock
    styles:
      - TextTrimming=1
      - Height=20
      - FontSize=14
  - target: TextBlock#BatteryTextBlock
    styles:
      - FontSize=14
  - target: TextBlock#TimeInnerTextBlock
    styles:
      - FontSize=14
  - target: TextBlock#DateInnerTextBlock
    styles:
      - Visibility=Collapsed
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Margin=0,-4,0,-4
      - Opacity=0.75
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=<SolidColorBrush Color="{ThemeResource TextFillColorInverse}"  Opacity="1.0" />
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid
    styles:
      - Background=Black
```
</details>
