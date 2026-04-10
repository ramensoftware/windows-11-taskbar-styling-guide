# LayerMicaUI theme for Windows 11 Taskbar Styler

LayerMicaUI is a modern Windows 11 taskbar theme with clean visuals and comprehensive styling.

**Author**: [Nimai-HK](https://github.com/Nimai-HK)

![TaskbarTheme](screenshot.png)

## Theme Specification
- Designed for Windows 11 25H2.
- Fully compatible with both Light and Dark modes.
- Optimized for a left-aligned taskbar only.
- Requires widgets on the taskbar to be disabled.
- Note: Clock styles and Taskbar Labels are an additional customisation, please refer to [Additional Configuration](#additional-configuration)

## Features
This theme also styles additional parts of Windows 11 for both Light and Dark modes.

- **Context Menus, Volume and Brightness HUD, Bluetooth and USB icons, Hover Flyouts, Window Snap Layouts, Taskbar Hidden Icons Tray**

  ![Features Grid](features-grid.png)

- **Task View and Alt Tab Window Switcher**

  ![View Grid](views-grid.png)

---
## Additional Configuration
To make the taskbar look better, follow these settings:

<details>
  <summary>Taskbar Layer Border (Click to expand)</summary>

- This border was originally styled by the theme.
- It was removed because applying a Border Style interfered with the Windows 11 taskbar’s click‑to‑minimize window behavior.
- Does not affect the focusing or maximizing window behaviour.
- If you don’t use that action or aren’t affected, you can re‑enable it by placing these styles under "Control Styles" Section in the "Windows 11 Taskbar Styler" mod settings.

  ```yaml
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - BorderBrush:=$ThemeOutBorder

  - target: Grid#SystemTrayFrameGrid
    styles:
      - BorderBrush:=$ThemeOutBorder
  ```
</details>

<details>
  <summary>Taskbar Search Bar Active States (Click to expand)</summary>

- Currently, the search bar active states are controlled by SearchHost.exe, which can be customized by the "Windows 11 Start Menu Styler" mod.
- Paste these styles under "Control Styles" Section in the "Windows 11 Start Menu Styler" Mod settings.

    ```yaml
    - target: Border#TaskbarSearchBackground
      styles:
        - CornerRadius=$InnerRadius
        - Background:=$ThemeOverlay
        - BorderThickness=0
        - Height=32
        - Transform3D:=<CompositeTransform3D TranslateY="-2" TranslateX="1"/>

    - target: Cortana.UI.Views.RichSearchBoxControl#SearchBoxControl > Grid#RootGrid
      styles:
        - CornerRadius=$InnerRadius
        - Transform3D:=<CompositeTransform3D TranslateY="-2" TranslateX="1"/>
    ```

</details>

<details>
  <summary>Font Customisation (Click to expand)</summary>

- Font to be installed: [Nunito](https://fonts.google.com/specimen/Nunito)
- Add these items to the "Style Constants" section of the settings page of the "Windows 11 Taskbar Styler" mod
    ```
  ThFntWt=Semibold
    ```
</details>

<details>
  <summary>Taskbar height and icon size (Click to expand)</summary>

- Open the "Taskbar Height and Icon Size" mod, go to the "Settings" tab, select "Textual mode" and paste the content below:

  ```yaml
  TaskbarHeight: 52
  IconSize: 24
  TaskbarButtonWidth: 42
  IconSizeSmall: 0
  TaskbarButtonWidthSmall: 30
  ```
</details>

<details>
  <summary>Taskbar Clock Customization (Click to expand)</summary>

- Open the "Taskbar Clock Customization" mod, go to the "Settings" tab, select "Textual mode" and paste the content below:

  ```yaml
  ShowSeconds: 0
  TimeFormat: 'HH'' : ''mm;HH'' : ''mm'
  DateFormat: ''' | '' ddd • MMM dd • yyyy;MMMM dd '' | '' yyyy;dddd'
  WeekdayFormat: dddd
  WeekdayFormatCustom: Sun, Mon, Tue, Wed, Thu, Fri, Sat
  TopLine: '%time% %date%'
  BottomLine: '%date%'
  MiddleLine: '%weekday%'
  TooltipLine: '%time2%  |  %date3%%n%%date2%%n%%n%%media_info%%n%%n%CPU:    %cpu%      |      GPU:  %gpu%%n%RAM:   %ram%      |      BAT:   %battery%%n%NET:    %upload_speed%  △   %download_speed%  ▼%n%DISK:   %disk_read%  ○   %disk_write%  ◉'
  TooltipLineMode: replace
  Width: 180
  Height: 60
  MaxWidth: 0
  TextSpacing: -1
  DataCollection:
    NetworkMetricsFormat: mbits
    NetworkMetricsFixedDecimals: 1
    PercentageFormat: spacePaddingAndSymbol
    UpdateInterval: 1
    NetworkAdapterName: ''
    GpuAdapterName: ''
  MediaPlayer:
    IgnoredPlayers:
      - ''
    MaxLength: 38
    NoMediaText: '- no media playing -'
    RemoveBrackets: 0
  WebContentWeatherLocation: ''
  WebContentWeatherFormat: '%c 🌡️%t 🌬️%w'
  WebContentWeatherUnits: autoDetect
  WebContentsItems:
    - Url: ''
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
    - ''
  TimeStyle:
    Hidden: 0
    TextColor: ''
    TextAlignment: Center
    FontSize: 14
    FontFamily: Nunito
    FontWeight: Bold
    FontStyle: ''
    FontStretch: ''
    CharacterSpacing: 0
  DateStyle:
    Hidden: 1
    TextColor: ''
    TextAlignment: Center
    FontSize: 0
    FontFamily: ''
    FontWeight: ''
    FontStyle: ''
    FontStretch: ''
    CharacterSpacing: 30
  oldTaskbarOnWin11: 0
  ```

  ![Clock Customisation](clock-customisation.png)

</details>

<details>
  <summary>Taskbar Labels for Windows 11 (Click to expand)</summary>

- Open the "Taskbar Labels for Windows 11" mod, go to the "Settings" tab, select "Textual mode" and paste the content below:

  ```yaml
  mode: labelsWithCombining
  taskbarItemWidth: 0
  runningIndicatorStyle: centerDynamic
  progressIndicatorStyle: fullWidth
  excludedPrograms:
    - ''
  minimumTaskbarItemWidth: 100
  maximumTaskbarItemWidth: 180
  fontSize: 12
  fontFamily: Nunito Bold
  textTrimming: clip
  leftAndRightPaddingSize: 5
  spaceBetweenIconAndLabel: 8
  runningIndicatorHeight: 3
  runningIndicatorVerticalOffset: 3
  alwaysShowThumbnailLabels: 0
  labelForSingleItem: ''
  labelForMultipleItems: ''
  ```
</details>

## Other LayerMicaUI Themes
- [LayerMicaUI Start Menu Theme](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/LayerMicaUI)

- [LayerMicaUI Notification And Control Center Theme](https://github.com/ramensoftware/windows-11-notification-center-styling-guide/tree/main/Themes/LayerMicaUI)

---

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
  - ThemeBlur=<WindhawkBlur BlurAmount="12" TintColor="{ThemeResource SystemChromeMediumColor}" TintSaturation="1.25" NoiseOpacity="0.1" NoiseDensity="0.8" TintOpacity="0.2" TintLuminosityOpacity="0.3" />
  - ThemeLayer=<AcrylicBrush BackgroundSource="Backdrop" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="{ThemeResource bgOpacity}" TintLuminosityOpacity="{ThemeResource bgLuminosity}" FallbackColor="{ThemeResource SystemChromeMediumColor}" />
  - OuterRadius=10
  - InnerRadius=8
  - ThemeBorder=<SolidColorBrush Color="{ThemeResource Border}"/>
  - ThFnt=Nunito
  - ThemeOutBorder=<SolidColorBrush Color="#56757575"/>
  - ThemeOverlay=<SolidColorBrush Color="{ThemeResource Overlay}" />
  - ThemeIsland=<SolidColorBrush Color="{ThemeResource Island}" />
  - ThemeControlBorder=<SolidColorBrush Color="{ThemeResource ControlBorder}" />
  - ThFntWt=Normal
  - ThemeFlyout=<AcrylicBrush BackgroundSource="Backdrop" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.1" TintLuminosityOpacity="0.8" FallbackColor="{ThemeResource SystemChromeMediumColor}" />
controlStyles:
  - target: Border#BackgroundDimmingLayer
    styles:
      - Background:=$ThemeBlur
      - // Win + tab View > Background
  - target: Border#OverflowFlyoutBackgroundBorder
    styles:
      - Background:=$ThemeLayer
      - CornerRadius=$OuterRadius
      - BorderBrush:=$ThemeOutBorder
      - BorderThickness=1
      - // Taskbar Tray Hidden List > Background
  - target: Border#VirtualDesktopBarBackground
    styles:
      - Background:=$ThemeLayer
      - CornerRadius=$OuterRadius
      - BorderBrush:=$ThemeOutBorder
      - // Win + tab View > Virtual Desktops List Background
  - target: Border#SnapPickerBorder
    styles:
      - Background:=$ThemeBlur
      - // Window Snapping Arrangement Picker ( Hover on Maximize/Minimize button )
  - target: Border#SnapBarBorder
    styles:
      - Background:=$ThemeBlur
      - // Window Snapping Arrangement Window ( Move Window to Top of screen )
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Background:=$ThemeLayer
      - CornerRadius=$OuterRadius
      - Margin=0,3,8,3
      - Padding=4,0,0,0
      - BorderThickness=1
      - // BorderBrush:=$ThemeOutBorder
      - // Taskbar System Tray (Right Region) Grid > Background
  - target: Grid#ModalRootGrid > Border#BackgroundElement
    styles:
      - Background:=$ThemeBlur
      - CornerRadius=$OuterRadius
      - BorderBrush:=$ThemeOutBorder
      - // Alt + Tab View Background
  - target: Grid#ConfirmatorMainGrid
    styles:
      - Background:=$ThemeLayer
      - CornerRadius=$OuterRadius
      - BorderThickness=1
      - BorderBrush:=$ThemeOutBorder
      - Height=46
      - // Brightness/Volume Popup Background
  - target: Grid#HorizontalTemplate > Rectangle#HorizontalDecreaseRect
    styles:
      - Height=7.5
      - RadiusX=3
      - RadiusY=3
      - // Brightness/Volume Popup > Increasing/decreasing slider
  - target: Grid#HorizontalTemplate > Rectangle#HorizontalTrackRect
    styles:
      - Height=7.5
      - RadiusX=3
      - RadiusY=3
      - Opacity=0.5
      - // Brightness/Volume Popup > Slider Track (Background)
  - target: Grid#VolumeConfirmator > Slider#volumeSlider
    styles:
      - Margin=0,-3.5,0,0
      - Width=120
      - // Volume Popup > Slider Region Grid
  - target: Grid#BrightnessConfirmator > Slider#brightnessSlider
    styles:
      - Width=135
      - Margin=0,-2.5,0,0
      - // Brightness Popup > Slider Region Grid
  - target: Grid#OverflowRootGrid > Border
    styles:
      - //Background:=$ThemeLayer
      - //CornerRadius:=$OuterRadius
      - //BorderThickness=1
      - //BorderBrush:=$ThemeOutBorder
      - // Taskbar Overflow when full > Background
  - target: Grid#DynamicSearchBoxGleamContainer
    styles:
      - Height=30
      - // Taskbar Search Box > Art container beside search
  - target: Grid > HyperlinkButton#Footer
    styles:
      - HorizontalContentAlignment=1
      - // IDR what this was for
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#BrightnessIcon
    styles:
      - Height=22
      - Width=22
      - // Brightness Popup > Icon
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#VolumeIcon
    styles:
      - Height=18
      - Width=18
      - // Volume Popup > Icon
  - target: SystemTray.NotifyIconView#NotifyItemIcon[AutomationProperties.Name=Bluetooth Devices] > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.ImageIconContent > Grid#ContainerGrid > Image
    styles:
      - Visibility=1
      - // Default Bluetooth Icon on taskbar
  - target: SystemTray.NotifyIconView#NotifyItemIcon[AutomationProperties.Name=Safely Remove Hardware and Eject Media] > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.ImageIconContent > Grid#ContainerGrid > Image
    styles:
      - Visibility=1
      - // Default Plugged in device/USB Indicator Icon on taskbar
  - target: SystemTray.NotifyIconView#NotifyItemIcon[AutomationProperties.Name=Bluetooth Devices] > Grid#ContainerGrid > ContentPresenter#ContentPresenter
    styles:
      - Content:=<FontIcon FontFamily="Segoe Fluent Icons" Glyph="&#xE702;" FontSize="16"/>
      - Foreground:=<SolidColorBrush Color="{ThemeResource Accent1}" />
      - Canvas.ZIndex=-1
      - // New (Themed) Bluetooth Icon on taskbar
  - target: SystemTray.NotifyIconView#NotifyItemIcon[AutomationProperties.Name=Safely Remove Hardware and Eject Media] > Grid#ContainerGrid > ContentPresenter#ContentPresenter
    styles:
      - Content:=<FontIcon FontFamily="Segoe Fluent Icons" Glyph="&#xE88E;" FontSize="16"/>
      - Foreground:=<SolidColorBrush Color="{ThemeResource Accent1}" />
      - Canvas.ZIndex=-1
      - // New (Themed) Plugged in device/USB Indicator Icon on taskbar
  - target: SystemTray.OmniButton#ControlCenterButton
    styles:
      - Grid.Column=4
      - CornerRadius=$InnerRadius
      - // System Tray > Control Center Button
  - target: SystemTray.OmniButton#NotificationCenterButton
    styles:
      - Grid.Column=5
      - CornerRadius=$InnerRadius
      - // System Tray > Notification Center Button
  - target: SystemTray.Stack#MainStack
    styles:
      - Grid.Column=6
      - CornerRadius=$InnerRadius
      - // System tray > Microphone and Location Icons Grid
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - CornerRadius=$InnerRadius
      - Grid.Column=7
      - Width=5
      - // System Tray > Show Desktop Button
  - target: SystemTray.Stack#NonActivatableStack
    styles:
      - Grid.Column=2
      - // System Tray > Taskbar Additional Buttons Grid (Touch keyboard, Emoji Buttons)
  - target: Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=TaskViewButton] > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - CornerRadius=$InnerRadius
      - Width=44
      - // Task View Button Background
  - target: Taskbar.TaskItemThumbnailView > Grid > Border
    styles:
      - CornerRadius=$OuterRadius
      - Background:=$ThemeLayer
      - BorderThickness=1
      - BorderBrush:=$ThemeOutBorder
      - // Task View > Hover Over Popup Preview > Background
  - target: Taskbar.TaskItemThumbnailView > Grid > TextBlock#DisplayNameTextBlock
    styles:
      - FontFamily=$ThFnt
      - FontWeight=Bold
      - // Task View > Hover Over Popup Preview > TextBlocks for Desktop Names
  - target: Taskbar.TaskListButton
    styles:
      - CornerRadius=$InnerRadius
      - Margin=0,-1,0,-1
      - BorderBrush:=$ThemeControlBorder
      - BorderThickness=1
      - // Taskbar Buttons > Main List buttons > Button Background
  - target: Taskbar.TaskbarBackground#BackgroundControl
    styles:
      - Opacity=0
      - // Default Taskbar Background
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill
    styles:
      - CornerRadius=$OuterRadius
      - // Taskbar Task list > Hover Over Window Thumbnails Region > Background
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl
    styles:
      - FontFamily=$ThFnt
      - // Taskbar Task list > Hover Over Window Thumbnails Region > Thumbnail Window Names Textblock
  - target: Taskbar.TaskbarFrame
    styles:
      - Width=Auto
      - // Taskbar Task Region Frame(Task list + search area + Start button Region grid)
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Margin=8,3,0,3
      - CornerRadius=$OuterRadius
      - Padding=-8,0,0,0
      - Background:=$ThemeLayer
      - BorderThickness=1
      - HorizontalAlignment=Left
      - // BorderBrush:=$ThemeOutBorder
      - // Taskbar Task Region Frame(Task list + search area + Start button Region grid) > Background
  - target: TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
      - // System Tray Hidden Icons Button TextBlock
  - target: TextBlock#volumeLevelText
    styles:
      - FontSize=15
      - Margin=0,-1,0,0
      - FontFamily=$ThFnt
      - FontWeight=$ThFntWt
      - // Volume Popup > Volume Level Text
  - target: TextBlock#BatteryTextBlock
    styles:
      - FontFamily=$ThFnt
      - FontSize=12
      - FontWeight=Bold
      - // New 25H2 Battery Level TextBlock
  - target: ToolTip > ContentPresenter#LayoutRoot
    styles:
      - Background:=$ThemeFlyout
      - CornerRadius=$OuterRadius
      - BorderBrush:=$ThemeOutBorder
      - BorderThickness=1
      - // Hover popups/tooltips > Background
  - target: ToolTip > ContentPresenter#LayoutRoot > TextBlock
    styles:
      - FontFamily=$ThFnt
      - FontWeight=$ThFntWt
      - FontSize=13
      - // Hover popups/tooltips > TextBlock
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed#NewVirtualDesktopButtonThemed > Grid#MainGrid > Border#MainBorder
    styles:
      - CornerRadius=$OuterRadius
      - Background:=$ThemeOverlay
      - // Virtual Desktops > Add new Desktop Button > Main Background
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed#NewVirtualDesktopButtonThemed > Grid#MainGrid > Border#BorderHighlight
    styles:
      - CornerRadius=$OuterRadius
      - // Virtual Desktops > Add new Desktop Button > Highlight Background
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > Grid#TitleGrid > Border#BackgroundBorder
    styles:
      - CornerRadius=$OuterRadius,$OuterRadius,0,0
      - // Window Title Background in Win + Tab View
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > Grid#TitleGrid
    styles:
      - FontFamily=$ThFnt
      - FontWeight=$ThFntWt
      - // Window Title Grid in Win + Tab View
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root > Border#BackgroundBorder
    styles:
      - CornerRadius=$OuterRadius
      - Background:=$ThemeLayer
      - BorderBrush:=$ThemeControlBorder
      - BorderThickness=1
      - // Window Grid Background in Win + Tab View
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Grid#MainGrid > Border#MainBorder
    styles:
      - CornerRadius=$OuterRadius
      - Background:=$ThemeOverlay
      - // Virtual Desktops Background
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Grid#MainGrid > Border#BorderHighlight
    styles:
      - CornerRadius=$OuterRadius
      - // Virtual Desktops Background Highlight
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Grid#MainGrid > Border#ActiveDesktopPill
    styles:
      - CornerRadius=$OuterRadius
      - // Virtual Desktops > Active Desktop Highlight
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid
    styles:
      - Background:=$ThemeLayer
      - BorderBrush:=$ThemeOutBorder
      - Shadow:=
      - CornerRadius=$OuterRadius
      - // Win + Space Input Language Switcher Bar Background
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid#OverlayPanel
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - // Win + Space Input Language Switcher Bar Background ( Overlaid Background )
  - target: Button#GleamEntryPointButton > Border
    styles:
      - Height=30
      - // Taskbar Search Bar >  Art container beside search > Button background
  - target: ContentPresenter > SearchUx.SearchUI.SearchButtonControl > Grid > SearchUx.SearchUI.SearchBoxButton#SearchBox > SearchUx.SearchUI.SearchButtonRootGrid#SearchBoxButtonRootPanel > TextBlock#SearchBoxTextBlock
    styles:
      - FontFamily=$ThFnt
      - FontWeight=$ThFntWt
      - FontSize=14
      - RenderTransform:=<TranslateTransform Y="1" />
      - // Taskbar Search Bar > TextBlock
  - target: MenuFlyoutPresenter
    styles:
      - Background:=$ThemeFlyout
      - CornerRadius=$OuterRadius
      - FontFamily=$ThFnt
      - FontWeight=$ThFntWt
      - BorderThickness=1
      - BorderBrush:=$ThemeOutBorder
      - // Menu Flyouts Root (Background + TextBlock Styles)
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Margin=0,0,2,0
      - // IDR what this was for
  - target: Rectangle#BackgroundStroke
    styles:
      - Visibility=1
      - // Thin Line running along the top of the Taskbar (edge)
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid
    styles:
      - Background:=<WindhawkBlur BlurAmount="5" TintColor="{ThemeResource SystemChromeMediumColor}" TintSaturation="2" NoiseOpacity="0.19" NoiseDensity="0.8" TintOpacity="0.2" TintLuminosityOpacity="0" />
      - // Taskbar Root > Base Presenter > Base Grid (Usually transparent, Styled by this theme)
  - target: SearchUx.SearchUI.SearchBoxButton#SearchBox
    styles:
      - Margin=0,-1,0,0
      - // Taskbar Search Bar Button
  - target: SearchUx.SearchUI.SearchButtonRootGrid@CommonStates > Border#BackgroundElement
    styles:
      - Background:=$ThemeIsland
      - BorderBrush:=$ThemeOutBorder
      - BorderThickness=1
      - CornerRadius=$InnerRadius
      - Margin=0,-2.5,0,-2.5
      - // Taskbar Search Bar Button > Background
  - target: SearchUx.SearchUI.SearchPillButton#SearchPill > SearchUx.SearchUI.SearchButtonRootGrid#SearchBoxButtonRootPanel > Border#SearchPillBackgroundElement
    styles:
      - CornerRadius=$InnerRadius
      - Height=26
      - BorderBrush:=$ThemeBorder
      - Background:=$ThemeOverlay
      - // Taskbar Search Button (Pill Shaped search) > Background
  - target: SystemTray.NotificationAreaIcons#NotificationAreaIcons
    styles:
      - Grid.Column=1
      - CornerRadius=$InnerRadius
      - // Apps Pinned to system tray + Bluetooth and Usb Grid
  - target: SystemTray.SystemTrayFrame
    styles:
      - HorizontalAlignment=Right
      - // System Tray Root Frame (Right Region of the taskbar )
  - target: Windows.UI.Xaml.Hosting.DesktopWindowXamlSource
    styles:
      - Background:=$ThemeBlur
      - CornerRadius=$OuterRadius
      - BorderBrush:=$ThemeOutBorder
      - // Alt Tab View Background
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement > Grid#GridElement > Border#VirtualDesktopSwitcherBackground
    styles:
      - Background:=$ThemeLayer
      - // Virtual Desktop Switcher Bar Background
themeResourceVariables:
  - Accent1@Dark={ThemeResource SystemAccentColorLight3}
  - Accent1@Light={ThemeResource SystemAccentColorDark2}
  - bgOpacity@Dark=0.3
  - bgOpacity@Light=0.2
  - bgLuminosity@Light=1
  - bgLuminosity@Dark=0.9
  - Overlay@Light=#40FFFFFF
  - Overlay@Dark=#09FFFFFF
  - Border@Light=#0F000000
  - Border@Dark=#19000000
  - ControlBorder@Light=#0F000000
  - ControlBorder@Dark=#15FFFFFF
  - Island@Light=#5FFFFFFF
  - Island@Dark=#10FFFFFF
```
</details>
