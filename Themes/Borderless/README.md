# Borderless theme for Windows 11 Taskbar Styler

Taskbar dock-like theme with removal of borders and drop shadows from hover flyouts (thus the name), tray flyout, volume/brightness flyouts, and taskbar overflow.

**Author**: [Ali Cool](https://github.com/AliCool412)

![Screenshot](screenshot.png)

## Notice
The theme might look different with the default taskbar height. To solve this, install the "Taskbar height and icon size" mod and set the taskbar height to a minimum of 56 (as opposed to the default height being 48).

![Screenshot with default height](screenshot-default-height.png)

## Customization

To apply the customizations below, set the corresponding style constants in the mod settings under "Style constants".

### Taskbar frame width

By default, the taskbar frame is set to 800px. Set `TaskbarFrameWidth` to adjust the width. For example, use `TaskbarFrameWidth=1000` for a wider 1000px taskbar.

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
styleConstants:
  - TaskbarFrameWidth=800
controlStyles:
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid
    styles:
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
      - HorizontalAlignment=Stretch
  - target: Taskbar.TaskbarFrame
    styles:
      - Grid.Column=1
      - Width=$TaskbarFrameWidth
      - Margin=0
      - MaxWidth=$TaskbarFrameWidth
  - target: SystemTray.SystemTrayFrame
    styles:
      - Grid.Column=1
      - Width=Auto
      - HorizontalAlignment=Right
      - Height=40
      - VerticalAlignment=Center
  - target: Taskbar.TaskbarFrame > Windows.UI.Xaml.Controls.Grid#RootGrid > Taskbar.TaskbarBackground#BackgroundControl
    styles:
      - CornerRadius=6
      - Margin=0,2,0,2
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Margin=0,4,0,4
  - target: Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder
    styles:
      - Shadow:=
      - BorderThickness:=
  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - Shadow:=
      - BorderThickness:=
  - target: Taskbar.OverflowToggleButton#OverflowButton > Taskbar.TaskListButtonPanel#OverflowToggleButtonRootPanel > Windows.UI.Xaml.Controls.FontIcon#FontIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock
    styles:
      - Text=
  - target: Windows.UI.Xaml.Shapes.Rectangle#MostRecentlyUsedDivider
    styles:
      - Height=32
      - Width=2
  - target: Windows.UI.Xaml.Shapes.Rectangle#LeftOverflowButtonDivider
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Shapes.Rectangle#RightOverflowButtonDivider
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#OverflowFlyoutListRepeater
    styles:
      - Height=48
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid
    styles:
      - Background:=
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid
    styles:
      - Margin=390,0,574,12
      - Shadow:=
      - BorderThickness:=
  - target: Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground
    styles:
      - Shadow:=
```
</details>
