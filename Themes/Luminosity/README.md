# Luminosity theme for Windows 11 Taskbar Styler

**Author**: [mendes.image](https://github.com/mendesimage)

![Demonstration](dock.png)

## Intro
**Luminosity** is based on native Acrylic, using the maximum **TintLuminosityOpacity** value as its backdrop.

It's meant to be used with **Mica** or **MicaAlt** backdrops, with or without the **Translucent Windows** mod.

---

## Options

### Dock

![Dock](dock.png)

- Docks are cool.


### Classic

![Classic](classic.png)

- Meant to cause minimal disruption for users who prefer the classic Taskbar placement.


### Compact
![Compact](compact.png)

- It's meant to be used with **Taskbar Labels for Windows 11**, using the **Centered Running Indicator** style, and **Taskbar Clock Customization**. Otherwise you will experience visual issues.


**Mods Guide**
To apply the same settings as mine, follow these steps:

* Open the **Taskbar Labels for Windows 11** and **Taskbar Clock Customization** mods in Windhawk.
* Go to the "Advanced" tab.
* Copy the content below to the text box under "Mod settings" and click "Save".

**Taskbar Labels for Windows 11**
<details>
<summary>Click to expand JSON content</summary>

```json
{
  "mode":"labelsWithoutCombining",
  "taskbarItemWidth":0,
  "runningIndicatorStyle":"centerDynamic",
  "progressIndicatorStyle":"centerDynamic",
  "excludedPrograms[0]":"excluded1.exe",
  "minimumTaskbarItemWidth":50,
  "maximumTaskbarItemWidth":176,
  "fontSize":12,
  "fontFamily":"",
  "textTrimming":"characterEllipsis",
  "leftAndRightPaddingSize":8,
  "spaceBetweenIconAndLabel":8,
  "runningIndicatorHeight":0,
  "runningIndicatorVerticalOffset":0,
  "alwaysShowThumbnailLabels":0,
  "labelForSingleItem":"%name%",
  "labelForMultipleItems":"[%amount%] %name%"
}
```

</details>


**Taskbar Clock Customization**
<details>
<summary>Click to expand JSON content</summary>

```json
{
  "ShowSeconds":1,
  "TimeFormat":"",
  "DateFormat":"",
  "WeekdayFormat":"dddd",
  "WeekdayFormatCustom":"Sun, Mon, Tue, Wed, Thu, Fri, Sat",
  "TopLine":"%date%   %time%","BottomLine":"",
  "MiddleLine":"%weekday%",
  "TooltipLine":"",
  "Width":180,"Height":60,"MaxWidth":0,"TextSpacing":0,"WebContentsItems[0].Url":"https://rss.nytimes.com/services/xml/rss/nyt/World.xml",
  "WebContentsItems[0].BlockStart":"<item>",
  "WebContentsItems[0].Start":"<title>",
  "WebContentsItems[0].End":"</title>",
  "WebContentsItems[0].MaxLength":28,"WebContentsUpdateInterval":10,"TimeZones[0]":"Eastern Standard Time",
  "TimeStyle.Hidden":0,"TimeStyle.TextColor":"",
  "TimeStyle.TextAlignment":"",
  "TimeStyle.FontSize":0,"TimeStyle.FontFamily":"",
  "TimeStyle.FontWeight":"",
  "TimeStyle.FontStyle":"",
  "TimeStyle.FontStretch":"",
  "TimeStyle.CharacterSpacing":0,"DateStyle.Hidden":1,"DateStyle.TextColor":"",
  "DateStyle.TextAlignment":"",
  "DateStyle.FontSize":0,"DateStyle.FontFamily":"",
  "DateStyle.FontWeight":"",
  "DateStyle.FontStyle":"",
  "DateStyle.FontStretch":"",
  "DateStyle.CharacterSpacing":0,"oldTaskbarOnWin11":0,"DataCollectionUpdateInterval":1,"WebContentWeatherLocation":"",
  "WebContentWeatherFormat":"%c 🌡️%t 🌬️%w",
  "DataCollection.NetworkMetricsFormat":"mbs",
  "DataCollection.NetworkMetricsFixedDecimals":-1,"DataCollection.PercentageFormat":"spacePaddingAndSymbol",
  "DataCollection.UpdateInterval":1,"WebContentWeatherUnits":"autoDetect"
}
```

</details>


---

## General Information

The theme changes the following elements:

- Taskbar Frame
- Taskbar Widget (compact version)

![Widget](widget.png)

- Icon borders
- Taskbar icon sizes (compact version)
- Search icon with label
- Search box
- System Tray
    - Icon sizes (compact version)
    - Chevron icon border
    - Software icon border
    - Microphone icon border
    - Spacing between element groups
    - Tray Overflow Flyout
- Alt+Tab

![Alt+Tab](alttab.png)

- Win+Tab background and Virtual Desktops bar
- Snap Bar and Picker
- Volume bar
- Window Preview Flyout

![Window Preview Flyout](wpf.png)

- Context menus (with animations)

![Menus](menu.png)

- Tooltips
- Removed drop shadows

## Animations Guide

To customize the animations, look for the last line `"styleConstants[7]": "AnimationSettings=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled=\"True\" FromHorizontalOffset=\"-50\" FromVerticalOffset=\"50\" /></TransitionCollection>"`

- For all items to display immediately, set `IsStaggeringEnabled=\"True\"` to `False`.

- `FromHorizontalOffset` and `FromVerticalOffset` are the directions where the items come from.
  - Horizontal **Positive** values is **Right**, **Negative** is **Left**.
  - Vertical **Positive** values is **Down**, **Negative** is **Up**.

---

## Known Issues

I didn't know how to fix these. I couldn't find the correct target names, or I'm not sure if they can even be changed/fixed.

- **Widget/Weather:** The bottom text line have incorrect placement in **Compact version** (renders off-screen).
- **Icon Hitboxes (Dock):** The Taskbar's rounded corners slightly limits the icon hitbox on the **top and bottom**, which makes it **impossible to minimize windows by clicking in those areas**.
- **SearchBox (Dock/Classic):** Have **unmatching look and position** when typing in.
- **SearchBox (Compact):** Have incorrect everything in the Compact version.
- **Missing Acrylic Backdrop:** The **Virtual Desktop Bar** and **Taskbar Overflow Flyout** (when taskbar is full) may not have Acrylic.

---

## Full Luminosity Theme
For that, download the listed mods and select "**Luminosity**" on each.
- Windows 11 Taskbar Styler
- Windows 11 Start Menu Styler
- Windows 11 Notification Center Styler
- Windows 11 File Explorer Styler

I also highly recommend **Translucent Windows** with **Mica** or **MicaAlt** selected as backdrop.

---

## Theme selection

The theme is integrated into the mod and can simply be selected from the mod's
settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Advanced" tab.
* Copy the content below to the text box under "Mod settings" and click "Save".

---

### Dock

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=$mbg",
  "controlStyles[1].target": "Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[1].styles[0]": "CornerRadius=$bcr",
  "controlStyles[2].target": "Taskbar.ExperienceToggleButton",
  "controlStyles[2].styles[0]": "CornerRadius=$bcr",
  "controlStyles[3].target": "Taskbar.TaskListButton",
  "controlStyles[3].styles[0]": "CornerRadius=$bcr",
  "controlStyles[4].target": "SearchUx.SearchUI.SearchButtonRootGrid#SearchBoxButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[4].styles[0]": "CornerRadius=$bcr",
  "controlStyles[5].target": "Windows.UI.Xaml.Controls.Border#SearchPillBackgroundElement",
  "controlStyles[5].styles[0]": "CornerRadius=$bcr",
  "controlStyles[6].target": "Windows.UI.Xaml.Controls.Border#MultiWindowElement",
  "controlStyles[6].styles[0]": "CornerRadius=$bcr",
  "controlStyles[6].styles[1]": "Margin=0,1,0,1",
  "controlStyles[7].target": "SystemTray.ChevronIconView",
  "controlStyles[7].styles[0]": "CornerRadius=$bcr",
  "controlStyles[7].styles[1]": "Margin=0,0,2,0",
  "controlStyles[8].target": "SystemTray.NotifyIconView > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[8].styles[0]": "CornerRadius=$bcr",
  "controlStyles[8].styles[1]": "Margin=2,4,2,4",
  "controlStyles[9].target": "SystemTray.IconView#SystemTrayIcon > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[9].styles[0]": "CornerRadius=$bcr",
  "controlStyles[9].styles[1]": "Margin=2,4,2,4",
  "controlStyles[10].target": "SystemTray.OmniButton#ControlCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[10].styles[0]": "CornerRadius=$bcr",
  "controlStyles[10].styles[1]": "Margin=2,4,2,4",
  "controlStyles[11].target": "SystemTray.OmniButton#NotificationCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[11].styles[0]": "CornerRadius=$bcr",
  "controlStyles[11].styles[1]": "Margin=2,4,2,4",
  "controlStyles[12].target": "Border#OverflowFlyoutBackgroundBorder",
  "controlStyles[12].styles[0]": "Background:=$mbg",
  "controlStyles[12].styles[1]": "CornerRadius:=$wcr",
  "controlStyles[12].styles[2]": "BorderThickness=$bt",
  "controlStyles[12].styles[3]": "BorderBrush=$bb",
  "controlStyles[12].styles[4]": "Shadow:=",
  "controlStyles[13].target": "Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid",
  "controlStyles[13].styles[0]": "Background:=$mbg",
  "controlStyles[13].styles[1]": "CornerRadius=$wcr",
  "controlStyles[13].styles[2]": "BorderThickness=$bt",
  "controlStyles[13].styles[3]": "BorderBrush=$bb",
  "controlStyles[13].styles[4]": "Shadow:=",
  "controlStyles[14].target": "Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect",
  "controlStyles[14].styles[0]": "Fill:=#10FFFFFF",
  "controlStyles[15].target": "Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill",
  "controlStyles[15].styles[0]": "Fill:=$t",
  "controlStyles[16].target": "Windows.UI.Xaml.Controls.Grid#HoverFlyoutGrid > Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground",
  "controlStyles[16].styles[0]": "Background:=$mbg",
  "controlStyles[16].styles[1]": "CornerRadius=$mcr",
  "controlStyles[16].styles[2]": "BorderThickness=$bt",
  "controlStyles[16].styles[3]": "BorderBrush=$bb",
  "controlStyles[16].styles[4]": "Shadow:=",
  "controlStyles[17].target": "Taskbar.TaskItemThumbnailView > Grid@CommonStates > Border#BackgroundBorder",
  "controlStyles[17].styles[0]": "Background=$t",
  "controlStyles[17].styles[1]": "CornerRadius=$mcr",
  "controlStyles[17].styles[2]": "BorderThickness@Normal=0",
  "controlStyles[17].styles[3]": "BorderBrush@Normal=$t",
  "controlStyles[17].styles[4]": "BorderThickness@PointerOver=0.05,0,0.05,2",
  "controlStyles[17].styles[5]": "BorderBrush@PointerOver:=<SolidColorBrush Color=\"{StaticResource SystemAccentColor}\" Opacity=\"0.8\" />",
  "controlStyles[18].target": "Windows.UI.Xaml.Controls.Button#CloseButton",
  "controlStyles[18].styles[0]": "CornerRadius=$mcr",
  "controlStyles[19].target": "Windows.UI.Xaml.Controls.ContentPresenter#BorderElement",
  "controlStyles[19].styles[0]": "CornerRadius=16",
  "controlStyles[19].styles[1]": "Margin=-1,-1,-1,-1",
  "controlStyles[20].target": "Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[20].styles[0]": "Background:=$mbg",
  "controlStyles[20].styles[1]": "CornerRadius=$wcr",
  "controlStyles[20].styles[2]": "BorderThickness=$bt",
  "controlStyles[20].styles[3]": "BorderBrush=$bb",
  "controlStyles[20].styles[4]": "Shadow:=",
  "controlStyles[21].target": "Windows.UI.Xaml.Controls.Border#BackgroundDimmingLayer",
  "controlStyles[21].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"0\" TintColor=\"#00000000\" />",
  "controlStyles[22].target": "WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar > Grid > Border",
  "controlStyles[22].styles[0]": "Background:=$mbg",
  "controlStyles[22].styles[1]": "CornerRadius=$wcr",
  "controlStyles[22].styles[2]": "BorderThickness=$bt",
  "controlStyles[22].styles[3]": "BorderBrush=$bb",
  "controlStyles[23].target": "WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar",
  "controlStyles[23].styles[0]": "MaxWidth:=900",
  "controlStyles[23].styles[1]": "Shadow:=",
  "controlStyles[24].target": "Windows.UI.Xaml.Controls.Grid#MainGrid",
  "controlStyles[24].styles[0]": "CornerRadius=$mcr",
  "controlStyles[24].styles[1]": "BorderThickness=$bt",
  "controlStyles[24].styles[2]": "BorderBrush=$bb",
  "controlStyles[25].target": "Windows.UI.Xaml.Controls.Button#VirtualDesktopElementCloseButton",
  "controlStyles[25].styles[0]": "CornerRadius=$bcr",
  "controlStyles[26].target": "Windows.UI.Xaml.Controls.Border#SnapBarBorder",
  "controlStyles[26].styles[0]": "Background:=$mbg",
  "controlStyles[26].styles[1]": "CornerRadius=$mcr",
  "controlStyles[26].styles[2]": "RenderTransform:=<TranslateTransform X=\"0\" Y=\"-20\" />",
  "controlStyles[26].styles[3]": "Margin=0,0,0,-10",
  "controlStyles[26].styles[4]": "Shadow:=",
  "controlStyles[27].target": "Windows.UI.Xaml.Controls.Border#SnapPickerBorder",
  "controlStyles[27].styles[0]": "Background:=$mbg",
  "controlStyles[27].styles[1]": "CornerRadius=$mcr",
  "controlStyles[27].styles[2]": "BorderThickness=$bt",
  "controlStyles[27].styles[3]": "BorderBrush=$bb",
  "controlStyles[28].target": "Windows.UI.Xaml.Controls.FlyoutPresenter > Border",
  "controlStyles[28].styles[0]": "Shadow:=",
  "controlStyles[29].target": "MenuFlyoutPresenter",
  "controlStyles[29].styles[0]": "CornerRadius=$mcr",
  "controlStyles[29].styles[1]": "Shadow:=",
  "controlStyles[30].target": "MenuFlyoutPresenter > Border",
  "controlStyles[30].styles[0]": "Background:=$mbg",
  "controlStyles[30].styles[1]": "CornerRadius=$mcr",
  "controlStyles[30].styles[2]": "BorderThickness=$bt",
  "controlStyles[30].styles[3]": "BorderBrush=$bb",
  "controlStyles[31].target": "Windows.UI.Xaml.Controls.MenuFlyoutItem",
  "controlStyles[31].styles[0]": "CornerRadius=$bcr",
  "controlStyles[32].target": "Windows.UI.Xaml.Controls.MenuFlyoutSubItem",
  "controlStyles[32].styles[0]": "CornerRadius=$bcr",
  "controlStyles[33].target": "Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot",
  "controlStyles[33].styles[0]": "Background:=$mbg",
  "controlStyles[33].styles[1]": "CornerRadius=$mcr",
  "controlStyles[33].styles[2]": "BorderThickness=$bt",
  "controlStyles[33].styles[3]": "BorderBrush=$bb",
  "controlStyles[33].styles[4]": "Shadow:=",
  "controlStyles[34].target": "ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel",
  "controlStyles[34].styles[0]": "ChildrenTransitions:=$AnimationSettings",
  "controlStyles[35].target": "Grid#LayoutRoot",
  "controlStyles[35].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  "controlStyles[36].target": "Border#BackgroundBorder",
  "controlStyles[36].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  "styleConstants[0]": "mbg=<AcrylicBrush TintColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" FallbackColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" TintOpacity=\"0.0\" TintLuminosityOpacity=\"1.0\" Opacity=\"1\"/>",
  "styleConstants[1]": "bcr=10",
  "styleConstants[2]": "wcr=20",
  "styleConstants[3]": "mcr=15",
  "styleConstants[4]": "t=Transparent",
  "styleConstants[5]": "bb=#20FFFFFF",
  "styleConstants[6]": "bt=1",
  "controlStyles[37].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[37].styles[0]": "Visibility=Collapsed",
  "controlStyles[38].target": "Taskbar.TaskbarFrame#TaskbarFrame",
  "controlStyles[38].styles[0]": "Height=53",
  "controlStyles[38].styles[1]": "Width=1200",
  "controlStyles[39].target": "Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid",
  "controlStyles[39].styles[0]": "Background:=$mbg",
  "controlStyles[39].styles[1]": "BorderThickness=$bt",
  "controlStyles[39].styles[2]": "BorderBrush:=$bb",
  "controlStyles[39].styles[3]": "CornerRadius=$mcr",
  "controlStyles[39].styles[4]": "Margin=0,0,0,5",
  "controlStyles[40].target": "Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke",
  "controlStyles[40].styles[0]": "Visibility=Collapsed",
  "controlStyles[41].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[41].styles[0]": "Margin=-417,-2,363,4",
  "styleConstants[7]": "AnimationSettings=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled=\"True\" FromHorizontalOffset=\"-50\" FromVerticalOffset=\"50\" /></TransitionCollection>"
}
```
</details>

---

### Classic

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=$mbg",
  "controlStyles[1].target": "Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[1].styles[0]": "CornerRadius=$bcr",
  "controlStyles[2].target": "Taskbar.ExperienceToggleButton",
  "controlStyles[2].styles[0]": "CornerRadius=$bcr",
  "controlStyles[3].target": "Taskbar.TaskListButton",
  "controlStyles[3].styles[0]": "CornerRadius=$bcr",
  "controlStyles[4].target": "SearchUx.SearchUI.SearchButtonRootGrid#SearchBoxButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[4].styles[0]": "CornerRadius=$bcr",
  "controlStyles[5].target": "Windows.UI.Xaml.Controls.Border#SearchPillBackgroundElement",
  "controlStyles[5].styles[0]": "CornerRadius=$bcr",
  "controlStyles[6].target": "Windows.UI.Xaml.Controls.Border#MultiWindowElement",
  "controlStyles[6].styles[0]": "CornerRadius=$bcr",
  "controlStyles[6].styles[1]": "Margin=0,1,0,1",
  "controlStyles[7].target": "SystemTray.ChevronIconView",
  "controlStyles[7].styles[0]": "CornerRadius=$bcr",
  "controlStyles[7].styles[1]": "Margin=0,0,2,0",
  "controlStyles[8].target": "SystemTray.NotifyIconView > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[8].styles[0]": "CornerRadius=$bcr",
  "controlStyles[8].styles[1]": "Margin=2,4,2,4",
  "controlStyles[9].target": "SystemTray.IconView#SystemTrayIcon > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[9].styles[0]": "CornerRadius=$bcr",
  "controlStyles[9].styles[1]": "Margin=2,4,2,4",
  "controlStyles[10].target": "SystemTray.OmniButton#ControlCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[10].styles[0]": "CornerRadius=$bcr",
  "controlStyles[10].styles[1]": "Margin=2,4,2,4",
  "controlStyles[11].target": "SystemTray.OmniButton#NotificationCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[11].styles[0]": "CornerRadius=$bcr",
  "controlStyles[11].styles[1]": "Margin=2,4,2,4",
  "controlStyles[12].target": "Border#OverflowFlyoutBackgroundBorder",
  "controlStyles[12].styles[0]": "Background:=$mbg",
  "controlStyles[12].styles[1]": "CornerRadius:=$wcr",
  "controlStyles[12].styles[2]": "BorderThickness=$bt",
  "controlStyles[12].styles[3]": "BorderBrush=$bb",
  "controlStyles[12].styles[4]": "Shadow:=",
  "controlStyles[13].target": "Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid",
  "controlStyles[13].styles[0]": "Background:=$mbg",
  "controlStyles[13].styles[1]": "CornerRadius=$wcr",
  "controlStyles[13].styles[2]": "BorderThickness=$bt",
  "controlStyles[13].styles[3]": "BorderBrush=$bb",
  "controlStyles[13].styles[4]": "Shadow:=",
  "controlStyles[14].target": "Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect",
  "controlStyles[14].styles[0]": "Fill:=#10FFFFFF",
  "controlStyles[15].target": "Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill",
  "controlStyles[15].styles[0]": "Fill:=$t",
  "controlStyles[16].target": "Windows.UI.Xaml.Controls.Grid#HoverFlyoutGrid > Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground",
  "controlStyles[16].styles[0]": "Background:=$mbg",
  "controlStyles[16].styles[1]": "CornerRadius=$mcr",
  "controlStyles[16].styles[2]": "BorderThickness=$bt",
  "controlStyles[16].styles[3]": "BorderBrush=$bb",
  "controlStyles[16].styles[4]": "Shadow:=",
  "controlStyles[17].target": "Taskbar.TaskItemThumbnailView > Grid@CommonStates > Border#BackgroundBorder",
  "controlStyles[17].styles[0]": "Background=$t",
  "controlStyles[17].styles[1]": "CornerRadius=$mcr",
  "controlStyles[17].styles[2]": "BorderThickness@Normal=0",
  "controlStyles[17].styles[3]": "BorderBrush@Normal=$t",
  "controlStyles[17].styles[4]": "BorderThickness@PointerOver=0.05,0,0.05,2",
  "controlStyles[17].styles[5]": "BorderBrush@PointerOver:=<SolidColorBrush Color=\"{StaticResource SystemAccentColor}\" Opacity=\"0.8\" />",
  "controlStyles[18].target": "Windows.UI.Xaml.Controls.Button#CloseButton",
  "controlStyles[18].styles[0]": "CornerRadius=$mcr",
  "controlStyles[19].target": "Windows.UI.Xaml.Controls.ContentPresenter#BorderElement",
  "controlStyles[19].styles[0]": "CornerRadius=16",
  "controlStyles[19].styles[1]": "Margin=-1,-1,-1,-1",
  "controlStyles[20].target": "Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[20].styles[0]": "Background:=$mbg",
  "controlStyles[20].styles[1]": "CornerRadius=$wcr",
  "controlStyles[20].styles[2]": "BorderThickness=$bt",
  "controlStyles[20].styles[3]": "BorderBrush=$bb",
  "controlStyles[20].styles[4]": "Shadow:=",
  "controlStyles[21].target": "Windows.UI.Xaml.Controls.Border#BackgroundDimmingLayer",
  "controlStyles[21].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"0\" TintColor=\"#00000000\" />",
  "controlStyles[22].target": "WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar > Grid > Border",
  "controlStyles[22].styles[0]": "Background:=$mbg",
  "controlStyles[22].styles[1]": "CornerRadius=$wcr",
  "controlStyles[22].styles[2]": "BorderThickness=$bt",
  "controlStyles[22].styles[3]": "BorderBrush=$bb",
  "controlStyles[23].target": "WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar",
  "controlStyles[23].styles[0]": "MaxWidth:=900",
  "controlStyles[23].styles[1]": "Shadow:=",
  "controlStyles[24].target": "Windows.UI.Xaml.Controls.Grid#MainGrid",
  "controlStyles[24].styles[0]": "CornerRadius=$mcr",
  "controlStyles[24].styles[1]": "BorderThickness=$bt",
  "controlStyles[24].styles[2]": "BorderBrush=$bb",
  "controlStyles[25].target": "Windows.UI.Xaml.Controls.Button#VirtualDesktopElementCloseButton",
  "controlStyles[25].styles[0]": "CornerRadius=$bcr",
  "controlStyles[26].target": "Windows.UI.Xaml.Controls.Border#SnapBarBorder",
  "controlStyles[26].styles[0]": "Background:=$mbg",
  "controlStyles[26].styles[1]": "CornerRadius=$mcr",
  "controlStyles[26].styles[2]": "RenderTransform:=<TranslateTransform X=\"0\" Y=\"-20\" />",
  "controlStyles[26].styles[3]": "Margin=0,0,0,-10",
  "controlStyles[26].styles[4]": "Shadow:=",
  "controlStyles[27].target": "Windows.UI.Xaml.Controls.Border#SnapPickerBorder",
  "controlStyles[27].styles[0]": "Background:=$mbg",
  "controlStyles[27].styles[1]": "CornerRadius=$mcr",
  "controlStyles[27].styles[2]": "BorderThickness=$bt",
  "controlStyles[27].styles[3]": "BorderBrush=$bb",
  "controlStyles[28].target": "Windows.UI.Xaml.Controls.FlyoutPresenter > Border",
  "controlStyles[28].styles[0]": "Shadow:=",
  "controlStyles[29].target": "MenuFlyoutPresenter",
  "controlStyles[29].styles[0]": "CornerRadius=$mcr",
  "controlStyles[29].styles[1]": "Shadow:=",
  "controlStyles[30].target": "MenuFlyoutPresenter > Border",
  "controlStyles[30].styles[0]": "Background:=$mbg",
  "controlStyles[30].styles[1]": "CornerRadius=$mcr",
  "controlStyles[30].styles[2]": "BorderThickness=$bt",
  "controlStyles[30].styles[3]": "BorderBrush=$bb",
  "controlStyles[31].target": "Windows.UI.Xaml.Controls.MenuFlyoutItem",
  "controlStyles[31].styles[0]": "CornerRadius=$bcr",
  "controlStyles[32].target": "Windows.UI.Xaml.Controls.MenuFlyoutSubItem",
  "controlStyles[32].styles[0]": "CornerRadius=$bcr",
  "controlStyles[33].target": "Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot",
  "controlStyles[33].styles[0]": "Background:=$mbg",
  "controlStyles[33].styles[1]": "CornerRadius=$mcr",
  "controlStyles[33].styles[2]": "BorderThickness=$bt",
  "controlStyles[33].styles[3]": "BorderBrush=$bb",
  "controlStyles[33].styles[4]": "Shadow:=",
  "controlStyles[34].target": "ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel",
  "controlStyles[34].styles[0]": "ChildrenTransitions:=$AnimationSettings",
  "controlStyles[35].target": "Grid#LayoutRoot",
  "controlStyles[35].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  "controlStyles[36].target": "Border#BackgroundBorder",
  "controlStyles[36].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  "styleConstants[0]": "mbg=<AcrylicBrush TintColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" FallbackColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" TintOpacity=\"0.0\" TintLuminosityOpacity=\"1.0\" Opacity=\"1\"/>",
  "styleConstants[1]": "bcr=10",
  "styleConstants[2]": "wcr=20",
  "styleConstants[3]": "mcr=15",
  "styleConstants[4]": "t=Transparent",
  "styleConstants[5]": "bb=#20FFFFFF",
  "styleConstants[6]": "bt=1",
  "controlStyles[37].target": "Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater",
  "controlStyles[37].styles[0]": "Margin=0,1,0,0",
  "controlStyles[38].target": "SystemTray.ChevronIconView",
  "controlStyles[38].styles[0]": "Margin=0,1,2,0",
  "controlStyles[39].target": "SystemTray.NotifyIconView > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[39].styles[0]": "Margin=2,5,2,4",
  "controlStyles[40].target": "SystemTray.IconView#SystemTrayIcon > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[40].styles[0]": "Margin=2,5,2,4",
  "controlStyles[41].target": "SystemTray.OmniButton#ControlCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[41].styles[0]": "Margin=2,5,2,4",
  "controlStyles[42].target": "SystemTray.OmniButton#NotificationCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[42].styles[0]": "Margin=2,5,2,4",
  "styleConstants[7]": "AnimationSettings=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled=\"True\" FromHorizontalOffset=\"-50\" FromVerticalOffset=\"50\" /></TransitionCollection>"
}
```
</details>

