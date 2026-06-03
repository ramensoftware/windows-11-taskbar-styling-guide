# Command Center for Windows 11 Taskbar Styler

Command Center theme inspired by the command centers from various mobile operating systems. It features a completely transparent background to allow for a floating widget styled appearance.

**Author**: [PhantomNimbi](https://github.com/PhantomNimbi)

<img width="100%" src="preview.png" alt="Preview" />

## Notes
- This theme consists of the following backgrounds:
  - Translucent
  - Glass
  - Frosted
  - Acrylic

  In order to switch between these backgrounds, set the value `Background=$Translucent`, `Background=$Glass`, `Background=$Frosted` or `Background=$Acrylic` in the "Style constants" section of the mod's settings.

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

```yml
styleConstants:
  - Translucent=<WindhawkBlur BlurAmount="15" TintColor="#10808080"/>
  - Glass=<WindhawkBlur BlurAmount="5" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Frosted=<WindhawkBlur BlurAmount="20" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Acrylic=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.8" />
  - Background=$Frosted
  - OverlayColor=<AcrylicBrush TintColor="{ThemeResource SystemAltLowColor}" TintOpacity="1" TintLuminosityOpacity="0.8" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" />
  - OverlayColor2=<AcrylicBrush TintColor="{ThemeResource SystemAltLowColor}" TintOpacity="1" TintLuminosityOpacity="0.5" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" />
  - AccentColor=<AcrylicBrush TintColor="{ThemeResource SystemAccentColor}" TintOpacity="1" TintLuminosityOpacity="0.5" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" />
  - ActiveColor=<AcrylicBrush TintColor="{ThemeResource SystemAltLowColor}" TintOpacity="1" TintLuminosityOpacity="1" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" />
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#60808080" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.25" /><GradientStop Color="#40808080" Offset="1" /></LinearGradientBrush>
  - BorderThickness=0.3,1,0.3,1
  - R1=6
  - R2=20
controlStyles:
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Visibility=1
  - target: Rectangle#BackgroundStroke
    styles:
      - Visibility=1
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$R1
  - target: Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - Padding=6
      - Margin=2
      - Background@ActiveNormal:=$ActiveColor
      - Background@ActivePointerOver:=$OverlayColor
      - Background@ActivePressed:=$OverlayColor
      - Background@InactiveNormal:=$Background
      - Background@InactivePointerOver:=$OverlayColor2
      - Background@InactivePressed:=$OverlayColor
      - Background@MultiWindowNormal:=$Background
      - Background@MultiWindowPointerOver:=$OverlayColor2
      - Background@MultiWindowActive:=$ActiveColor
      - Background@MultiWindowPressed:=$OverlayColor
      - CornerRadius=$R1
  - target: Border#BackgroundElement
    styles:
      - Padding=6
      - Margin=2
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$R1
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - Padding=6
      - Margin=2
      - Background@ActiveNormal:=$ActiveColor
      - Background@ActivePointerOver:=$OverlayColor
      - Background@ActivePressed:=$OverlayColor
      - Background@InactiveNormal:=$Background
      - Background@InactivePointerOver:=$OverlayColor2
      - Background@InactivePressed:=$OverlayColor
      - Background@MultiWindowNormal:=$Background
      - Background@MultiWindowPointerOver:=$OverlayColor2
      - Background@MultiWindowActive:=$ActiveColor
      - Background@MultiWindowPressed:=$OverlayColor
      - CornerRadius=$R1
  - target: Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Rectangle#RunningIndicator
    styles:
      - RadiusX=1.5
      - RadiusY=1.5
      - Height=4
      - Width=12
      - Fill:=$ActiveColor
      - Fill@ActiveRunningIndicator:=$AccentColor
      - Width@ActiveRunningIndicator=21
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Padding=6
      - Margin=2
      - Background:=Transparent
      - BorderBrush:=Transparent
      - BorderThickness=0
      - Shadow:=
  - target: Border#BackgroundBorder
    styles:
      - Padding=6
      - Margin=2
      - Background:=Transparent
      - BorderBrush:=Transparent
      - BorderThickness=0
      - Shadow:=
  - target: Grid#OverflowRootGrid > Border
    styles:
      - Padding=6
      - Background:=Transparent
      - BorderBrush:=Transparent
      - BorderThickness=0
      - Shadow:=
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect
    styles:
      - Height=8
      - Margin=0
      - Fill:=$OverlayColor
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalDecreaseRect
    styles:
      - Height=8
  - target: Windows.UI.Xaml.Controls.TextBlock#volumeLevelText
    styles:
      - Margin=0,-2,0,0
  - target: Windows.UI.Xaml.Controls.Grid#VolumeConfirmator
    styles:
      - Padding=8,0,3,0
      - CornerRadius=$R2
  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
      - BorderThickness=0
      - Shadow:=
  - target: Windows.UI.Xaml.Controls.Grid#BrightnessConfirmator
    styles:
      - Padding=25,0,17,0
      - CornerRadius=$R2
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#BrightnessIcon
    styles:
      - Margin=0,-1,12,0
  - target: Microsoft.UI.Xaml.Controls.ProgressBar#ProgressIndicator
    styles:
      - Margin=0,0,0,1
  - target: Windows.UI.Xaml.Shapes.Rectangle#ProgressBarTrack
    styles:
      - Fill:=$OverlayColor
      - RadiusX=1.5
      - RadiusY=1.5
  - target: Windows.UI.Xaml.Shapes.Rectangle#DeterminateProgressBarIndicator
    styles:
      - Fill:=$AccentColor
  - target: Taskbar.TaskListButton#TaskListButton > Taskbar.TaskListLabeledButtonPanel#IconPanel > Microsoft.UI.Xaml.Controls.ProgressBar#ProgressIndicator
    styles:
      - MinHeight=4
      - Width=26
  - target: Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - Padding=6
      - Margin=2
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
      - CornerRadius=$R1
      - Shadow:=
  - target: Taskbar.Badge#BadgeControl
    styles:
      - Height=14
      - MinWidth=14
      - Margin=0,0,0,0
      - CornerRadius=$R2
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundRect
    styles:
      - RadiusX=4
      - RadiusY=4
  - target: MenuFlyoutPresenter
    styles:
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$R1
```
</details>