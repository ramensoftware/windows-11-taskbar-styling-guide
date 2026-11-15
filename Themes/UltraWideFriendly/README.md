# UltraWideFriendly theme for Windows 11 Taskbar Styler

A minimal, floating dual-island taskbar inspired by macOS dock aesthetics. Separates the app icons and system tray into two distinct rounded islands with a semi-transparent ghost bar behind them.

**Author**: [CryptoProgenitor](https://github.com/CryptoProgenitor)

![Screenshot](screenshot.png)

## Features

- **Dual Islands**: App icons and system tray float as separate rounded containers
- **Ghost Bar**: Semi-transparent backdrop ties the composition together
- **Centered Layout**: Both islands center automatically using flexible grid columns
- **Floating Effect**: Small vertical margin creates a subtle lift from screen edge
- **Clean Aesthetic**: Theme-aware backgrounds with rounded corners (10px radius)

## Customization

To apply the customizations below, set the corresponding style constants in the mod settings under "Style constants".

### Taskbar frame max width

Set `TaskbarFrameMaxWidth` to limit the maximum width of the taskbar. For example: `TaskbarFrameMaxWidth=800` will cap the taskbar at 800px.

### Island background color

Set `IslandBackgroundColor` to your preferred color. Example values:
* `IslandBackgroundColor=#FF202020`  → Dark gray (default)
* `IslandBackgroundColor=#FF000000`  → Pure black
* `IslandBackgroundColor=#FF1a1a2e`  → Dark navy

### Ghost bar opacity

Set `GhostBarBackgroundColor` to adjust the opacity of the ghost bar behind the islands. The default is `#66000000`, which is black with 40% opacity. You can increase or decrease the opacity by changing the alpha channel (the first two digits):
* `GhostBarBackgroundColor=#66000000`   → 40% opacity (default)
* `GhostBarBackgroundColor=#99000000`   → 60% opacity
* `GhostBarBackgroundColor=#33000000`   → 20% opacity
* `GhostBarBackgroundColor=Transparent` → No ghost bar

### Adjust island float (vertical gap)

Set `IslandVerticalMargin` to adjust the vertical margins of the islands, creating more or less of a floating effect:
* `IslandVerticalMargin=3`  → 3px float (default)
* `IslandVerticalMargin=6`  → 6px float (more dramatic)
* `IslandVerticalMargin=0`  → No float

### Adjust island gap

Set `IslandHorizontalMargin` to change the horizontal margins between islands:
* `IslandHorizontalMargin=5`  → 10px gap (default)
* `IslandHorizontalMargin=10` → 20px gap

## Notes

- Designed for Windows 11 with taskbar icons centered
- Works with both light and dark system themes
- The app island has wider padding (25px) for more clickable area; tray has tighter padding (5px)

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
  - GhostBarBackgroundColor=#66000000
  - IslandBackgroundColor={ThemeResource ControlFillColorDefault}
  - IslandVerticalMargin=3
  - IslandHorizontalMargin=5
  - TaskbarFrameMaxWidth=8000
  - // Builds where the tray is an item of the taskbar frame, with a horizontal taskbar. The frame stays at the taskbar's left edge and the repeater at the frame's top left corner there, since Explorer places the tray, its flyouts and the jump lists as if the repeater started there.
  - TrayInFrame=(TrayInFrameWidth==``?0:taskbarDock!=`vertical`)
  - // Where TrayInFrame is set, the island's distance from the screen's left edge.
  - IslandOffset=max((containerGridWidth-IslandRepeaterWidth-25)/2,0)
controlStyles:
  - target: ':root > ScrollViewer > ScrollContentPresenter > Border > Grid'
    styles:
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
      - HorizontalAlignment=Stretch
      - Background:=<SolidColorBrush Color="$GhostBarBackgroundColor"/>
  - target: Taskbar.TaskbarFrame > Grid#RootGrid@DockingStates
    styles:
      - Tag=horizontal
      - Tag@DockedLeft=vertical
      - Tag@DockedRight=vertical
      - Tag=>taskbarDock
  - target: Taskbar.TaskbarFrame
    styles:
      - Grid.Column=1
      - Width={{taskbarDock==`vertical`?skip():`Auto`}}
      - HorizontalAlignment={{$TrayInFrame?`Left`:`Right`}}
      - Margin=0,0,$IslandHorizontalMargin,0
      - MaxWidth={{$TrayInFrame?`Infinity`:containerGridWidth>0?min($TaskbarFrameMaxWidth,containerGridWidth):$TaskbarFrameMaxWidth}}
      - MinWidth={{$TrayInFrame?$IslandOffset+IslandRepeaterWidth-TrayInFrameWidth-2*$IslandHorizontalMargin+25:skip()}}
      - // Makes room for the island background, since the item offset below isn't part of the repeater's width.
  - target: Taskbar.TaskbarFrame > Grid
    styles:
      - Background:={{$TrayInFrame?skip():`<SolidColorBrush Color="$IslandBackgroundColor"/>`}}
      - CornerRadius={{$TrayInFrame?0:10}}
      - Padding={{$TrayInFrame?0:`25,0,25,0`}}
      - Margin={{$TrayInFrame?0:`0,$IslandVerticalMargin,0,$IslandVerticalMargin`}}
  - target: SystemTray.SystemTrayFrame
    styles:
      - Grid.Column=2
      - Width=Auto
      - HorizontalAlignment=Left
      - Margin={{$TrayInFrame?25+2*$IslandHorizontalMargin:$IslandHorizontalMargin}},0,0,0
  - target: StackPanel#SystemTrayFrameGrid, Grid#SystemTrayFrameGrid
    styles:
      - Background:=<SolidColorBrush Color="$IslandBackgroundColor"/>
      - CornerRadius=10
      - Padding=5,0,5,0
      - Margin=0,$IslandVerticalMargin,0,$IslandVerticalMargin
  - target: Taskbar.TaskbarBackground#BackgroundControl
    styles:
      - Visibility={{$TrayInFrame?`Visible`:`Collapsed`}}
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid
    styles:
      - Background:={{$TrayInFrame?`<SolidColorBrush Color="$IslandBackgroundColor"/>`:skip()}}
      - CornerRadius=10
      - Margin={{$TrayInFrame?$IslandOffset:skip()}},$IslandVerticalMargin,{{$TrayInFrame?max(TrayInFrameWidth+2*$IslandHorizontalMargin-25-$IslandOffset,0):skip()}},$IslandVerticalMargin
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill=Transparent
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarExtensionElement > ContentPresenter > SystemTray.SystemTrayFrame
    styles:
      - ActualWidth=>TrayInFrameWidth
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - HorizontalAlignment={{$TrayInFrame?`Left`:skip()}}
      - MaxWidth={{$TrayInFrame?min($TaskbarFrameMaxWidth-25+TrayInFrameWidth+2*$IslandHorizontalMargin,containerGridWidth-25):skip()}}
      - ActualWidth=>IslandRepeaterWidth
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.ExperienceToggleButton, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.TaskListButton, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.AugmentedEntryPointButton, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.TaskbarExtensionElement, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.OverflowToggleButton
    styles:
      - Margin={{$TrayInFrame?25+$IslandOffset:skip()}},0,{{$TrayInFrame?-(25+$IslandOffset):skip()}},0
      - // Moves each item by the island offset. The negative right margin keeps the item's width, and so the repeater's, independent of the offset. Also replaces the gap Explorer adds before the tray.
  - target: :root > ScrollViewer > ScrollContentPresenter > Border
    styles:
      - ActualWidth=>containerGridWidth
      - Background:={{TrayInFrameWidth==``?skip():`<SolidColorBrush Color="$GhostBarBackgroundColor"/>`}}
```
</details>