---

### Compact

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[0].styles[0]": "Fill:=$mbg",
  "controlStyles[1].target": "Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[1].styles[0]": "CornerRadius=$bcr",
  "controlStyles[2].target": "Taskbar.ExperienceToggleButton",
  "controlStyles[2].styles[0]": "CornerRadius=$bcr",
  "controlStyles[3].target": "Taskbar.TaskListButton",
  "controlStyles[3].styles[0]": "CornerRadius=$bcr",
  "controlStyles[4].target": "SearchUx.SearchUI.SearchButtonRootGrid#SearchBoxButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[4].styles[0]": "CornerRadius=$bcr",
  "controlStyles[5].target": "Windows.UI.Xaml.Controls.Border#SearchPillBackgroundElement",
  "controlStyles[5].styles[0]": "CornerRadius=$bcr",
  "controlStyles[6].target": "Windows.UI.Xaml.Controls.Border#MultiWindowElement",
  "controlStyles[6].styles[0]": "CornerRadius=$bcr",
  "controlStyles[6].styles[1]": "Margin=0,1,0,1",
  "controlStyles[7].target": "SystemTray.ChevronIconView",
  "controlStyles[7].styles[0]": "CornerRadius=$bcr",
  "controlStyles[7].styles[1]": "Margin=0,0,2,0",
  "controlStyles[8].target": "SystemTray.NotifyIconView > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[8].styles[0]": "CornerRadius=$bcr",
  "controlStyles[8].styles[1]": "Margin=2,4,2,4",
  "controlStyles[9].target": "SystemTray.IconView#SystemTrayIcon > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[9].styles[0]": "CornerRadius=$bcr",
  "controlStyles[9].styles[1]": "Margin=2,4,2,4",
  "controlStyles[10].target": "SystemTray.OmniButton#ControlCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[10].styles[0]": "CornerRadius=$bcr",
  "controlStyles[10].styles[1]": "Margin=2,4,2,4",
  "controlStyles[11].target": "SystemTray.OmniButton#NotificationCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[11].styles[0]": "CornerRadius=$bcr",
  "controlStyles[11].styles[1]": "Margin=2,4,2,4",
  "controlStyles[12].target": "Border#OverflowFlyoutBackgroundBorder",
  "controlStyles[12].styles[0]": "Background:=$mbg",
  "controlStyles[12].styles[1]": "CornerRadius:=$wcr",
  "controlStyles[12].styles[2]": "BorderThickness=$bt",
  "controlStyles[12].styles[3]": "BorderBrush=$bb",
  "controlStyles[12].styles[4]": "Shadow:=",
  "controlStyles[13].target": "Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid",
  "controlStyles[13].styles[0]": "Background:=$mbg",
  "controlStyles[13].styles[1]": "CornerRadius=$wcr",
  "controlStyles[13].styles[2]": "BorderThickness=$bt",
  "controlStyles[13].styles[3]": "BorderBrush=$bb",
  "controlStyles[13].styles[4]": "Shadow:=",
  "controlStyles[14].target": "Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect",
  "controlStyles[14].styles[0]": "Fill:=#10FFFFFF",
  "controlStyles[15].target": "Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill",
  "controlStyles[15].styles[0]": "Fill:=$t",
  "controlStyles[16].target": "Windows.UI.Xaml.Controls.Grid#HoverFlyoutGrid > Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground",
  "controlStyles[16].styles[0]": "Background:=$mbg",
  "controlStyles[16].styles[1]": "CornerRadius=$mcr",
  "controlStyles[16].styles[2]": "BorderThickness=$bt",
  "controlStyles[16].styles[3]": "BorderBrush=$bb",
  "controlStyles[16].styles[4]": "Shadow:=",
  "controlStyles[17].target": "Taskbar.TaskItemThumbnailView > Grid@CommonStates > Border#BackgroundBorder",
  "controlStyles[17].styles[0]": "Background=$t",
  "controlStyles[17].styles[1]": "CornerRadius=$mcr",
  "controlStyles[17].styles[2]": "BorderThickness@Normal=0",
  "controlStyles[17].styles[3]": "BorderBrush@Normal=$t",
  "controlStyles[17].styles[4]": "BorderThickness@PointerOver=0.05,0,0.05,2",
  "controlStyles[17].styles[5]": "BorderBrush@PointerOver:=<SolidColorBrush Color=\"{StaticResource SystemAccentColor}\" Opacity=\"0.8\" />",
  "controlStyles[18].target": "Windows.UI.Xaml.Controls.Button#CloseButton",
  "controlStyles[18].styles[0]": "CornerRadius=$mcr",
  "controlStyles[19].target": "Windows.UI.Xaml.Controls.ContentPresenter#BorderElement",
  "controlStyles[19].styles[0]": "CornerRadius=16",
  "controlStyles[19].styles[1]": "Margin=-1,-1,-1,-1",
  "controlStyles[20].target": "Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[20].styles[0]": "Background:=$mbg",
  "controlStyles[20].styles[1]": "CornerRadius=$wcr",
  "controlStyles[20].styles[2]": "BorderThickness=$bt",
  "controlStyles[20].styles[3]": "BorderBrush=$bb",
  "controlStyles[20].styles[4]": "Shadow:=",
  "controlStyles[21].target": "Windows.UI.Xaml.Controls.Border#BackgroundDimmingLayer",
  "controlStyles[21].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"0\" TintColor=\"#00000000\" />",
  "controlStyles[22].target": "WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar > Grid > Border",
  "controlStyles[22].styles[0]": "Background:=$mbg",
  "controlStyles[22].styles[1]": "CornerRadius=$wcr",
  "controlStyles[22].styles[2]": "BorderThickness=$bt",
  "controlStyles[22].styles[3]": "BorderBrush=$bb",
  "controlStyles[23].target": "WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar",
  "controlStyles[23].styles[0]": "MaxWidth:=900",
  "controlStyles[23].styles[1]": "Shadow:=",
  "controlStyles[24].target": "Windows.UI.Xaml.Controls.Grid#MainGrid",
  "controlStyles[24].styles[0]": "CornerRadius=$mcr",
  "controlStyles[24].styles[1]": "BorderThickness=$bt",
  "controlStyles[24].styles[2]": "BorderBrush=$bb",
  "controlStyles[25].target": "Windows.UI.Xaml.Controls.Button#VirtualDesktopElementCloseButton",
  "controlStyles[25].styles[0]": "CornerRadius=$bcr",
  "controlStyles[26].target": "Windows.UI.Xaml.Controls.Border#SnapBarBorder",
  "controlStyles[26].styles[0]": "Background:=$mbg",
  "controlStyles[26].styles[1]": "CornerRadius=$mcr",
  "controlStyles[26].styles[2]": "RenderTransform:=<TranslateTransform X=\"0\" Y=\"-20\" />",
  "controlStyles[26].styles[3]": "Margin=0,0,0,-10",
  "controlStyles[26].styles[4]": "Shadow:=",
  "controlStyles[27].target": "Windows.UI.Xaml.Controls.Border#SnapPickerBorder",
  "controlStyles[27].styles[0]": "Background:=$mbg",
  "controlStyles[27].styles[1]": "CornerRadius=$mcr",
  "controlStyles[27].styles[2]": "BorderThickness=$bt",
  "controlStyles[27].styles[3]": "BorderBrush=$bb",
  "controlStyles[28].target": "Windows.UI.Xaml.Controls.FlyoutPresenter > Border",
  "controlStyles[28].styles[0]": "Shadow:=",
  "controlStyles[29].target": "MenuFlyoutPresenter",
  "controlStyles[29].styles[0]": "CornerRadius=$mcr",
  "controlStyles[29].styles[1]": "Shadow:=",
  "controlStyles[30].target": "MenuFlyoutPresenter > Border",
  "controlStyles[30].styles[0]": "Background:=$mbg",
  "controlStyles[30].styles[1]": "CornerRadius=$mcr",
  "controlStyles[30].styles[2]": "BorderThickness=$bt",
  "controlStyles[30].styles[3]": "BorderBrush=$bb",
  "controlStyles[31].target": "Windows.UI.Xaml.Controls.MenuFlyoutItem",
  "controlStyles[31].styles[0]": "CornerRadius=$bcr",
  "controlStyles[32].target": "Windows.UI.Xaml.Controls.MenuFlyoutSubItem",
  "controlStyles[32].styles[0]": "CornerRadius=$bcr",
  "controlStyles[33].target": "Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot",
  "controlStyles[33].styles[0]": "Background:=$mbg",
  "controlStyles[33].styles[1]": "CornerRadius=$mcr",
  "controlStyles[33].styles[2]": "BorderThickness=$bt",
  "controlStyles[33].styles[3]": "BorderBrush=$bb",
  "controlStyles[33].styles[4]": "Shadow:=",
  "controlStyles[34].target": "ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel",
  "controlStyles[34].styles[0]": "ChildrenTransitions:=$AnimationSettings",
  "controlStyles[35].target": "Grid#LayoutRoot",
  "controlStyles[35].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  "controlStyles[36].target": "Border#BackgroundBorder",
  "controlStyles[36].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  "styleConstants[0]": "mbg=<AcrylicBrush TintColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" FallbackColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" TintOpacity=\"0.0\" TintLuminosityOpacity=\"1.0\" Opacity=\"1\"/>",
  "styleConstants[1]": "bcr=10",
  "styleConstants[2]": "wcr=20",
  "styleConstants[3]": "mcr=15",
  "styleConstants[4]": "t=Transparent",
  "styleConstants[5]": "bb=#20FFFFFF",
  "styleConstants[6]": "bt=1",
  "controlStyles[37].target": "Taskbar.TaskbarFrame#TaskbarFrame",
  "controlStyles[37].styles[0]": "Height=30",
  "controlStyles[38].target": "Windows.UI.Xaml.Controls.Border#LargeTicker1",
  "controlStyles[38].styles[0]": "Margin=1,-7,0,0",
  "controlStyles[38].styles[1]": "RenderTransform:=<ScaleTransform ScaleX=\"0.75\" ScaleY=\"0.75\" />",
  "controlStyles[39].target": "SearchUx.SearchUI.SearchButtonRootGrid#SearchBoxButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
  "controlStyles[39].styles[0]": "Margin=0,4,0,4",
  "controlStyles[40].target": "SearchUx.SearchUI.SearchButtonControl",
  "controlStyles[40].styles[0]": "Margin=0,-4,0,-4",
  "controlStyles[41].target": "Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer#Icon",
  "controlStyles[42].target": "Windows.UI.Xaml.Controls.Image#Icon",
  "controlStyles[41].styles[0]": "Width=16",
  "controlStyles[42].styles[0]": "Width=16",
  "controlStyles[41].styles[1]": "Height=16",
  "controlStyles[42].styles[1]": "Height=16",
  "controlStyles[43].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[43].styles[0]": "Margin=0,0,0,18",
  "controlStyles[44].target": "SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock",
  "controlStyles[44].styles[0]": "FontSize=14",
  "controlStyles[45].target": "SystemTray.ImageIconContent > Grid#ContainerGrid > Image",
  "controlStyles[45].styles[0]": "Width=14",
  "controlStyles[45].styles[1]": "Height=14",
  "styleConstants[7]": "AnimationSettings=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled=\"True\" FromHorizontalOffset=\"-50\" FromVerticalOffset=\"50\" /></TransitionCollection>"
}
```
</details>
