# ✦ TaskbarXII theme for Windows 11 Taskbar Styler :3

**Author**: [ryokr](https://github.com/ryokr)

![Demonstration](screenshot.png)

## Suggested Windows settings

- Use the default taskbar alignment (center).
- This theme is not compatible with the vertical taskbar and small taskbar size.

## Widget placement

By default, the widget, if enabled, is shown separately from the taskbar:

![Demonstration](screenshot_dark_with_widget.png)
![Demonstration](screenshot_light_with_widget.png)

To show the widget as part of the taskbar instead, set `separateWidget=0` in the
"Style constants" section of the mod's settings:

![Demonstration](screenshot_dark_no_widget.png)

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
  - separateWidget=1
controlStyles:
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid
    styles:
      - Background:=<AcrylicBrush TintColor="{ThemeResource SystemListLowColor}" TintOpacity="0.1" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="4"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
      - ActualWidth=>containerGridWidth
  - target: Taskbar.TaskbarFrame > Grid#RootGrid@DockingStates
    styles:
      - Tag=horizontal
      - Tag@DockedLeft=vertical
      - Tag@DockedRight=vertical
      - Tag=>taskbarDock
  - target: Taskbar.TaskbarFrame
    styles:
      - Grid.Column=1
      - HorizontalAlignment=Right
      - Width={{taskbarDock==`vertical`?skip():`Auto`}}
      - Height={{taskbarDock==`vertical`?skip():56}}
      - MaxWidth={{taskbarDock==`vertical`?skip():(containerGridWidth>0?containerGridWidth:skip())}}
  - target: Taskbar.TaskbarFrame > Grid
    styles:
      - Height=48
      - CornerRadius=4
  - target: Taskbar.TaskbarBackground#BackgroundControl
    styles:
      - Transform3D:=<CompositeTransform3D TranslateX="{{$separateWidget?(widgetWidth==``?skip():widgetWidth+4.5):skip()}}"/>
      - Opacity=0.7
      - Height=48
  - target: Taskbar.TaskbarBackground > Grid
    styles:
      - CornerRadius=4
      - Opacity=1
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Height=0
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Margin=3,0,3,0
  - target: Taskbar.AugmentedEntryPointButton > Taskbar.TaskListButtonPanel
    styles:
      - Background:={{$separateWidget?`<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="0.6" />`:skip()}}
      - CornerRadius={{$separateWidget?4:skip()}}
      - Padding={{$separateWidget?`6,0,6,0`:skip()}}
      - Margin={{$separateWidget?-3:-4}},0,8,0
      - Width=>widgetBaseWidth
      - MinWidth={{$separateWidget?(widgetBaseWidth>0?widgetBaseWidth+8:skip()):skip()}}
      - ActualWidth=>widgetWidth
  - target: Border#LargeTicker1
    styles:
      - Margin=0,2,4,0
  - target: Border#LargeTicker1 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Image
    styles:
      - MaxHeight=27
      - MaxWidth=27
  - target: Border#LargeTicker1 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer
    styles:
      - MaxHeight=27
      - MaxWidth=27
  - target: Taskbar.SearchBoxButton > Taskbar.TaskListButtonPanel, SearchUx.SearchUI.SearchButtonRootGrid#SearchBoxButtonRootPanel
    styles:
      - Margin=4,0,8,0
  - target: TextBlock#SearchBoxTextBlock
    styles:
      - Text=✦ Meow
  - target: SystemTray.SystemTrayFrame
    styles:
      - Grid.Column=3
      - HorizontalAlignment=Left
      - VerticalAlignment=Center
  - target: StackPanel#SystemTrayFrameGrid, Grid#SystemTrayFrameGrid
    styles:
      - Background:=<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="0.6" />
      - CornerRadius=4
      - Padding=8,3,0,3
  - target: TextBlock#InnerTextBlock[Text=], TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
  - target: SystemTray.DateTimeIconContent > Grid > StackPanel
    styles:
      - Orientation=Horizontal
      - Spacing=12
  - target: TextBlock#TimeInnerTextBlock
    styles:
      - FontSize=15
      - FontWeight=Bold
  - target: TextBlock#DateInnerTextBlock
    styles:
      - FontSize=15
      - FontWeight=SemiBold
```
</details>
