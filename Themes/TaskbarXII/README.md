# ✦ TaskbarXII theme for Windows 11 Taskbar Styler :3

**Author**: [ryokr](https://github.com/ryokr)

![Demonstration](screenshot.png)

## Suggested Windows settings

- Use the default taskbar alignment (center).
- You can hide the bell icon via Notifications in Settings.

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
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid
    styles:
      - Background:=<AcrylicBrush TintColor="{ThemeResource SystemListLowColor}" TintOpacity="0.1" FallbackColor="{ThemeResource SystemChromeHighColor}" />
  - target: Taskbar.TaskbarFrame
    styles:
      - HorizontalAlignment=Right
      - Width=Auto
      - Height=56
      - Grid.Column=0
      - Margin=0,0,2,0
  - target: Taskbar.TaskbarFrame > Grid
    styles:
      - Height=48
      - CornerRadius=4
  - target: Taskbar.TaskbarBackground#BackgroundControl
    styles:
      - Height=48
      - Opacity=0.7
      - //Transform3D:=<CompositeTransform3D TranslateX="156.5"/>
  - target: Taskbar.TaskbarBackground > Grid
    styles:
      - CornerRadius=4
      - Opacity=1
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Margin=0,0,3,0
  - target: Taskbar.SearchBoxButton > Taskbar.TaskListButtonPanel
    styles:
      - Margin=2,0,6,0
  - target: TextBlock#SearchBoxTextBlock
    styles:
      - Text=✦ Meow
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.AugmentedEntryPointButton > Taskbar.TaskListButtonPanel
    styles:
      - //Background:=<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="0.6" />
      - //CornerRadius=4
      - //Padding=0
      - //Margin=0,0,7,0
      - //Margin=4
  - target: Taskbar.AugmentedEntryPointButton > Taskbar.TaskListButtonPanel > Grid
    styles:
      - //Margin=8,0,0,0
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
  - target: SystemTray.SystemTrayFrame
    styles:
      - HorizontalAlignment=Left
      - Grid.Column=1
      - Margin=2,0,0,0
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Background:=<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="0.6" />
      - CornerRadius=4
      - Padding=8,3,0,3
  - target: SystemTray.Stack#SecondaryClockStack
    styles:
      - Grid.Column=8
  - target: SystemTray.OmniButton#ControlCenterButton
    styles:
      - Grid.Column=4
  - target: SystemTray.OmniButton#NotificationCenterButton
    styles:
      - Grid.Column=5
  - target: SystemTray.Stack#MainStack
    styles:
      - Grid.Column=6
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Grid.Column=7
  - target: SystemTray.DateTimeIconContent > Grid > StackPanel
    styles:
      - Orientation=Horizontal
      - Spacing=12
  - target: TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
  - target: TextBlock#TimeInnerTextBlock
    styles:
      - //Transform3D:=<CompositeTransform3D TranslateY="10"/>
      - FontSize=15
      - FontWeight=Bold
      - //Margin=94,0,0,0
  - target: TextBlock#DateInnerTextBlock
    styles:
      - //Transform3D:=<CompositeTransform3D TranslateY="-10"/>
      - FontSize=15
      - FontWeight=SemiBold
      - //HorizontalAlignment=Left
  - target: Windows.UI.Xaml.Controls.ScrollViewer > Windows.UI.Xaml.Controls.ScrollContentPresenter > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.Grid
    styles:
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
  - target: Taskbar.AugmentedEntryPointButton > Taskbar.TaskListButtonPanel
    styles:
      - Margin=0
```
</details>
