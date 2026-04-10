# DockLike theme for Windows 11 Taskbar Styler

**Author**: [Amber](https://github.com/AmberWat)

![Screenshot of taskbar](screenshot.png)

## Notes

This theme is meant as a fairly vanilla implementation of a dock-like taskbar. It works great out of the box, but there are several tweaks that can be made.

### Suggested Windows settings

- Set taskbar alignment to center
- Hide the widgets button
- If you have another clock, for example from a Rainmeter skin or an application like ElevenClock, you can hide the taskbar clock in Windows date & time settings

### Left align the taskbar (tweak)

Do not use the Windows taskbar setting to left align. Instead, add the following control styles:

Target:
```
Taskbar.TaskbarFrame
```
Styles:
```
HorizontalAlignment=Left
Margin=0,0,250,0
```

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Style:
```
CornerRadius=0,8,0,0
```

### Make the taskbar float (tweak)

This gives it an appearance closer to the MacOS dock.

![Screenshot of floating taskbar](screenshot_floating.png)

1. Use the mod [Taskbar height and icon size](https://windhawk.net/mods/taskbar-icon-size) to increase the height of the taskbar by 4 (usually from 48 to 52). This compensates for the added spacing.

2. Add the following control styles:

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Styles:
```
Margin=0,1,0,3
```
```
CornerRadius=8
```

Target:
```
Grid#SystemTrayFrameGrid
```
Style:
```
Margin=8,1,8,3
```

### Add a border (tweak)

1. Add the following control styles:

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Styles:
```
BorderThickness=1
```
```
BorderBrush:=<SolidColorBrush Color="{ThemeResource SurfaceStrokeColorDefault}" />
```

Target:
```
Grid#SystemTrayFrameGrid
```
Styles:
```
BorderThickness=1
```
```
BorderBrush:=<SolidColorBrush Color="{ThemeResource SurfaceStrokeColorDefault}" />
```

2. If you haven't applied the floating taskbar tweak, add the following control style:

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Style:
```
Margin=0,0,0,-2
```

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
  - target: Taskbar.TaskbarFrame
    styles:
      - Width=Auto
      - HorizontalAlignment=Center
      - Margin=250,0,250,0
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Background:=<AcrylicBrush TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.8" FallbackColor="{ThemeResource SystemChromeLowColor}" />
      - Padding=6,0,6,0
      - CornerRadius=8,8,0,0
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SurfaceStrokeColorDefault}" />
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Visibility=Collapsed
  - target: Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Margin=0
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Background:=<AcrylicBrush TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.8" FallbackColor="{ThemeResource SystemChromeLowColor}" />
      - Margin=-4,-8,-4,-8
      - CornerRadius=10
      - BorderThickness=12,12,12,12
      - BackgroundSizing=InnerBorderEdge
  - target: SystemTray.ChevronIconView
    styles:
      - Padding=0
  - target: SystemTray.NotifyIconView#NotifyItemIcon
    styles:
      - Padding=0
  - target: SystemTray.OmniButton
    styles:
      - Padding=0
  - target: SystemTray.CopilotIcon
    styles:
      - Padding=0
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > systemtray:IconView#SystemTrayIcon > Grid
    styles:
      - Padding=4,0,4,0
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid
    styles:
      - Padding=0
  - target: SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon
    styles:
      - Padding=0
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Margin=0,-4,-12,-4
  - target: Taskbar.Gripper#GripperControl
    styles:
      - Width=Auto
      - MinWidth=24
```
</details>
