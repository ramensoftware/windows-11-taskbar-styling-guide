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
      - ActualHeight=>containerGridHeight
  - target: Taskbar.TaskbarFrame > Grid#RootGrid@DockingStates
    styles:
      - Tag=horizontal
      - Tag@DockedLeft=vertical
      - Tag@DockedRight=vertical
      - Tag=>taskbarDock
  - target: Taskbar.TaskbarFrame
    styles:
      - Width={{taskbarDock==`vertical`?$TaskbarFrameHeight:TrayInFrameWidth==``?$TaskbarFrameWidth:`Auto`}}
      - MaxWidth={{taskbarDock==`vertical`?skip():TrayInFrameWidth==``?$TaskbarFrameWidth:skip()}}
      - MinWidth={{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():max((containerGridWidth-$TaskbarFrameWidth)/2,0)+$TaskbarFrameWidth}}
      - Height={{taskbarDock==`vertical`?min($TaskbarFrameWidth,containerGridHeight):$TaskbarFrameHeight}}
      - Grid.Column={{TrayInFrameWidth==``?1:taskbarDock==`vertical`?1:0}}
      - Grid.ColumnSpan={{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():4}}
      - Grid.Row=1
      - HorizontalAlignment={{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():`Left`}}
      - // Builds where the tray is an item of the taskbar frame. The frame and the repeater stay at the left edge, since Explorer positions the tray, its flyouts and the jump lists from item positions within the repeater as if it started there. The bar is moved by margins on the items instead.
  - target: SystemTray.SystemTrayFrame
    styles:
      - Height={{taskbarDock==`vertical`?skip():40}}
      - Width={{taskbarDock==`vertical`?50:skip()}}
      - HorizontalAlignment={{taskbarDock==`vertical`?skip():2}}
      - VerticalAlignment={{taskbarDock==`vertical`?skip():1}}
      - Grid.Column=1
      - Grid.Row=1
  - target: Taskbar.TaskbarFrame > Windows.UI.Xaml.Controls.Grid#RootGrid > Taskbar.TaskbarBackground#BackgroundControl
    styles:
      - CornerRadius=6
      - Margin={{TrayInFrameWidth==``?2:taskbarDock==`vertical`?2:max((containerGridWidth-$TaskbarFrameWidth)/2,0)+2}},2,2,2
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Margin={{TrayInFrameWidth==``?4:taskbarDock==`vertical`?4:0}},4,{{TrayInFrameWidth==``?4:taskbarDock==`vertical`?4:0}},4
      - HorizontalAlignment={{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():`Left`}}
      - MaxWidth={{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():$TaskbarFrameWidth-8}}
      - ActualWidth=>BarRepeaterWidth
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.ExperienceToggleButton, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.TaskListButton, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.AugmentedEntryPointButton, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.TaskbarExtensionElement
    styles:
      - Margin={{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():4+max((containerGridWidth-$TaskbarFrameWidth)/2,0)}},0,{{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():-(4+max((containerGridWidth-$TaskbarFrameWidth)/2,0))}},0
      - // Moves each item by the bar offset. The negative right margin keeps the item's width, and so the repeater's, independent of the offset.
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
      - Height={{taskbarDock==`vertical`?2:32}}
      - Width={{taskbarDock==`vertical`?32:2}}
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
  - target: Taskbar.TaskbarExtensionElement > ContentPresenter > SystemTray.SystemTrayFrame
    styles:
      - ActualWidth=>TrayInFrameWidth
      - Margin={{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():max($TaskbarFrameWidth-8-BarRepeaterWidth,0)}},0,{{TrayInFrameWidth==``?skip():taskbarDock==`vertical`?skip():-max($TaskbarFrameWidth-8-BarRepeaterWidth,0)}},0
      - // Moves the tray to the bar's right edge. The negative right margin keeps the repeater's width independent of the move.
  - target: :root > ScrollViewer > ScrollContentPresenter > Border
    styles:
      - ActualWidth=>containerGridWidth
```
</details>
