# Borderless theme for Windows 11 Taskbar Styler

Taskbar dock-like theme with removal of borders and drop shadows from hover flyouts (thus the name), tray flyout, volume/brightness flyouts, and taskbar overflow.

**Author**: [Ali Cool](https://github.com/AliCool412)

**Special thanks to**: [CryptoProgenitor](https://github.com/CryptoProgenitor) for the column definitions used in this theme.

![Screenshot](screenshot.png)

## Customization

To apply the customizations below, set the corresponding style constants in the mod settings under "Style constants".

### Taskbar frame width

By default, the taskbar frame width is set to 800px. Set `TaskbarFrameWidth` to adjust the width. For example, use `TaskbarFrameWidth=1000` for a wider 1000px taskbar, this also applies to the height of the vertical taskbar.

### Taskbar frame height

By default, the taskbar frame height is set to 56px. Set `TaskbarFrameHeight` to adjust the height. For example, use `TaskbarFrameHeight=60` for a higher 60px taskbar, this also applies to the Width of the vertical taskbar.

### Re-enabling drop shadows

By default, the theme disables drop shadows from hover popouts and language switcher etc., to re-enable them, set ``Shadows`` to ``<ThemeShadow />``.

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
  - TaskbarFrameHeight=56
  - Shadows=
controlStyles:
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid
    styles:
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
      - HorizontalAlignment=Stretch
      - RowDefinitions:=<RowDefinitionCollection><RowDefinition Height="*"/><RowDefinition Height="Auto"/><RowDefinition Height="Auto"/><RowDefinition Height="*"/></RowDefinitionCollection>
      - VerticalAlignment=Stretch
  - target: Taskbar.TaskbarFrame > Grid#RootGrid@DockingStates
    styles:
      - Tag=horizontal
      - Tag@DockedLeft=vertical
      - Tag@DockedRight=vertical
      - Tag=>taskbarDock
  - target: Taskbar.TaskbarFrame
    styles:
      - Width={{taskbarDock==`vertical`?$TaskbarFrameHeight:$TaskbarFrameWidth}}
      - MaxWidth={{taskbarDock==`vertical`?skip():$TaskbarFrameWidth}}
      - Height={{taskbarDock==`horizontal`?$TaskbarFrameHeight:$TaskbarFrameWidth}}
      - MaxHeight={{taskbarDock==`horizontal`?skip():$TaskbarFrameWidth}}
      - Grid.Column=1
      - Grid.Row=1
  - target: SystemTray.SystemTrayFrame
    styles:
      - Height={{taskbarDock==`vertical`?skip():40}}
      - Width={{taskbarDock==`horizontal`?skip():50}}
      - HorizontalAlignment={{taskbarDock==`vertical`?skip():2}}
      - VerticalAlignment={{taskbarDock==`vertical`?skip():1}}
      - Grid.Column=1
      - Grid.Row=1
  - target: Taskbar.TaskbarFrame > Windows.UI.Xaml.Controls.Grid#RootGrid > Taskbar.TaskbarBackground#BackgroundControl
    styles:
      - CornerRadius=6
      - Margin=2
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Margin=4
  - target: Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder
    styles:
      - Shadow:=$Shadows
      - BorderThickness=0
  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - Shadow:=$Shadows
      - BorderThickness=0
  - target: Taskbar.OverflowToggleButton#OverflowButton > Taskbar.TaskListButtonPanel#OverflowToggleButtonRootPanel > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.FontIcon#FontIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock, Taskbar.OverflowToggleButton#OverflowButton > Taskbar.TaskListButtonPanel#OverflowToggleButtonRootPanel > Windows.UI.Xaml.Controls.FontIcon#FontIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock
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
      - Shadow:=$Shadows
      - BorderThickness=0
  - target: Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground
    styles:
      - Shadow:=$Shadows
      - BorderThickness=0
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher
    styles:
      - Width=960
  - target: Windows.UI.Xaml.Controls.Border#VirtualDesktopSwitcherBackground
    styles:
      - BorderThickness=0
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement
    styles:
      - Margin=210,0,210,12
```
</details>
