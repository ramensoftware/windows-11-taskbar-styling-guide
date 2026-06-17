# LiquidGlass theme for Windows 11 Taskbar Styler

**Author**: [mohsinhasanpc](https://github.com/mohsinhasanpc)

![Screenshot](screenshot.png)

> [!NOTE]
> This theme is made for dark mode. As such it may not display correctly if used on light themes.
> This was made on screen resolution of 1920x1440 pixels & 15'6 screen size.
> Windows OS version used for the mod - 26200.8655

## Taskbar Clock Customization (Optional)

The get the clock to show up like it does in the screenshot, follow these steps:

* Open the Taskbar Clock Customization mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
ShowSeconds: 1
TimeFormat: hh':'mm tt;hh':'mm':'ss tt
DateFormat: MM/dd;dddd - MMMM dd, yyyy
WeekdayFormat: dddd
WeekdayFormatCustom: Sun, Mon, Tue, Wed, Thu, Fri, Sat
TopLine: %time%
BottomLine: %date%
MiddleLine: '%weekday%'
TooltipLine: 📅 %date2%%n%🕒 %time2%%n%%n%🌐 %web1_full%%n%%n%📻 %media_info%
TooltipLineMode: replace
Width: 180
Height: 60
MaxWidth: 0
TextSpacing: 0
DataCollection:
  NetworkMetricsFormat: mbsDynamic
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
  RemoveBrackets: 1
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
  - ''
TimeStyle:
  Hidden: 0
  TextColor: ''
  TextAlignment: Center
  FontSize: 0
  FontFamily: ''
  FontWeight: ''
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
  CharacterSpacing: 0
oldTaskbarOnWin11: 0
```
</details>

## Taskbar Height and Icon Size

> [!NOTE]
> This is required for the taskbar and icons to have the correct size since this theme attempts to mimic the sizing of the macOS Dock. Attempting to do this directly makes it far too blurry.

The get the taskbar and icons sizes to show up like they do in the screenshot, follow these steps:

* Open the Taskbar Height and Icon Size mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
TaskbarHeight: 69
IconSize: 45
TaskbarButtonWidth: 57
IconSizeSmall: 16
TaskbarButtonWidthSmall: 32
```
</details>

## Theme selection

The theme is integrated into the mod and can simply be selected from the mod's
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
  - target: Taskbar.TaskbarFrame#TaskbarFrame
    styles:
      - Width=Auto
      - HorizontalAlignment=Center
      - MinWidth=100
      - MaxWidth={{max(containerGridWidth - 250, 100)}}
      - Grid.Column=1
  - target: Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid
    styles:
      - Padding=50,0,50,0
      - Margin=0,0,0,3
      - CornerRadius=Auto
      - Background=Transparent
      - HorizontalAlignment=Center
      - Width=Auto
      - BorderThickness=0
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=<WindhawkBlur BlurAmount="3" TintColor="#14090909"/>
      - RadiusX=33
      - RadiusY=33
      - StrokeThickness=1.2,1,1.2,1
      - Canvas.ZIndex=1
      - Margin=-50,0,-50,0
      - Stroke:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.1" /><GradientStop Color="#40404040" Offset="0.25" /><GradientStop Color="#40292929" Offset="0.5" /><GradientStop Color="#40404040" Offset="0.75" /><GradientStop Color="#50404040" Offset="0.9" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=<WindhawkBlur BlurAmount="4" TintColor="#1D101010"/>
      - RadiusX=35
      - RadiusY=35
      - Margin=
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundStroke
    styles:
      - Visibility=Visible
      - Stroke:=<WindhawkBlur BlurAmount="25" TintColor="#00000000"/>
      - StrokeThickness=6
      - RadiusX=36
      - RadiusY=35
      - Canvas.ZIndex=-1
      - VerticalAlignment=Stretch
      - HorizontalAlignment=Stretch
      - Height=NaN
      - Margin=-50,0,-50,0
      - Fill:=<WindhawkBlur BlurAmount="0" TintColor="#00101010"/>
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Background:=<WindhawkBlur BlurAmount="5" TintColor="#30101010"/>
      - CornerRadius=30.5
      - BorderThickness=1.2,1,1.2,1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.1" /><GradientStop Color="#60404040" Offset="0.25" /><GradientStop Color="#40292929" Offset="0.5" /><GradientStop Color="#90404040" Offset="0.75" /><GradientStop Color="#90404040" Offset="0.9" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
      - Padding=11,0,10,0
      - Margin=0,1,0,1
      - VerticalAlignment=Center
      - Height=60
  - target: SystemTray.SystemTrayFrame
    styles:
      - HorizontalAlignment=Left
      - Margin=50,0,0,0
      - Grid.Column=2
  - target: Taskbar.Gripper#GripperControl
    styles:
      - MinWidth=24
  - target: SystemTray.AdaptiveTextBlock#Base
    styles:
      - FontFamily=vivo Sans Global
      - FontWeight=Medium
      - FontSize=17.5
  - target: MenuFlyoutPresenter
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
      - CornerRadius=27
      - BorderThickness=0
  - target: MenuFlyoutPresenter > Border
    styles:
      - Background:=<WindhawkBlur BlurAmount="5" TintColor="#25131313"/>
      - BorderThickness=1,1,1,1
      - CornerRadius=32,32,30,30
      - Padding=5,9,6,9
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#59D3D3D3" Offset="0.0" /><GradientStop Color="#45494949" Offset="0.1" /><GradientStop Color="#50505050" Offset="0.5" /><GradientStop Color="#45494949" Offset="0.9" /><GradientStop Color="#50D3D3D3" Offset="1" /></LinearGradientBrush>
  - target: Grid#ConfirmatorMainGrid
    styles:
      - Background:=<WindhawkBlur BlurAmount="5" TintColor="#1C101010"/>
      - CornerRadius=34.5
      - BorderThickness=1,1,1,1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.15" /><GradientStop Color="#45404040" Offset="0.28" /><GradientStop Color="#55252525" Offset="0.5" /><GradientStop Color="#45404040" Offset="0.72" /><GradientStop Color="#50404040" Offset="0.85" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
      - RenderTransform:=<ScaleTransform ScaleX="1.12" ScaleY="1.15" />
      - Margin=7,0,13,155
      - MinHeight=53
      - MinWidth=180
      - Padding=9,2,9,1
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect
    styles:
      - Height=21
      - RadiusX=10.5
      - RadiusY=10.5
      - Fill:=<WindhawkBlur BlurAmount="18" TintColor="#35252525"/>
      - Stroke:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#809F9F9F" Offset="0.0" /><GradientStop Color="#10696969" Offset="0.5" /><GradientStop Color="#809F9F9F" Offset="1" /></LinearGradientBrush>
      - StrokeThickness=1
      - Margin=0.5
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalDecreaseRect
    styles:
      - Height=20
      - RadiusX=10
      - RadiusY=10
  - target: MenuFlyoutItem
    styles:
      - FontSize=14
      - FontWeight=Medium
  - target: MenuFlyoutSubItem
    styles:
      - FontSize=14
      - FontWeight=Medium
  - target: Border#OverflowFlyoutBackgroundBorder
    styles:
      - Background:=<WindhawkBlur BlurAmount="5" TintColor="#15101010"/>
      - BorderThickness=1
      - CornerRadius=27
      - Margin=-2,-2,-2,-2
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.15" /><GradientStop Color="#45404040" Offset="0.28" /><GradientStop Color="#55252525" Offset="0.5" /><GradientStop Color="#45404040" Offset="0.72" /><GradientStop Color="#50404040" Offset="0.85" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid
    styles:
      - Background:=<WindhawkBlur BlurAmount="5" TintColor="#1C101010"/>
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=<WindhawkBlur BlurAmount="5" TintColor="#15101010"/>
      - BorderThickness=1.2,1,1.2,1
      - CornerRadius=20
      - Padding=16,9,16,10
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#40404040" Offset="0.15" /><GradientStop Color="#40404040" Offset="0.28" /><GradientStop Color="#50252525" Offset="0.5" /><GradientStop Color="#40404040" Offset="0.72" /><GradientStop Color="#40404040" Offset="0.85" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
  - target: Windows.UI.Xaml.Controls.ToolTip
    styles:
      - CornerRadius=18
      - FontSize=14
      - FontWeight=Medium
  - target: Border#HoverFlyoutBackground
    styles:
      - Background:=<WindhawkBlur BlurAmount="0" TintColor="#1B242424"/>
      - BorderThickness=1
      - CornerRadius=35
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.15" /><GradientStop Color="#45404040" Offset="0.28" /><GradientStop Color="#55252525" Offset="0.5" /><GradientStop Color="#45404040" Offset="0.72" /><GradientStop Color="#50404040" Offset="0.85" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
  - target: ContentPresenter#HoverFlyoutContent
    styles:
      - CornerRadius=20
      - BorderThickness=0
      - Padding=4,0,4,4
      - Margin:=4,4,4,4.5
      - Background:=Transparent
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Grid#ModalRootGrid > Border#BackgroundElement
    styles:
      - CornerRadius=67.5
      - BorderThickness=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#69D3D3D3" Offset="0.0" /><GradientStop Color="#55494949" Offset="0.1" /><GradientStop Color="#60505050" Offset="0.5" /><GradientStop Color="#55494949" Offset="0.9" /><GradientStop Color="#69D3D3D3" Offset="1" /></LinearGradientBrush>
      - Background:=<WindhawkBlur BlurAmount="6" TintColor="#2C101010"/>
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid > Border
    styles:
      - CornerRadius=25,25,10,10
      - Background:=<WindhawkBlur BlurAmount="18" TintColor="#801F1F1F"/>
      - BorderThickness=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#69D3D3D3" Offset="0.0" /><GradientStop Color="#609F9F9F" Offset="0.1" /><GradientStop Color="#50707070" Offset="0.5" /><GradientStop Color="#50505050" Offset="0.9" /><GradientStop Color="#69404040" Offset="1" /></LinearGradientBrush>
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#VolumeIcon
    styles:
      - Width=20
      - Height=20
      - VerticalAlignment=Center
      - Margin=2,0,6,0
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#BrightnessIcon
    styles:
      - Width=21
      - Height=21
  - target: Windows.UI.Xaml.Controls.Border#SnapBarBorder
    styles:
      - Background:=<WindhawkBlur BlurAmount="9" TintColor="#1B242424"/>
      - BorderThickness=1.2,1,1.2,1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#60D3D3D3" Offset="0.0" /><GradientStop Color="#4F494949" Offset="0.1" /><GradientStop Color="#60505050" Offset="0.5" /><GradientStop Color="#4F494949" Offset="0.9" /><GradientStop Color="#60D3D3D3" Offset="1" /></LinearGradientBrush>
      - CornerRadius=27
      - Margin=-2,0,-2,0
  - target: SnapLayout.SnapLayoutPickerControl
    styles:
      - Background:=<WindhawkBlur BlurAmount="12" TintColor="#1B242424"/>
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50DDDDDD" Offset="0.0" /><GradientStop Color="#1C696969" Offset="0.28" /><GradientStop Color="#20696969" Offset="0.43" /><GradientStop Color="#20696969" Offset="0.58" /><GradientStop Color="#1C606060" Offset="0.75" /><GradientStop Color="#50C1C1C1" Offset="1" /></LinearGradientBrush>
      - BorderThickness=1
      - CornerRadius=10
  - target: SnapLayout.SnapLayoutControl
    styles:
      - Background:=<WindhawkBlur BlurAmount="12" TintColor="#15151515"/>
      - CornerRadius=10
      - BorderThickness=1
      - BorderBrush:=<SolidColorBrush Color="#50808080" />
  - target: SnapLayout.SnapLayoutControl@CommonStates > Windows.UI.Xaml.Controls.Border#LayoutBorder
    styles:
      - Background@PointerOver:=$ElementSysColor2
      - Background@Pressed:=$ElementSysColor3
  - target: Windows.UI.Xaml.Shapes.Rectangle#InvokeRect
    styles:
      - ''
  - target: Windows.UI.Xaml.Shapes.Rectangle#HintRect
    styles:
      - ''
  - target: Border#VirtualDesktopBarBackground
    styles:
      - Background:=<WindhawkBlur BlurAmount="8" TintColor="#6B242424"/>
      - BorderThickness=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50DDDDDD" Offset="0.0" /><GradientStop Color="#0C696969" Offset="0.28" /><GradientStop Color="#50C1C1C1" Offset="1" /></LinearGradientBrush>
      - Margin=45,-5,45,-2
      - CornerRadius=45
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed
    styles:
      - CornerRadius=12
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed
    styles:
      - CornerRadius=12
  - target: TextBlock#VirtualDesktopNameBlock
    styles:
      - Margin=12,8,0,5
      - FontSize=14
  - target: TextBox#VirtualDesktopCustomNameBlock
    styles:
      - Margin=10,10,10,5
      - FontSize=14
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed TextBlock
    styles:
      - Margin=10,10,0,5
      - FontSize=14
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundStroke
    styles:
      - Visibility=Visible
      - Stroke:=<WindhawkBlur BlurAmount="30" TintColor="#10303030"/>
      - StrokeThickness=5
      - RadiusX=30
      - RadiusY=32
      - Canvas.ZIndex=-1
      - VerticalAlignment=Stretch
      - HorizontalAlignment=Stretch
      - Height=NaN
      - Margin=0,1,0,0
      - Fill:=<WindhawkBlur BlurAmount="0" TintColor="#00101010"/>
  - target: ':root > ScrollViewer > ScrollContentPresenter > Border > Grid'
    styles:
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
      - ActualWidth=>containerGridWidth
      - HorizontalAlignment=Stretch
  - target: Taskbar.OverflowToggleButton
    styles:
      - MinWidth=60
      - Margin=5,0,5,0
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: SystemTray.ChevronIconView
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Visibility=1
  - target: ContentPresenter#ContentPresenter > Grid#ContentGrid > Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer#LottieIcon
    styles:
      - Visibility=1
  - target: SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[2] > SystemTray.IconView > Grid > Grid
    styles:
      - Visibility=1
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
    styles:
      - Visibility=1
  - target: SystemTray.NotificationAreaIcons#NotificationAreaIcons > ItemsPresenter
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: SystemTray.OmniButton#ControlCenterButton
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: SystemTray.OmniButton#NotificationCenterButton
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: SystemTray.DateTimeIconContent > Grid#ContainerGrid > StackPanel > TextBlock#TimeInnerTextBlock
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: SystemTray.DateTimeIconContent > Grid#ContainerGrid > StackPanel > TextBlock#DateInnerTextBlock
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: SystemTray.OmniButton#ControlCenterButton@CommonStates > Grid > Border#BackgroundBorder
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.BatteryIconContent
    styles:
      - Margin=2,0,0,0
      - RenderTransform:=<ScaleTransform ScaleX="1.15" ScaleY="1.15" />
      - RenderTransformOrigin=0.5,0.5
  - target: SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
    styles:
      - Margin=0,0,2,0
      - RenderTransform:=<ScaleTransform ScaleX="1.15" ScaleY="1.15" />
      - RenderTransformOrigin=0.5,0.5
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid > SystemTray.SystemTrayFrame > Grid#SystemTrayFrameGrid > SystemTray.Stack#NotifyIconStack > Grid#Content > SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.ChevronIconView > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock
    styles:
      - FontSize=19
      - Margin=2,0,0,0
  - target: SystemTray.OmniButton#NotificationCenterButton@CommonStates > Grid > Border#BackgroundBorder
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: SystemTray.ChevronIconView@CommonStates > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: SystemTray.ChevronIconView > * > TextBlock#InnerTextBlock
    styles:
      - Text:=&#xED14;
  - target: SystemTray.NotifyIconView@CommonStates > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
      - BorderBrush:=<SolidColorBrush Color="Transparent"/>
  - target: SystemTray.NotifyIconView@CommonStates > Grid > Border#BackgroundBorder
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
      - BorderBrush:=<SolidColorBrush Color="Transparent"/>
  - target: Windows.UI.Xaml.Controls.Button#CloseButton
    styles:
      - CornerRadius=15
      - Background:=<WindhawkBlur BlurAmount="15" TintColor="#2D101010"/>
      - BorderThickness=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#60404040" Offset="0.15" /><GradientStop Color="#55404040" Offset="0.28" /><GradientStop Color="#65252525" Offset="0.5" /><GradientStop Color="#55404040" Offset="0.72" /><GradientStop Color="#60404040" Offset="0.85" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
  - target: Taskbar.TaskItemThumbnailView@CommonStates > Grid > Border#BackgroundBorder
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: Taskbar.TaskItemThumbnailView@CommonStates > Border#BackgroundBorder
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: Border#ThumbnailVisualHostWrapper
    styles:
      - HorizontalAlignment=Center
      - VerticalAlignment=Center
  - target: Border#ThumbnailVisualHost
    styles:
      - CornerRadius=14
      - Background:=<SolidColorBrush Color="Transparent"/>
      - BorderThickness=1
      - BorderBrush:=<SolidColorBrush Color="Transparent"/>
  - target: Windows.UI.Xaml.Controls.Button#SwitchItemElementCloseButton
    styles:
      - CornerRadius=16
      - Padding=2.5
      - Margin=0,1,10,0
      - Background:=<WindhawkBlur BlurAmount="0" TintColor="#5D101010"/>
  - target: Windows.UI.Xaml.Controls.FlyoutPresenter
    styles:
      - RequestedTheme=Dark
      - Background:=<WindhawkBlur BlurAmount="8" TintColor="#2D101010"/>
      - BorderThickness=1.2,1,1.2,1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#70D3D3D3" Offset="0.0" /><GradientStop Color="#60404040" Offset="0.15" /><GradientStop Color="#55404040" Offset="0.28" /><GradientStop Color="#65252525" Offset="0.5" /><GradientStop Color="#55404040" Offset="0.72" /><GradientStop Color="#60404040" Offset="0.85" /><GradientStop Color="#70C1C1C1" Offset="1" /></LinearGradientBrush>
      - CornerRadius=33
      - Padding=2,3,2,3
  - target: Windows.UI.Xaml.Controls.Border#SnapPickerBorder
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
      - BorderThickness=0
      - Margin=0
  - target: Windows.UI.Xaml.Controls.Border#LayoutBorder
    styles:
      - Background:=<WindhawkBlur BlurAmount="15" TintColor="#30505050"/>
      - BorderThickness=1
      - BorderBrush:=<SolidColorBrush Color="#50FFFFFF"/>
      - CornerRadius=12
  - target: SnapLayout.SnapLayoutControl#SuggestionSnapLayout Windows.UI.Xaml.Controls.Border#LayoutBorder
    styles:
      - Background:=Transparent
  - target: Windows.UI.Xaml.Controls.Grid#LayoutGrid > Windows.UI.Xaml.Controls.Button
    styles:
      - BorderBrush:=<SolidColorBrush Color="#70BBBBBB"/>
      - BorderThickness=1
      - CornerRadius=9.5
      - Margin=1.5
  - target: Windows.UI.Xaml.Controls.Grid#LayoutGrid > Windows.UI.Xaml.Controls.Button@CommonStates > Windows.UI.Xaml.Controls.Grid#RootGrid
    styles:
      - Background@PointerOver:=<SolidColorBrush Color="#40FFFFFF"/>
      - Background@Pressed:=<SolidColorBrush Color="#20FFFFFF"/>
  - target: Windows.UI.Xaml.Controls.Button#WindowGroupSuggestionButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - Background:=Transparent
  - target: Windows.UI.Xaml.Controls.Button#WindowGroupSuggestionButton@CommonStates > Windows.UI.Xaml.Controls.Grid#RootGrid
    styles:
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark2}" Opacity="1" />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark2}" Opacity="1" />
```
</details>