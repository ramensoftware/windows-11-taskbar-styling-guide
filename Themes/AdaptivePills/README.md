# AdaptivePills theme for Windows 11 Taskbar Styler

**Author**: [Deen-0x](https://github.com/Deen-0x)

## Description
AdaptivePills. A sleek, minimal reinterpretation of the Windows 11 taskbar with a background that turns task buttons into rounded adaptive pills that keep the native feel but breathe more.

## Light Mode
Normal
![Light1](Light1.png)
Maximized
![LightMaximized](LightMaximized.png)

## Dark Mode
Normal
![Dark1](Dark1.png)
Maximized
![DarkMaximized](DarkMaximized.png)

## Demonstration

Pill States
![Dark1](PillDemo.png)

Comparison
![AdaptivePillsTransition](AdaptivePillsTransition.gif)

## Notes
- Theme is designed on Windows 11 - 25H2
- Tested on monitors: 1920x1080 (100% scaling) | 3840x2160 (250% scaling)
- Designed for both light and dark modes
- Designed to work with:
  - *Widgets - On
  - Task view - Off
  - Search - Hidden
  - Taskbar alignment - Center
  - Show smaller taskbar buttons - Never
- *Widgets must be installed to enable the weather widget on the left. Install it back if you previously removed it.
  - https://apps.microsoft.com/detail/9mssgkg348sp
- Pinned applications are not supported (transparent background)
- Activated border indicator for opened application - Optional

## Required Windhawk Mods for similar results
To achieve similar results, install and configure the following Windhawk mods in addition to Taskbar Styler:

- Taskbar Height and Icon Size:

  <details>
  <summary>Click to expand Taskbar Height and Icon Size settings</summary>

  ```yaml
  TaskbarHeight: 41
  IconSize: 15
  TaskbarButtonWidth: 30
  IconSizeSmall: 15
  TaskbarButtonWidthSmall: 15
  ```
  </details><br>

- Taskbar Labels for Windows 11 – to control panels width:

  <details>
  <summary>Click to expand Taskbar Labels for Windows 11 settings</summary>

  ```yaml
    mode: labelsWithCombining
    taskbarItemWidth: 0
    runningIndicatorStyle: fullWidth
    progressIndicatorStyle: sameAsRunningIndicatorStyle
    excludedPrograms:
      - ''
    minimumTaskbarItemWidth: 70
    maximumTaskbarItemWidth: 200
    fontSize: 12
    fontFamily: ''
    textTrimming: characterEllipsis
    leftAndRightPaddingSize: 8
    spaceBetweenIconAndLabel: 18
    runningIndicatorHeight: -1
    runningIndicatorVerticalOffset: 0
    alwaysShowThumbnailLabels: 0
    labelForSingleItem: '%name%'
    labelForMultipleItems: '[%amount%] %name%'
  ```
  </details><br>

- Taskbar Clock Customization – for styling the clock:

  <details>
  <summary>Click to expand Taskbar Clock Customization settings</summary>

  ```yaml
  ShowSeconds: 0
  TimeFormat: ''
  DateFormat: d/M/y
  WeekdayFormat: custom
  WeekdayFormatCustom: Sun, Mon, Tue, Wed, Thu, Fri, Sat
  TopLine: ''
  BottomLine: 📅  %date% | %time%
  MiddleLine: '%weekday%'
  TooltipLine: '%web1_full%'
  TooltipLineMode: append
  Width: 180
  Height: 60
  MaxWidth: 0
  TextSpacing: 1
  DataCollection:
    NetworkMetricsFormat: mbs
    NetworkMetricsFixedDecimals: -1
    PercentageFormat: spacePaddingAndSymbol
    UpdateInterval: 1
    NetworkAdapterName: ''
    GpuAdapterName: ''
  MediaPlayer:
    IgnoredPlayers:
      - ''
    MaxLength: 28
    NoMediaText: No media
    RemoveBrackets: 0
  WebContentWeatherLocation: ''
  WebContentWeatherFormat: '%c 🌡️%t 🌬️%w'
  WebContentWeatherUnits: autoDetect
  WebContentsItems:
    - Url: https://rss.nytimes.com/services/xml/rss/nyt/World.xml
      BlockStart: <item>
      Start: <title>
      End: </title>
      ContentMode: xmlHtml
      SearchReplace:
        - Search: ''
          Replace: ''
      MaxLength: 28
  WebContentsUpdateInterval: 10
  TimeZones:
    - Eastern Standard Time
  TimeStyle:
    Hidden: 1
    TextColor: ''
    TextAlignment: Right
    FontSize: 0
    FontFamily: ''
    FontWeight: ''
    FontStyle: ''
    FontStretch: ''
    CharacterSpacing: 0
  DateStyle:
    Hidden: 0
    TextColor: ''
    TextAlignment: ''
    FontSize: 12
    FontFamily: ''
    FontWeight: Medium
    FontStyle: Normal
    FontStretch: ''
    CharacterSpacing: 0
  oldTaskbarOnWin11: 0
  ```
  </details><br>

- Taskbar Background Helper:

  <details>
  <summary>Click to expand Taskbar Background Helper settings</summary>

  ```yaml
  backgroundStyle: acrylicBlur
  color:
    red: 200
    green: 200
    blue: 200
    accentColor: 0
    transparency: 150
  onlyWhenMaximized: 1
  excludedPrograms:
    - ''
  styleForDarkMode:
    use: 1
    backgroundStyle: acrylicBlur
    color:
      red: 40
      green: 40
      blue: 40
      accentColor: 0
      transparency: 255
  ```
  </details>

## Recommended visual Windhawk Mods
To achieve maximum Taskbar aesthetics, install and configure the following Windhawk mods.

- Taskbar tray system icon tweaks - to declutter the system tray icons (you may also disable the language indicator if you don't need it):
  <details>
  <summary>Click to expand Taskbar tray system icon tweaks settings</summary>

  ```yaml
  hideVolumeIcon: 0
  hideNetworkIcon: 1
  hideBatteryIcon: 1
  grayscaleBatteryIcon: 0
  hideMicrophoneIcon: 0
  hideGeolocationIcon: 1
  hideStudioEffectsIcon: 0
  hideRecallIcon: 0
  hideLanguageBar: 0
  hideLanguageSupplementaryIcons: 1
  hideBellIcon: never
  showDesktopButtonWidth: 12
  ```
  </details><br>

- Windows 11 Notification Center Styler - to remove Notification Center shadows copy the content below (flyout shadows look truncated with transparent taskbar):

  <details>
  <summary>Click to expand Windows 11 Notification Center Styler settings</summary>

  ```yaml
  controlStyles:
    - target: Grid#NotificationCenterGrid
      styles:
        - Shadow :=
    - target: Grid#CalendarCenterGrid
      styles:
        - Shadow :=
    - target: Grid#ControlCenterRegion
      styles:
        - Shadow :=
  ```
  </details><br>

- Windows 11 Start Menu Styler - to remove Start Menu shadows copy the content below (shadows look truncated with transparent taskbar):
  <details>
  <summary>Click to expand Windows 11 Start Menu Styler settings</summary>

  ```yaml
  controlStyles:
    - target: Windows.UI.Xaml.Controls.Border#DropShadow
      styles:
        - Visibility=Collapsed
    - target: Windows.UI.Xaml.Controls.Border#StartDropShadow
      styles:
        - Visibility=Collapsed
    - target: Windows.UI.Xaml.Controls.Border#RootGridDropShadow
      styles:
        - Visibility=Collapsed
    - target: Windows.UI.Xaml.Controls.Border#RightCompanionDropShadow
      styles:
        - Visibility=Collapsed
  ```
  </details>

## Recommended functional Windhawk Mods

To achieve compatible Taskbar functionality, install and configure the following Windhawk mods:

- Click on empty taskbar space - to middle click show desktop on bottom right corner:
  <details>
  <summary>Click to expand Click on empty taskbar space settings</summary>

  ```yaml
  TriggerActionOptions:
    - KeyboardTriggers:
        - none
        - lctrl
        - lshift
        - lalt
        - win
        - rctrl
        - rshift
        - ralt
      MouseTrigger: middle
      TaskbarType: all
      Action: ACTION_SHOW_DESKTOP
      AdditionalArgs: arg1;arg2
  oldTaskbarOnWin11: 0
  eagerTriggerEvaluation: 1
  ```
  </details><br>

- Taskbar minimize/restore on scroll:
  <details>
  <summary>Click to expand Taskbar minimize/restore on scroll settings</summary>

  ```yaml
  scrollOverTaskbarButtons: 1
  scrollOverThumbnailPreviews: 1
  maximizeAndRestore: 0
  reverseScrollingDirection: 0
  oldTaskbarOnWin11: 0
  ```
  </details><br>

- Taskbar Volume Control - to control volume by mouse scroll wheel while hovering over the tray area:
  <details>
  <summary>Click to expand Taskbar Volume Control settings</summary>

  ```yaml
  volumeIndicator: win11
  scrollArea: notification_area
  additionalScrollRegions: ''
  middleClickToMute: 1
  ctrlScrollVolumeChange: 0
  scrollAnywhereKeys:
    shift: 0
    ctrl: 0
    alt: 0
    win: 0
  fullScreenScrolling: disabled
  noAutomaticMuteToggle: 0
  volumeChangeStep: 2
  oldTaskbarOnWin11: 0
  ```
  </details><br>

- Middle click to close on the taskbar:
  <details>
  <summary>Click to expand Middle click to close on the taskbar settings</summary>

  ```yaml
  multipleItemsBehavior: closeAll
  keysToEndTask:
    Ctrl: 1
    Alt: 0
  oldTaskbarOnWin11: 0
  ```
  </details><br>

- Disable Taskbar Thumbnails - to prevent thumbnails opening on hover:
  <details>
  <summary>Click to expand Disable Taskbar Thumbnails settings</summary>

  ```yaml
  mode: disabled
  noVirtualDesktopSwitcherHover: 0
  noTooltips: 0
  oldTaskbarOnWin11: 0
  ```
  </details><br>

- Taskbar Thumbnail Reorder:


## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme "AdaptivePills" and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

  <details>
  <summary>Theme content to import (click to expand)</summary>
  
  ```yaml
  styleConstants:
    - pillHeight = 26
    - pillRadius = 7
    - highlightRadius = {{$pillRadius*0.69}}
    - highlightOffset = 3
    - pillBorderThickness = 1
    - highlightBorderThickness = 1
    - showHighlightActiveBorder = 1
    - pillBorderColor = <SolidColorBrush Color="{ThemeResource AdaptivePillBorder}"/>
    - highlightActiveBorderColor = <SolidColorBrush Color="{ThemeResource SystemAccentColor}" Opacity="0.9"/>
    - pillFillColor = <WindhawkBlur BlurAmount="8" TintColor="{ThemeResource AdaptivePillFill}" TintOpacity="0.45" TintLuminosityOpacity="0.8" NoiseOpacity="0.2"/>
    - iconLabelSpacing = 7
    - pillSpacing = 8
    - iconBadgeHeight = 13
    - iconBadgeSpacing = 0,5,2,0
  controlStyles:
    - target: Border#BackgroundBorder
      styles:
        - CornerRadius := $highlightRadius
        - BorderThickness := $highlightBorderThickness
    - target: Border#BackgroundElement
      styles:
        - CornerRadius := $highlightRadius
    - target: ScrollViewer > ScrollContentPresenter > Border > Grid > Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.TaskListButton#TaskListButton > Taskbar.TaskListLabeledButtonPanel#IconPanel
      styles:
        - Padding = 0
        - Margin = 0
    - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Rectangle#RunningIndicator
      styles:
        - Visibility = Visible
        - Margin = 0,2,0,1
        - Height := $pillHeight
        - VerticalAlignment = 1
        - RadiusX := $pillRadius
        - RadiusY := $pillRadius
        - Fill := $pillFillColor
        - StrokeThickness := $pillBorderThickness
        - Stroke := $pillBorderColor
        - Canvas.ZIndex = -1
    - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement
      styles:
        - VerticalAlignment = 1
        - Margin := {{$highlightOffset}},1,{{$highlightOffset+6}},0
        - Height = {{$pillHeight-$highlightOffset*2}}
        - BorderThickness := $highlightBorderThickness
        - Margin@MultiWindowPointerOver := {{$highlightOffset}},1,16,0
        - Margin@MultiWindowNormal := {{$highlightOffset}},1,16,0
        - Margin@MultiWindowActive := {{$highlightOffset}},1,16,0
        - Margin@MultiWindowPressed := {{$highlightOffset}},1,16,0
        - Margin@RequestingAttentionMulti := {{$highlightOffset}},1,16,0
        - Margin@RequestingAttentionMultiPointerOver := {{$highlightOffset}},1,16,0
        - Margin@RequestingAttentionMultiPressed := {{$highlightOffset}},1,16,0
        - BorderThickness@ActiveNormal := {{$highlightBorderThickness*$showHighlightActiveBorder}}
        - BorderThickness@ActivePointerOver := {{$highlightBorderThickness*$showHighlightActiveBorder}}
        - BorderBrush@ActivePointerOver := $highlightActiveBorderColor
        - BorderBrush@ActiveNormal := $highlightActiveBorderColor
        - BorderThickness@MultiWindowActive := {{$highlightBorderThickness*$showHighlightActiveBorder}}
        - BorderBrush@MultiWindowPointerOver := $highlightActiveBorderColor
        - BorderThickness@MultiWindowPointerOver := {{$highlightBorderThickness*$showHighlightActiveBorder}}
        - BorderBrush@MultiWindowActive := $highlightActiveBorderColor
    - target: Border#MultiWindowElement
      styles:
        - HorizontalAlignment = 2
        - CornerRadius := $highlightRadius
        - BorderThickness = 0
        - Height := {{$pillHeight-$highlightOffset-$pillBorderThickness-4}}
        - Margin = 0,0,10,0
    - target: Taskbar.TaskbarBackground#BackgroundControl > Grid > Rectangle#BackgroundFill
      styles:
        - Visibility = Collapsed
    - target: Rectangle#BackgroundStroke
      styles:
        - Visibility = Collapsed
    - target: Taskbar.SearchBoxButton
      styles:
        - Visibility = Collapsed
    - target: Taskbar.ExperienceToggleButton#LaunchListButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
      styles:
        - Height = 0
    - target: Taskbar.TaskListButton#TaskListButton
      styles:
        - Margin := {{$pillSpacing-6}},0,0,0
        - Padding = 0
    - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > TextBlock#LabelControl
      styles:
        - Margin := {{$iconLabelSpacing}},0,12,2
        - HorizontalAlignment = 0
        - VerticalAlignment = 1
    - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Image#OverlayIcon
      styles:
        - Width := $iconBadgeHeight
        - Height := $iconBadgeHeight
        - Margin := $iconBadgeSpacing
    - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Taskbar.Badge#BadgeControl
      styles:
        - MinWidth := $iconBadgeHeight
        - Width := $iconBadgeHeight
        - Height := $iconBadgeHeight
        - Margin := $iconBadgeSpacing
    - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Taskbar.Badge#BadgeControl > Grid > TextBlock#BadgeText
      styles:
        - FontSize = 10
        - HorizontalAlignment = 1
    - target: Grid#SystemTrayFrameGrid
      styles:
        - Margin = 0,7,5,7
    - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.OmniButton#NotificationCenterButton > Grid
      styles:
        - Height := $pillHeight
        - Margin := {{$pillSpacing}},0,-7,0
        - CornerRadius = $pillRadius
        - Background := $pillFillColor
        - BorderThickness := $pillBorderThickness
        - BorderBrush := $pillBorderColor
    - target: Grid > Border#BackgroundBorder
      styles:
        - Margin = {{$highlightOffset}}
    - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter#ContentPresenter
      styles:
        - Margin = 0,0,0,1
    - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.OmniButton#ControlCenterButton > Grid
      styles:
        - Height := $pillHeight
        - Padding := {{-$pillBorderThickness}}
        - Background := $pillFillColor
        - CornerRadius = 0,$pillRadius,$pillRadius,0
        - BorderThickness := 0,$pillBorderThickness,$pillBorderThickness,$pillBorderThickness
        - BorderBrush := $pillBorderColor
    - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.Stack#MainStack > Grid#Content
      styles:
        - Height := $pillHeight
        - Padding := {{-$pillBorderThickness}}
        - Background := $pillFillColor
        - BorderThickness := 0,$pillBorderThickness,0,$pillBorderThickness
        - BorderBrush := $pillBorderColor
    - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.Stack#NonActivatableStack > Grid#Content
      styles:
        - Height := $pillHeight
        - Padding := {{-$pillBorderThickness}}
        - Background := $pillFillColor
        - BorderThickness := 0,$pillBorderThickness,0,$pillBorderThickness
        - BorderBrush := $pillBorderColor
    - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.NotificationAreaIcons#NotificationAreaIcons > ItemsPresenter > StackPanel
      styles:
        - Height := $pillHeight
        - Padding := {{-$pillBorderThickness}}
        - Background := $pillFillColor
        - BorderThickness := 0,$pillBorderThickness,0,$pillBorderThickness
        - BorderBrush := $pillBorderColor
    - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.Stack#NotifyIconStack > Grid#Content > SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter
      styles:
        - Height := $pillHeight
        - Padding := {{-$pillBorderThickness}}
        - Background := $pillFillColor
        - CornerRadius = $pillRadius,0,0,$pillRadius
        - BorderThickness := $pillBorderThickness,$pillBorderThickness,0,$pillBorderThickness
        - BorderBrush := $pillBorderColor
    - target: Grid#OverflowRootGrid > Border
      styles:
        - Shadow :=
    - target: ScrollViewer > ScrollContentPresenter > Border > Grid > Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton
      styles:
        - Margin = 0,0,20,0
    - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid[2] > Grid > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Border > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Grid > Border#LargeTicker2 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > TextBlock[1]
      styles:
        - ActualWidth => WeatherCondWidth
        - RenderTransform := <TranslateTransform X="0" Y="8" />
    - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid[2] > Grid > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Border > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Grid > Border#LargeTicker2 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > TextBlock[2]
      styles:
        - ActualWidth => WeatherTempWidth
        - RenderTransform := <TranslateTransform X="{{WeatherCondWidth+7}}" Y="-8" />
    - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid
      styles:
        - Width = {{WeatherTempWidth+WeatherCondWidth+50}}
        - HorizontalAlignment = 0
    - target: Grid#AugmentedEntryPointContentGrid
      styles:
        - Margin = 5,0,0,0
    - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
      styles:
        - Width = {{WeatherTempWidth+WeatherCondWidth+50}}
        - Height := $pillHeight
        - CornerRadius = $pillRadius
        - Margin = 10,0,5,0
        - Padding = 0
        - Background := $pillFillColor
        - BorderThickness := $pillBorderThickness
        - BorderBrush := $pillBorderColor
    - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement
      styles:
        - BorderThickness := $highlightBorderThickness
        - Margin = {{$highlightOffset}}
  themeResourceVariables:
    - AdaptivePillFill@Light =#FFFFFF
    - AdaptivePillFill@Dark =#0F1E1E1E
    - AdaptivePillBorder@Light =#FFFFFF
    - AdaptivePillBorder@Dark =#54464646
  ```
  </details>