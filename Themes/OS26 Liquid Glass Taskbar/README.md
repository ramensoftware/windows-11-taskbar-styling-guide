# OS26 Liquid Glass Taskbar

This theme styles the Windows 11 Taskbar into a floating, premium OS26-inspired "Liquid Glass" dock. It introduces heavily padded floating margins, pill-shaped rounded elements, custom running indicators, and tailored system tray styling.

## Taskbar Previews
![Taskbar Preview](taskbar_preview.png)

## System Tray & Elements Detail
![System Tray Preview](system_tray_preview.png)

---

## Design Features
* **Floating Dock Layout:** Padded margins (`150px` left/right) transform the taskbar into a distinct floating deck with a `20px` corner radius.
* **Liquid Glass Blur:** Embedded custom `<WindhawkBlur>` styling applied across individual blocks (Start Button, Search Box, Task List, Tray).
* **Cyberpunk Clock Accent:** Configured for the high-tech `Quantico` font face, enlarged text, and cleanly hidden date layouts.
* **Polished Micro-Borders:** Linear gradient accent strokes mimicking glass edge reflections.

### Theme selection

The theme is integrated into the mod and can be selected directly from the mod's settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

### Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>
  
```json
styleConstants:
  - glassBorder = <LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#50ffffff" Offset="0.0" /><GradientStop Color="#10ffffff" Offset="0.5" /><GradientStop Color="#30ffffff" Offset="1.0" /></LinearGradientBrush>
  - buttonBorder = <LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#E0ffffff" Offset="0.0" /><GradientStop Color="#20ffffff" Offset="0.5" /><GradientStop Color="#A0ffffff" Offset="1.0" /></LinearGradientBrush>
  - notifyBorder = <LinearGradientBrush StartPoint="0,0" EndPoint="1,0"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
  - indicatorActive = #60CDFF
  - osdAccent = #ff7060
  - osdTrack = #20ffffff

controlStyles:
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Background := <WindhawkBlur BlurAmount="15" TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.2" />
      - Margin = 150,1,150,4
      - CornerRadius = 20
      - BorderBrush := $glassBorder
      - BorderThickness = 1.2
      - Padding = 10,0

  - target: Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - CornerRadius = 20
      - Background := <WindhawkBlur BlurAmount="60" TintColor="#35ffffff" />
      - Background@InactivePointerOver := <WindhawkBlur BlurAmount="60" TintColor="#45ffffff" />
      - Background@ActivePointerOver := <WindhawkBlur BlurAmount="60" TintColor="#45ffffff" />
      - Background@ActiveNormal := <WindhawkBlur BlurAmount="60" TintColor="#30ffffff" />
      - Background@InactiveNormal := <WindhawkBlur BlurAmount="60" TintColor="#25ffffff" />
      - Background@InactivePressed := <WindhawkBlur BlurAmount="60" TintColor="#30ffffff" />
      - Background@ActivePressed := <WindhawkBlur BlurAmount="60" TintColor="#25ffffff" />
      - BorderBrush := $buttonBorder
      - BorderThickness = 1.2

  - target: Grid#SystemTrayFrameGrid
    styles:
      - Background := <WindhawkBlur BlurAmount="15" TintColor="#25ffffff" />
      - CornerRadius = 14
      - Margin = 60,10,-280,10
      - RenderTransform := <TranslateTransform X="-435" Y="-2"/>
      - Padding = 10
      - BorderBrush := $glassBorder
      - BorderThickness = 1.2

  - target: Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Rectangle#RunningIndicator
    styles:
      - Fill := #90ffffff
      - RadiusX = 4
      - RadiusY = 4
      - Height = 3
      - Width = 10
      - Width@ActiveRunningIndicator = 20
      - Fill@ActiveRunningIndicator = $indicatorActive

  - target: Taskbar.TaskListLabeledButtonPanel > TextBlock#LabelControl
    styles:
      - Margin = 4,0,0,0
      - Foreground = White

  - target: Taskbar.SearchBoxButton
    styles:
      - Background := <WindhawkBlur BlurAmount="60" TintColor="#35ffffff" />
      - CornerRadius = 20
      - Margin = 2,6,2,6
      - BorderBrush := $buttonBorder
      - BorderThickness = 1.2

  - target: TextBlock#SearchBoxTextBlock
    styles:
      - FontSize = 12
      - Foreground = White

  - target: Grid
    styles:
      - RequestedTheme = 2

  - target: Taskbar.TaskListButton#TaskListButton[AutomationProperties.Name=Copilot] > Taskbar.TaskListLabeledButtonPanel#IconPanel > Border#BackgroundElement
    styles:
      - Background := <WindhawkBlur BlurAmount="10" TintColor="#10ffffff" />

  - target: Taskbar.StartButton#StartButton
    styles:
      - Background := <WindhawkBlur BlurAmount="60" TintColor="#35ffffff" />
      - CornerRadius = 20
      - Margin = 2,6,2,6
      - BorderBrush := $buttonBorder
      - BorderThickness = 1.2

  - target: Border#MultiWindowElement
    styles:
      - Visibility = Collapsed

  - target: TextBlock#TimeInnerTextBlock
    styles:
      - Foreground = White
      - FontSize = 18
      - FontFamily = Quantico
      - Margin = 0
      - Padding = 0
      - RenderTransform := <TranslateTransform X="0" Y="1" />

  - target: TextBlock#DateInnerTextBlock
    styles:
      - Foreground = White
      - Visibility = Collapsed
      - RenderTransform := <TranslateTransform X="0" Y="-9" />
      - FontSize = 11
      - FontFamily = vivo Sans EN VF

  - target: SystemTray.TextIconContent > Grid > SystemTray.AdaptiveTextBlock#Base > TextBlock
    styles:
      - Foreground = White

  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton
    styles:
      - Margin = -12,0,0,0

  - target: Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.Name=Task View]
    styles:
      - Background := <WindhawkBlur BlurAmount="60" TintColor="#35ffffff" />
      - CornerRadius = 20
      - Margin = 2,6,2,6
      - BorderBrush := $buttonBorder
      - BorderThickness = 1.2

  - target: taskbar:TaskListLabeledButtonPanel@RunningIndicatorStates > Border
    styles:
      - Background@InactiveRunningIndicatorPointerOver := <WindhawkBlur BlurAmount="40" TintColor="#10ffffff" />
      - CornerRadius = 12
      - BorderBrush@InactiveRunningIndicatorPointerOver := $notifyBorder
      - BorderThickness@InactiveRunningIndicatorPointerOver = 1

  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - CornerRadius = 20
      - Background := <WindhawkBlur BlurAmount="60" TintColor="#35ffffff" />
      - Background@InactivePointerOver := <WindhawkBlur BlurAmount="60" TintColor="#45ffffff" />
      - Background@ActivePointerOver := <WindhawkBlur BlurAmount="60" TintColor="#45ffffff" />
      - Background@ActiveNormal := <WindhawkBlur BlurAmount="60" TintColor="#30ffffff" />
      - Background@InactiveNormal := <WindhawkBlur BlurAmount="60" TintColor="#25ffffff" />
      - Background@InactivePressed := <WindhawkBlur BlurAmount="60" TintColor="#30ffffff" />
      - Margin = 0
      - BorderBrush := $buttonBorder
      - BorderThickness = 1.2

  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundStroke
    styles:
      - Visibility = Collapsed

  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill = Transparent

  - target: SystemTray.NotifyIconView#NotifyItemIcon
    styles:
      - Background := <WindhawkBlur BlurAmount="10" TintColor="#40ffffff" />
      - CornerRadius = 12
      - Margin = 2
      - Padding = 2
      - BorderBrush := $notifyBorder
      - BorderThickness = 2

  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - Background := <WindhawkBlur BlurAmount="30" TintColor="#25ffffff" />
      - CornerRadius = 24
      - BorderThickness = 1.2
      - BorderBrush := $glassBorder
      - Margin = 0,0,0,10
      - Shadow :=

  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect
    styles:
      - Fill = $osdTrack
      - RadiusX = 12
      - RadiusY = 12
      - Height = 18
      - Margin = 0

  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalDecreaseRect
    styles:
      - Fill = $osdAccent
      - RadiusX = 12
      - RadiusY = 12
      - Height = 18

  - target: Windows.UI.Xaml.Controls.Grid#VolumeConfirmator
    styles:
      - Padding = 8,0,8,0

  - target: Windows.UI.Xaml.Controls.Grid#BrightnessConfirmator
    styles:
      - Padding = 15,0,17,0

  - target: Windows.UI.Xaml.Controls.TextBlock#volumeLevelText
    styles:
      - Foreground = White````
