# AdaptivePills theme for Windows 11 Taskbar Styler

**Author**: [Deen-0x](https://github.com/Deen-0x)

## Description
AdaptivePills. A sleek reinterpretation of the Windows 11 taskbar with a background that turns task buttons into small rounded adaptive pills that keep the native feel but breathe more.

The theme is very parameterized. You can tweak styleConstants easily to generate various designs/adjustments. Scroll to the bottom for more info. 

## Demo (27" Monitor | 1920x1080)

Dark Mode | Normal & Maximized Window

![Dark](Dark.png)

![DarkMaximized](DarkMaximized.png)

Light Mode | Normal & Maximized Window

![Light](Light.png)

![LightMaximized](LightMaximized.png)

## Notes
- Theme is designed on Windows 11 - 25H2 (OS Build 26200.8737)
- Tested on monitors: 1920x1080 (100% scaling) | 3840x2160 (250% scaling)
- Designed for both light and dark modes
- Designed to work with: Search - Hide | Task view - Off  | *Widgets - On | Taskbar alignment - Center | Show smaller taskbar buttons - Never

  <details>
  <summary>Click to expand to view Taskbar Windows Settings for similar results</summary>

  ![TaskbarSettings](TaskbarSettings.png)
  </details><br>
  
- *Widgets must be installed to enable the weather widget on the left. Download link in case it was removed:
   https://apps.microsoft.com/detail/9mssgkg348sp
  <details>
  <summary>Click to expand to view Widget Board Settings for similar results</summary>

  ![WidgetBoardSettings](WidgetBoardSettings.png)
  </details><br>
- The media player on the right of the weather widget is a separate Mod that is included in Recommended Mods - Optional.

<br>

## Required Windhawk Mods for similar results
To achieve similar results, install and configure the following Windhawk mods in addition to Taskbar Styler (click each to expand settings):

  <details>
  <summary>Taskbar Height and Icon Size.</summary>

  ```yaml
  TaskbarHeight: 31
  IconSize: 14
  TaskbarButtonWidth: 30
  IconSizeSmall: 14
  TaskbarButtonWidthSmall: 15
  ```
  </details><br>

  <details>
  <summary>Taskbar Labels for Windows 11 – for labels and control of taskbar buttons width. You may increase taskbarItemWidth value to achieve longer buttons.</summary>

  ```yaml
  mode: labelsWithCombining
  taskbarItemWidth: 0
  runningIndicatorStyle: fullWidth
  progressIndicatorStyle: sameAsRunningIndicatorStyle
  excludedPrograms:
    - ''
  minimumTaskbarItemWidth: 20
  maximumTaskbarItemWidth: 200
  fontSize: 12
  fontFamily: ''
  textTrimming: characterEllipsis
  leftAndRightPaddingSize: 0
  spaceBetweenIconAndLabel: 0
  runningIndicatorHeight: -1
  runningIndicatorVerticalOffset: 0
  alwaysShowThumbnailLabels: 0
  labelForSingleItem: ''
  labelForMultipleItems: ''

  ```
  </details><br>

  <details>
  <summary>Taskbar Clock Customization – for styling the clock.</summary>

  ```yaml
  ShowSeconds: 0
  TimeFormat: ''
  DateFormat: d/M/y
  DateLocale: ''
  WeekdayFormat: custom
  WeekdayFormatCustom: Sun, Mon, Tue, Wed, Thu, Fri, Sat
  TopLine: ''
  BottomLine: 📅  %date%  |  %time%
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
    DiskMetricsFormat: ''
    DiskMetricsFixedDecimals: 0
    PercentageFormat: spacePaddingAndSymbol
    UpdateInterval: 1
    NetworkAdapterName: ''
    GpuAdapterName: ''
  MediaPlayer:
    IgnoredPlayers:
      - ''
    MaxLength: 28
    MediaInfoFormat: ''
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
    LineHeight: 0
  DateStyle:
    Hidden: 0
    TextColor: ''
    TextAlignment: ''
    FontSize: 12
    FontFamily: Segoe UI Variable
    FontWeight: Medium
    FontStyle: Normal
    FontStretch: ''
    CharacterSpacing: 0
    LineHeight: 0
  oldTaskbarOnWin11: 0
  ```
  </details><br>

  <details>
  <summary>Dynamic Taskbar Transparency - to dynamically show taskbar background when a window is maximized.</summary>

  ```yaml
    desktop:
    style: clear
  fallback:
    style: captured
  maximized:
    enabled: 1
    style: fallback
  startOpened:
    enabled: 1
    style: fallback
  searchOpened:
    enabled: 1
    style: fallback
  taskViewOpened:
    enabled: 1
    style: fallback
  trayFlyoutOpened:
    enabled: 1
    style: fallback
  otherInteraction:
    enabled: 1
    style: fallback
  animation:
    durationMs: 220
  detection:
    fullscreenAsMaximized: 1
  ```
  </details><br>

  <details>
  <summary>Taskbar tray system icon tweaks - to set showDesktopButtonWidth and declutter the system tray icons.</summary>

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

## Recommended visual Windhawk Mods
To remove clipped flyout shadows, install and configure the following Windhawk mods (click each to expand settings):


  <details>
  <summary>Windows 11 Notification Center Styler.</summary>

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

  <details>
  <summary>Windows 11 Start Menu Styler.</summary>

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
  </details><br>

Set the media player:
  <details>
  <summary>Taskbar Fluent Media Player.</summary>

  ```yaml
MainSettings:
  PlayerSetting:
    position: taskbar_after_widgets_right
    playerWidth: 0 0
    playerHeight: 24 24
    playerMargin: '-55 5'
    mirrorLayout: 0
  AlbumArtSetting:
    showAlbumArt: 0
    albumArtWidth: 32 64
    albumArtHeight: 24 24
    albumArtMargin: 0 0
  TextAreaSetting:
    showTrackTitle: 0
    showTrackArtist: 0
    textAreaWidth: 0 60
    textAreaHeight: 0 0
    textAreaMargin: 5 5
    textSpacing: -1
    enableTitleScrolling: 1
    enableArtistScrolling: 0
    scrollSpeed: 1
    scrollPauseDuration: 1000
    scrollMode: bounce
    loopGap: 40
    swapTitleArtist: 0
    emptyTitleText: Untitled
    noMediaTitleText: Not Playing
    emptyArtistText: ''
    noMediaArtistText: ''
  MediaButtonsSettings:
    showMediaButtons: 1
    mediaButtons:
      - prev
      - play
      - next
    mediaButtonsMargin: 2 2
    buttonSize: 20
    hideUnsupportedButtons: 0
  VisualizerFunctionsSettings:
    vizEnabled: 1
    vizPosition: right
    vizShape: stereo
    vizEQ: default
    vizAnchor: middle
    vizBarCountGap: 7 4
    vizBarSize: 2 3
    vizPadding: 0 0
    vizSensitivity: 150
AppearanceSettings:
  BackgroundStyleSettings:
    backgroundType: none
    solidColor: 35 35 35
    solidColor2: 35 35 35
    gradientColor2: 128 128 128
    solidOpacity: 100
    gradientAngle: 50
    gradientBalance: 50
    acrylicTintOpacity: 50
    micaOpacity: 50
    blurOpacity: 65
    blurRadius: 11
    cornerRadius: '7'
    enablePlayerHoverEffect: 'off'
    enableMediaButtonsHoverEffect: auto
  MediaButtonsStyleSettings:
    iconStyle: fluent_outline
    buttonSpacing: 0
    buttonIconSize: 12
    buttonCornerRadius: '4'
    buttonColor: 0 0 0$255 255 255
    buttonColorOpacity: 100
  TitleTextStyleSettings:
    titleColor: 0 0 0$255 255 255
    titleColorOpacity: 100
    titleFont: segoe_ui_variable
    titleFontSize: 12
    titleFontFamily: ''
    titleFontWeight: ''
    titleFontStyle: ''
    titleCharacterSpacing: 0
  ArtistTextStyleSettings:
    artistColor: 0 0 0$255 255 255
    artistColorOpacity: 80
    artistFont: segoe_ui_variable
    artistFontSize: 11
    artistFontFamily: ''
    artistFontWeight: ''
    artistFontStyle: ''
    artistCharacterSpacing: 0
  AlbumArtDisplaySettings:
    albumArtEmptyBehavior: show
    emptyIconGlyph: E189
    emptyIconSize: 16
    emptyIconFont: segoe_fluent
    emptyIconColor: 140 140 140
    emptyIconOpacity: 100
    albumArtQuality: medium
    showPauseOverlay: 1
    pauseOverlayIconSize: 16
    pauseOverlayOpacity: 60
    albumArtOpacity: 100
    albumArtCornerRadius: '4'
    showAppIcon: 0
    appIconCorner: bottom_right
    appIconSize: 12
  VisualizerStyleSettings:
    vizColorMode: acrylic
    vizColor: 0 0 0$255 255 255
    vizColor1: 30 215 96
    vizColor2: 0 180 255
BehaviorSettings:
  disableAlbumArtClick: 0
  ClickActionSettings:
    - object: player
      click: left_click
      action: play_pause
    - object: player
      click: right_click
      action: open_context_menu
    - object: album_art
      click: left_double_click
      action: open_app
  MouseWheelActionSettings:
    - object: player
      click: mouse_wheel
      action: switch_tracks
    - object: album_art
      click: mouse_wheel
      action: switch_sessions
  hideWhenNoMedia: 0
  hideFullscreen: 1
  idleHideSeconds: 0
  showFullTitleOnHover: 1
AnimationSettings:
  enableSmoothPositionAnimation: 1
NotificationSettings:
  showSuccessNotification: 0
ContextMenuSettings:
  contextMenuItems:
    - repeat
    - shuffle
    - forward
    - rewind
    - next
    - prev
    - switch_sessions
    - open_app
  repeatStyle: submenu
  shuffleStyle: toggle
  showOpenWindhawk: 1
  contextMenuIconStyle: as_media_buttons
  contextMenuIconColor: 0 0 0$255 255 255
  contextMenuIconOpacity: 100
DebugSettings:
  ignoredProcesses: ''
  enableTreeDump: 0
  showDebugBorders: 0
  showLayoutAnchors: 0
  showRestartButton: 0
  ```
  </details>
  
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
  - taskbarLeftOffset = 10
  - taskbarRightOffset = 10
  - taskbarTopOffset = 5
  - taskbarBottomOffset = 4
  - buttonSpacing = 6
  - sysTraySpacing = 6
  - highlightOffset = 2
  - borderThickness = 1
  - highlightMinWidth = 38
  - buttonRadius = 7
  - highlightRadius = 6
  - iconLabelSpacing = 5
  - leftRightPadding = 5
  - multiWindowNotch = 4
  - badgeSize = 13
  - badgeNudge = 5,3,0,0
  - sysTrayIconSize = 15
  - taskbarSidesRounded = 1
  - fillColor = <WindhawkBlur BlurAmount="7" TintColor="{ThemeResource AdaptiveFill}" TintOpacity="0.2" TintLuminosityOpacity="0.2"/>
  - borderColor = <SolidColorBrush Color="{ThemeResource AdaptiveBorder}"/>
  - progressColor = <SolidColorBrush Color="{ThemeResource SystemAccentColor}" Opacity="0.2"/>
controlStyles:
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid > Taskbar.TaskbarFrame#TaskbarFrame
    styles:
      - Height =>TaskbarHeight
  - target: Taskbar.TaskListButton#TaskListButton > Taskbar.TaskListLabeledButtonPanel#IconPanel
    styles:
      - Padding := 2,0,2,0
      - MinWidth := $highlightMinWidth
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - Height := {{TaskbarHeight-($taskbarBottomOffset+$taskbarTopOffset)-2*$highlightOffset}}
      - Margin := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{$highlightOffset+2}},{{$taskbarBottomOffset-$highlightOffset}}
      - Margin@MultiWindowNormal := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{($highlightOffset+2)+$multiWindowNotch}},{{$taskbarBottomOffset-$highlightOffset}}
      - Margin@MultiWindowPointerOver := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{($highlightOffset+2)+$multiWindowNotch}},{{$taskbarBottomOffset-$highlightOffset}}
      - Margin@MultiWindowActive := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{($highlightOffset+2)+$multiWindowNotch}},{{$taskbarBottomOffset-$highlightOffset}}
      - Margin@MultiWindowPressed := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{($highlightOffset+2)+$multiWindowNotch}},{{$taskbarBottomOffset-$highlightOffset}}
      - Margin@RequestingAttentionMulti := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{($highlightOffset+2)+$multiWindowNotch}},{{$taskbarBottomOffset-$highlightOffset}}
      - Margin@RequestingAttentionMultiPointerOver := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{($highlightOffset+2)+$multiWindowNotch}},{{$taskbarBottomOffset-$highlightOffset}}
      - Margin@RequestingAttentionMultiPressed := {{$highlightOffset}},{{$taskbarTopOffset-$highlightOffset}},{{($highlightOffset+2)+$multiWindowNotch}},{{$taskbarBottomOffset-$highlightOffset}}
      - CornerRadius := $highlightRadius
      - BorderThickness = 0
      - VerticalAlignment = 1
      - Canvas.ZIndex = 2
  - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Rectangle#RunningIndicator
    styles:
      - Visibility = Visible
      - Height := {{TaskbarHeight-($taskbarBottomOffset+$taskbarTopOffset)}}
      - Margin = 0,{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - RadiusX := $buttonRadius
      - RadiusY := $buttonRadius
      - StrokeThickness := $borderThickness
      - VerticalAlignment = 1
      - Fill := $fillColor
      - Stroke := $borderColor
      - Canvas.ZIndex = -1
  - target: Microsoft.UI.Xaml.Controls.ProgressBar#ProgressIndicator
    styles:
      - Margin = 0,{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - Height := {{TaskbarHeight-($taskbarBottomOffset+$taskbarTopOffset)}}
  - target: Microsoft.UI.Xaml.Controls.ProgressBar#ProgressIndicator > Grid#LayoutRoot
    styles:
      - Background := $fillColor
      - BorderThickness := $borderThickness
      - BorderBrush := $borderColor
      - CornerRadius := $buttonRadius
  - target: Border#ProgressBarRoot > Border > Grid
    styles:
      - Height = Auto
  - target: Grid#LayoutRoot@CommonStates > Border#ProgressBarRoot > Border > Grid > Rectangle#ProgressBarTrack
    styles:
      - Fill = Transparent
  - target: Grid#LayoutRoot@CommonStates > Border#ProgressBarRoot > Border > Grid > Rectangle#DeterminateProgressBarIndicator
    styles:
      - RadiusX := $highlightRadius
      - RadiusY := $highlightRadius
      - Fill := $progressColor
      - Fill@Paused := <SolidColorBrush Color="orange" Opacity="0.2"/>
  - target: Grid#LayoutRoot@CommonStates > Border#ProgressBarRoot > Border > Grid > Rectangle#IndeterminateProgressBarIndicator
    styles:
      - RadiusX := $highlightRadius
      - RadiusY := $highlightRadius
      - Fill := $progressColor
      - Fill@Paused := <SolidColorBrush Color="orange" Opacity="0.2"/>
  - target: Grid#LayoutRoot@CommonStates > Border#ProgressBarRoot > Border > Grid > Rectangle#IndeterminateProgressBarIndicator2
    styles:
      - RadiusX := $highlightRadius
      - RadiusY := $highlightRadius
      - Fill := $progressColor
      - Fill@Paused := <SolidColorBrush Color="orange" Opacity="0.2"/>
  - target: Border#MultiWindowElement
    styles:
      - Visibility = Collapsed
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > TextBlock#LabelControl
    styles:
      - FontFamily = Segoe UI Variable
      - Margin := {{$iconLabelSpacing-6}},{{$taskbarTopOffset}},6,{{$taskbarBottomOffset+3}}
      - Padding := {{$leftRightPadding}},0
      - HorizontalAlignment = 1
      - VerticalAlignment = 1
      - Canvas.ZIndex = 3
  - target: Taskbar.TaskListButton#TaskListButton
    styles:
      - Margin := {{$buttonSpacing-6}},0,0,0
  - target: Taskbar.TaskListButton#TaskListButton > Taskbar.TaskListLabeledButtonPanel#IconPanel > Image#Icon
    styles:
      - Margin := 0,{{$taskbarTopOffset}},3,{{$taskbarBottomOffset}}
      - HorizontalAlignment = 2
      - Canvas.ZIndex = 3
  - target: Taskbar.TaskbarExtensionElement
    styles:
      - Visibility = Collapsed
  - target: Taskbar.ExperienceToggleButton#LaunchListButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Visibility = Collapsed
  - target: Taskbar.ExperienceToggleButton#LaunchListButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement
    styles:
      - CornerRadius := $buttonRadius
      - BorderThickness := $borderThickness
      - Background := $fillColor
      - BorderBrush := $borderColor
  - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Image#OverlayIcon
    styles:
      - Width := $badgeSize
      - Height := $badgeSize
      - Margin := $badgeNudge
      - Canvas.ZIndex = 3
  - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Taskbar.Badge#BadgeControl
    styles:
      - MinWidth := $badgeSize
      - Width := $badgeSize
      - Height := $badgeSize
      - Margin := $badgeNudge
      - Canvas.ZIndex = 3
  - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Taskbar.Badge#BadgeControl > Grid > TextBlock#BadgeText
    styles:
      - FontSize = 10
      - HorizontalAlignment = 1
  - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.OmniButton#NotificationCenterButton
    styles:
      - Margin := 0,0,{{$taskbarRightOffset-12}},0
  - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter#ContentPresenter > ItemsPresenter > StackPanel
    styles:
      - Padding = 4,0
  - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.OmniButton#NotificationCenterButton > Grid
    styles:
      - Margin := {{$sysTraySpacing}},{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - Padding := {{-$borderThickness}}
      - CornerRadius := {{$buttonRadius}},{{$buttonRadius*$taskbarSidesRounded}},{{$buttonRadius*$taskbarSidesRounded}},{{$buttonRadius}}
      - BorderThickness := $borderThickness
      - Background := $fillColor
      - BorderBrush := $borderColor
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > Border#BackgroundBorder
    styles:
      - Margin := {{$highlightOffset}}
      - CornerRadius := $highlightRadius
      - BorderThickness = 0
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - Margin := {{$highlightOffset}}
      - CornerRadius := $highlightRadius
      - BorderThickness = 0
  - target: SystemTray.ChevronIconView > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - Margin := {{$highlightOffset}}
      - CornerRadius := $highlightRadius
      - BorderThickness = 0
  - target: SystemTray.OmniButton#ControlCenterButton > Grid > Border#BackgroundBorder
    styles:
      - Margin := {{$highlightOffset}}
      - CornerRadius := $highlightRadius
      - BorderThickness = 0
  - target: SystemTray.NotifyIconView#NotifyItemIcon > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - Margin := {{$highlightOffset}}
      - CornerRadius := $highlightRadius
      - BorderThickness = 0
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter#ContentPresenter
    styles:
      - Margin = 0,0,0,1
  - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.OmniButton#ControlCenterButton > Grid
    styles:
      - Margin := 0,{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - Padding := {{-$borderThickness}}
      - CornerRadius := 0,$buttonRadius,$buttonRadius,0
      - BorderThickness := 0,$borderThickness,$borderThickness,$borderThickness
      - Background := $fillColor
      - BorderBrush := $borderColor
  - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.Stack#MainStack > Grid#Content
    styles:
      - Margin := 0,{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - Padding := {{-$borderThickness}}
      - BorderThickness := 0,$borderThickness,0,$borderThickness
      - Background := $fillColor
      - BorderBrush := $borderColor
  - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.Stack#NonActivatableStack > Grid#Content
    styles:
      - Margin := 0,{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - Padding := {{-$borderThickness}}
      - BorderThickness := 0,$borderThickness,0,$borderThickness
      - Background := $fillColor
      - BorderBrush := $borderColor
  - target: SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.NotificationAreaIcons#NotificationAreaIcons > ItemsPresenter > StackPanel
    styles:
      - Margin := 0,{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - Padding := {{-$borderThickness}}
      - BorderThickness := 0,$borderThickness,0,$borderThickness
      - Background := $fillColor
      - BorderBrush := $borderColor
  - target: SystemTray.Stack#NotifyIconStack > Grid#Content > SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter
    styles:
      - Margin := 0,{{$taskbarTopOffset}},0,{{$taskbarBottomOffset}}
      - Padding := {{-$borderThickness}}
      - BorderThickness := $borderThickness,$borderThickness,0,$borderThickness
      - Background := $fillColor
      - CornerRadius := $buttonRadius,0,0,$buttonRadius
      - BorderBrush := $borderColor
  - target: SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock
    styles:
      - FontSize := $sysTrayIconSize
  - target: SystemTray.ImageIconContent > Grid#ContainerGrid > Image
    styles:
      - Width := $sysTrayIconSize
      - Height := $sysTrayIconSize
  - target: SystemTray.AdaptiveTextBlock#LanguageInnerTextBlock > TextBlock#InnerTextBlock
    styles:
      - Margin = 0,0,0,3
      - MaxLines = 1
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > Grid#ContentGrid > SystemTray.DateTimeIconContent > Grid#ContainerGrid > StackPanel
    styles:
      - Margin = 0,0,0,3
  - target: Grid#OverflowRootGrid > Border
    styles:
      - Background := $fillColor
      - Shadow :=
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid > Grid > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Border > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Grid > Border#LargeTicker2 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > TextBlock[1]
    styles:
      - ActualWidth => WeatherTempWidth
      - RenderTransform := <TranslateTransform X="0" Y="8" />
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid > Grid > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Border > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Grid > Border#LargeTicker2 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > TextBlock[2]
    styles:
      - ActualWidth => WeatherCondWidth
      - RenderTransform := <TranslateTransform X="{{WeatherTempWidth+7}}" Y="-8" />
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid
    styles:
      - Width := {{WeatherCondWidth+WeatherTempWidth+53}}
      - HorizontalAlignment = 0
  - target: Grid#AugmentedEntryPointContentGrid
    styles:
      - Margin = 5,0,0,0
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Width := {{WeatherCondWidth+WeatherTempWidth+53}}
      - Height = Auto
      - Margin := {{$taskbarLeftOffset}},{{$taskbarTopOffset}},60,{{$taskbarBottomOffset}}
      - Padding = 0
      - CornerRadius := {{$buttonRadius*$taskbarSidesRounded}},{{$buttonRadius}},{{$buttonRadius}},{{$buttonRadius*$taskbarSidesRounded}}
      - BorderThickness := $borderThickness
      - Background := $fillColor
      - BorderBrush := $borderColor
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement
    styles:
      - CornerRadius := $highlightRadius
      - Margin := {{$highlightOffset}}
      - BorderThickness = 0
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid > Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid > Grid[1]
    styles:
      - HorizontalAlignment = 0
      - Margin = 3,0,0,0
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid > Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid > Grid[2]
    styles:
      - HorizontalAlignment = 0
      - VerticalAlignment = 0
      - RenderTransformOrigin = -0.5,0.5
      - RenderTransform := <TransformGroup><ScaleTransform ScaleX = "0.7" ScaleY = "0.7" /><TranslateTransform X="16" Y="0" /></TransformGroup>
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid
    styles:
      - Shadow :=
themeResourceVariables:
  - AdaptiveFill@Light =#FFFFFF
  - AdaptiveFill@Dark =#000000
  - AdaptiveBorder@Light =#75B4B4B4
  - AdaptiveBorder@Dark =#60454545
```
</details><br>

If you'd like to tweak styleConstants (located at the top of the theme content), you may use the styleConstants illustration below as a guide:

![styleConstantsIllustration](styleConstantsIllustration.png)