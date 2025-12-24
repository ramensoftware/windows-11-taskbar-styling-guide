# TintedGlass theme for Windows 11 Taskbar Styler

**Author**: [TheRealCisWhiteMale](https://github.com/TheRealCisWhiteMale)

![Screenshot](screenshot.png)

## Required Windhawk Mods for similar results
To achieve similar results, install and configure the following Windhawk mods in addition to Taskbar Styler:

- Taskbar Clock Customization – for styling the clock. You will need to add your weather location if you have the desire to use that function and may need to change date formatting if you wish.

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "ShowSeconds": 1,
  "TimeFormat": "HH':'mm':'ss",
  "DateFormat": "ddd',' dd MMM yyyy",
  "WeekdayFormat": "custom",
  "WeekdayFormatCustom": "Mon, Tue, Wed, Thu, Fri, Sat, Sun",
  "TopLine": "%time%",
  "BottomLine": "%date%",
  "MiddleLine": "%weekday%",
  "TooltipLine": "%weather%",
  "Width": 180,
  "Height": 60,
  "MaxWidth": 0,
  "TextSpacing": -4,
  "WebContentsUpdateInterval": 10,
  "TimeStyle.Hidden": 0,
  "TimeStyle.TextColor": "",
  "TimeStyle.TextAlignment": "Right",
  "TimeStyle.FontSize": 16,
  "TimeStyle.FontFamily": "",
  "TimeStyle.FontWeight": "Medium",
  "TimeStyle.FontStyle": "",
  "TimeStyle.FontStretch": "",
  "TimeStyle.CharacterSpacing": 70,
  "DateStyle.Hidden": 0,
  "DateStyle.TextColor": "",
  "DateStyle.TextAlignment": "Right",
  "DateStyle.FontSize": 12,
  "DateStyle.FontFamily": "",
  "DateStyle.FontWeight": "",
  "DateStyle.FontStyle": "",
  "DateStyle.FontStretch": "",
  "DateStyle.CharacterSpacing": 0,
  "oldTaskbarOnWin11": 0,
  "DataCollectionUpdateInterval": 1,
  "WebContentsItems[0].Url": "https://rss.nytimes.com/services/xml/rss/nyt/World.xml",
  "WebContentsItems[0].BlockStart": "<item>",
  "WebContentsItems[0].Start": "<title>",
  "WebContentsItems[0].End": "</title>",
  "WebContentsItems[0].ContentMode": "xmlHtml",
  "WebContentsItems[0].SearchReplace[0].Search": "",
  "WebContentsItems[0].SearchReplace[0].Replace": "",
  "WebContentsItems[0].MaxLength": 28,
  "WebContentWeatherLocation": "",
  "WebContentWeatherFormat": "%c 🌡️%t 🌬️%w",
  "TimeZones[0]": "GMT Standard Time"
}
```
</details>

---

- Taskbar Height and Icon Size

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "IconSize": 32,
  "TaskbarHeight": 40,
  "TaskbarButtonWidth": 40,
  "IconSizeSmall": 16,
  "TaskbarButtonWidthSmall": 32
}
```
</details>

---

- Taskbar Labels for Windows 11

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "mode": "labelsWithoutCombining",
  "taskbarItemWidth": 0,
  "runningIndicatorStyle": "centerFixed",
  "progressIndicatorStyle": "sameAsRunningIndicatorStyle",
  "excludedPrograms[0]": "excluded1.exe",
  "minimumTaskbarItemWidth": 43,
  "maximumTaskbarItemWidth": 300,
  "fontSize": 13,
  "fontFamily": "",
  "textTrimming": "clip",
  "leftAndRightPaddingSize": 6,
  "spaceBetweenIconAndLabel": 6,
  "runningIndicatorHeight": 0,
  "runningIndicatorVerticalOffset": 0,
  "alwaysShowThumbnailLabels": 0,
  "labelForSingleItem": "%name%",
  "labelForMultipleItems": "[%amount%] %name%"
}
```
</details>

---

## Suggested Windhawk Mods for full theme continuity
To achieve the full look, install and configure the following Windhawk mods in addition to Taskbar Styler:

- Windows 11 Start Menu Styler - Be sure to add SearchHost.exe to Custom process inclusion list for full funtionality.

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "controlStyles[0].target": "Border#AcrylicBorder",
  "controlStyles[0].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[0].styles[1]": "BorderThickness=0",
  "controlStyles[0].styles[2]": "CornerRadius=14",
  "controlStyles[1].target": "Border#AcrylicOverlay",
  "controlStyles[1].styles[0]": "Visibility=Collapsed",
  "controlStyles[2].target": "Border#BorderElement",
  "controlStyles[2].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"18\" TintColor=\"#1AFFFFFF\"/>",
  "controlStyles[2].styles[1]": "BorderThickness=0",
  "controlStyles[2].styles[2]": "CornerRadius=14",
  "controlStyles[3].target": "Grid#ShowMoreSuggestions",
  "controlStyles[3].styles[0]": "Visibility=Collapsed",
  "controlStyles[4].target": "Grid#SuggestionsParentContainer",
  "controlStyles[4].styles[0]": "Visibility=Collapsed",
  "controlStyles[5].target": "Grid#TopLevelSuggestionsListHeader",
  "controlStyles[5].styles[0]": "Visibility=Collapsed",
  "controlStyles[6].target": "StartMenu.PinnedList",
  "controlStyles[6].styles[0]": "Height=504",
  "controlStyles[7].target": "MenuFlyoutPresenter > Border",
  "controlStyles[7].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"25\" TintColor=\"#00000000\"/>",
  "controlStyles[7].styles[1]": "BorderThickness=0",
  "controlStyles[8].target": "Border#AppBorder",
  "controlStyles[8].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[8].styles[1]": "BorderThickness=0",
  "controlStyles[8].styles[2]": "CornerRadius=14",
  "controlStyles[9].target": "Border#AccentAppBorder",
  "controlStyles[9].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[9].styles[1]": "BorderThickness=0",
  "controlStyles[9].styles[2]": "CornerRadius=14",
  "controlStyles[10].target": "Border#TaskbarSearchBackground",
  "controlStyles[10].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"25\" TintColor=\"#15000000\"/>",
  "controlStyles[10].styles[1]": "BorderThickness=0",
  "controlStyles[10].styles[2]": "CornerRadius=14",
  "controlStyles[11].target": "Border#ContentBorder@CommonStates > Grid#DroppedFlickerWorkaroundWrapper > Border",
  "controlStyles[11].styles[0]": "Background@Normal:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"0\" Opacity=\"0.2\"/>",
  "controlStyles[11].styles[1]": "Background@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.3\"/>",
  "controlStyles[11].styles[2]": "BorderBrush@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\"/>",
  "controlStyles[11].styles[3]": "Margin=1",
  "controlStyles[11].styles[4]": "Background@Pressed:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.3\"/>",
  "controlStyles[11].styles[5]": "BorderBrush@Pressed:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\"/>",
  "controlStyles[12].target": "Button#ShowAllAppsButton > ContentPresenter@CommonStates",
  "controlStyles[12].styles[0]": "Background@Normal:=<WindhawkBlur BlurAmount=\"25\" TintColor=\"#15000000\"/>",
  "controlStyles[12].styles[1]": "Background@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.5\"/>",
  "controlStyles[12].styles[2]": "BorderBrush@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\"/>",
  "controlStyles[12].styles[3]": "BorderThickness=1",
  "controlStyles[13].target": "StartDocked.SearchBoxToggleButton#StartMenuSearchBox > Grid > Border#BorderElement",
  "controlStyles[13].styles[0]": "BorderBrush:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\"/>",
  "controlStyles[13].styles[1]": "BorderThickness=1",
  "controlStyles[14].target": "StartDocked.NavigationPaneButton#UserTileButton > Grid@CommonStates > Border",
  "controlStyles[14].styles[0]": "Background@Normal:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"0\" Opacity=\"0.2\"/>",
  "controlStyles[14].styles[1]": "Background@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.5\"/>",
  "controlStyles[14].styles[2]": "BorderBrush@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.8\"/>",
  "controlStyles[14].styles[3]": "BorderThickness=1",
  "controlStyles[15].target": "StartDocked.AppListViewItem > Grid@CommonStates > Border",
  "controlStyles[15].styles[0]": "Background:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.45\"/>",
  "controlStyles[15].styles[1]": "BorderBrush:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.7\"/>",
  "controlStyles[15].styles[2]": "BorderThickness=1",
  "controlStyles[15].styles[3]": "Margin@Normal=4",
  "controlStyles[16].target": "StartDocked.NavigationPaneButton#PowerButton > Grid@CommonStates > Border",
  "controlStyles[16].styles[0]": "Background:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.45\"/>",
  "controlStyles[16].styles[1]": "BorderBrush:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.7\"/>",
  "controlStyles[16].styles[2]": "BorderThickness=1",
  "controlStyles[16].styles[3]": "Margin@Normal=4",
  "controlStyles[17].target": "ToolTip > ContentPresenter#LayoutRoot",
  "controlStyles[17].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"25\" TintColor=\"#15000000\"/>",
  "controlStyles[18].target": "StartDocked.AllAppsGridListViewItem > Grid@CommonStates > Border",
  "controlStyles[18].styles[0]": "BorderBrush@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.8\"/>",
  "controlStyles[18].styles[1]": "Background@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.55\"/>",
  "controlStyles[18].styles[2]": "BorderThickness=1",
  "controlStyles[19].target": "Button#CloseAllAppsButton > ContentPresenter@CommonStates",
  "controlStyles[19].styles[0]": "Background@Normal:=<WindhawkBlur BlurAmount=\"25\" TintColor=\"#15000000\"/>",
  "controlStyles[19].styles[1]": "Background@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.5\"/>",
  "controlStyles[19].styles[2]": "BorderBrush@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\"/>",
  "controlStyles[19].styles[3]": "BorderThickness=1",
  "controlStyles[20].target": "StartDocked.AllAppsZoomListViewItem > Grid@CommonStates > Border",
  "controlStyles[20].styles[0]": "Background@Normal:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"0\" Opacity=\"0.2\"/>",
  "controlStyles[20].styles[1]": "Background@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.3\"/>",
  "controlStyles[20].styles[2]": "BorderBrush@PointerOver:=<RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"0.6\"/>",
  "controlStyles[21].target": "Border#dropshadow",
  "controlStyles[21].styles[0]": "CornerRadius=14",
  "controlStyles[21].styles[1]": "Margin=-1",
  "controlStyles[22].target": "Border#DropShadow",
  "controlStyles[22].styles[0]": "CornerRadius=14",
  "controlStyles[23].target": "StartDocked.AllAppsGridListViewItem > Grid#ContentBorder@CommonStates",
  "controlStyles[23].styles[0]": "Background@PointerOver:=<WindhawkBlur BlurAmount=\"25\" TintColor=\"#15C0C0C0\"/>",
  "controlStyles[23].styles[1]": "CornerRadius=14",
  "styleConstants[0]": "CommonBgBrush=<WindhawkBlur BlurAmount=\"18\" TintColor=\"#80000000\"/>",
  "disableNewStartMenuLayout": 0,
  "webContentStyles[0].target": "",
  "webContentStyles[0].styles[0]": "",
  "webContentCustomJs": "",
  "resourceVariables[0].variableKey": "",
  "resourceVariables[0].value": ""
}
```
</details>

---

- Windows 11 Notification Center Styler

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "controlStyles[0].target": "Grid#NotificationCenterGrid",
  "controlStyles[0].styles[0]": "Background:=$Base",
  "controlStyles[0].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[0].styles[2]": "CornerRadius=$Radius",
  "controlStyles[1].target": "Grid#CalendarCenterGrid",
  "controlStyles[1].styles[0]": "Background:=$Base",
  "controlStyles[1].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[1].styles[2]": "CornerRadius=$Radius",
  "controlStyles[2].target": "ScrollViewer#CalendarControlScrollViewer",
  "controlStyles[3].target": "Border#CalendarHeaderMinimizedOverlay",
  "controlStyles[3].styles[0]": "Background:=$Transparent",
  "controlStyles[4].target": "ActionCenter.FocusSessionControl#FocusSessionControl > Grid#FocusGrid",
  "controlStyles[4].styles[0]": "Background:=$Transparent",
  "controlStyles[5].target": "MenuFlyoutPresenter > Border",
  "controlStyles[5].styles[0]": "Background:=$Overlay",
  "controlStyles[5].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[5].styles[2]": "CornerRadius=$Radius",
  "controlStyles[5].styles[3]": "Padding=2,4,2,4",
  "controlStyles[6].target": "Border#JumpListRestyledAcrylic",
  "controlStyles[6].styles[0]": "Background:=$Base",
  "controlStyles[6].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[6].styles[2]": "CornerRadius=$Radius",
  "controlStyles[6].styles[3]": "Margin=-2,-2,-2,-2",
  "controlStyles[7].target": "Grid#ControlCenterRegion",
  "controlStyles[7].styles[0]": "Background:=$Base",
  "controlStyles[7].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[7].styles[2]": "CornerRadius=$Radius",
  "controlStyles[8].target": "Grid#L1Grid > Border",
  "controlStyles[8].styles[0]": "Background:=$Transparent",
  "controlStyles[9].target": "Grid#MediaTransportControlsRegion",
  "controlStyles[9].styles[0]": "Background:=$Base",
  "controlStyles[9].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[9].styles[2]": "CornerRadius=$Radius",
  "controlStyles[10].target": "Grid#MediaTransportControlsRoot",
  "controlStyles[10].styles[0]": "Background:=$Transparent",
  "controlStyles[11].target": "ContentPresenter#PageContent",
  "controlStyles[11].styles[0]": "Background:=$Transparent",
  "controlStyles[12].target": "ContentPresenter#PageContent > Grid > Border",
  "controlStyles[12].styles[0]": "Background:=$Transparent",
  "controlStyles[13].target": "QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot",
  "controlStyles[13].styles[0]": "Background:=$Transparent",
  "controlStyles[14].target": "QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot > ContentPresenter#PageHeader",
  "controlStyles[14].styles[0]": "Background:=$Transparent",
  "controlStyles[15].target": "ScrollViewer#ListContent",
  "controlStyles[15].styles[0]": "Background:=$Transparent",
  "controlStyles[16].target": "ActionCenter.FlexibleToastView#FlexibleNormalToastView",
  "controlStyles[16].styles[0]": "Background:=$Transparent",
  "controlStyles[17].target": "Border#ToastBackgroundBorder2",
  "controlStyles[17].styles[0]": "Background:=$Base",
  "controlStyles[17].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[17].styles[2]": "CornerRadius=$Radius",
  "controlStyles[18].target": "JumpViewUI.SystemItemListViewItem > Grid#LayoutRoot > Border#BackgroundBorder",
  "controlStyles[19].target": "JumpViewUI.JumpListListViewItem > Grid#LayoutRoot > Border#BackgroundBorder",
  "controlStyles[19].styles[0]": "CornerRadius=$Radius",
  "controlStyles[20].target": "ActionCenter.FlexibleItemView",
  "controlStyles[20].styles[0]": "CornerRadius=$Radius",
  "controlStyles[21].target": "Grid#MediaTransportControlsRegion",
  "controlStyles[21].styles[0]": "Height=470",
  "controlStyles[22].target": "Grid#AlbumTextAndArtContainer",
  "controlStyles[22].styles[0]": "Height=350",
  "controlStyles[23].target": "Grid#ThumbnailImage",
  "controlStyles[23].styles[0]": "Width=300",
  "controlStyles[23].styles[1]": "Height=300",
  "controlStyles[23].styles[2]": "HorizontalAlignment=Center",
  "controlStyles[23].styles[3]": "VerticalAlignment=Top",
  "controlStyles[23].styles[4]": "Grid.Column=1",
  "controlStyles[24].target": "Grid#ThumbnailImage > Border",
  "controlStyles[24].styles[0]": "CornerRadius=$Radius",
  "controlStyles[25].target": "StackPanel#PrimaryAndSecondaryTextContainer",
  "controlStyles[25].styles[0]": "VerticalAlignment=Bottom",
  "controlStyles[25].styles[1]": "Grid.Column=0",
  "controlStyles[26].target": "StackPanel#PrimaryAndSecondaryTextContainer > TextBlock#TitleText",
  "controlStyles[26].styles[0]": "TextAlignment=Center",
  "controlStyles[27].target": "StackPanel#PrimaryAndSecondaryTextContainer > TextBlock#SubtitleText",
  "controlStyles[27].styles[0]": "TextAlignment=Center",
  "resourceVariables[0].variableKey": "",
  "resourceVariables[0].value": "",
  "styleConstants[0]": "Base=<WindhawkBlur BlurAmount=\"18\" TintColor=\"#80000000\"/>",
  "styleConstants[1]": "Radius=14",
  "styleConstants[2]": "Transparent=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[2].styles[0]": "BorderThickness=0,0,0,0",
  "controlStyles[3].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[4].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[8].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[28].target": "ContentControl#TogglesGroup > ContentPresenter > ControlCenter.PaginatedGridView > Grid",
  "controlStyles[28].styles[0]": "BorderThickness=0,0,0,0",
  "controlStyles[29].target": "Grid#FooterGrid",
  "controlStyles[29].styles[0]": "BorderThickness=0,0,0,0",
  "styleConstants[3]": "Accent=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\" Opacity = \"1\" />",
  "styleConstants[4]": "Overlay=<WindhawkBlur BlurAmount=\"18\" TintColor=\"#1AFFFFFF\"/>",
  "controlStyles[2].styles[1]": "Background:=$Transparent",
  "controlStyles[18].styles[0]": "Background:=$Transparent",
  "controlStyles[18].styles[1]": "CornerRadius=$Radius"
}
```
</details>

---

- Windows 11 File Explorer Styler

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "controlStyles[0].target": "Grid#CommandBarControlRootGrid",
  "controlStyles[0].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[0].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[0].styles[2]": "BorderBrush=$CommonBgBrush",
  "controlStyles[1].target": "CommandBar#FileExplorerCommandBar",
  "controlStyles[1].styles[0]": "Background=Transparent",
  "controlStyles[2].target": "Grid#NavigationBarControlGrid",
  "controlStyles[2].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[3].target": "TabViewItem > Grid#LayoutRoot > Canvas > Microsoft.UI.Xaml.Shapes.Path#SelectedBackgroundPath",
  "controlStyles[4].target": "Grid#HomeViewRootGrid",
  "controlStyles[4].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[5].target": "FileExplorerExtensions.GalleryViewControl#GalleryViewControl > Grid",
  "controlStyles[5].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[6].target": "Microsoft.UI.Xaml.Controls.Grid#GalleryRootGrid",
  "controlStyles[6].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[7].target": "ToolTip",
  "controlStyles[7].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[8].target": "Grid#DetailsViewControlRootGrid",
  "controlStyles[8].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[9].target": "StackPanel#DetailsViewThumbnail > Grid",
  "controlStyles[9].styles[0]": "Background:=$CommonBgBrush",
  "explorerFrameContainerHeight": 0,
  "controlStyles[3].styles[0]": "Fill:=$CommonBgBrush",
  "styleConstants[0]": "CommonBgBrush=<WindhawkBlur BlurAmount=\"18\" TintColor=\"#80000000\"/>",
  "controlStyles[10].target": "TextBlock",
  "controlStyles[10].styles[0]": "Fill=#FFFFFF",
  "resourceVariables[0].variableKey": "",
  "resourceVariables[0].value": ""
}
```
</details>

---

- Translucent Windows

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "RenderingMod.ThemeBackground": 1,
  "RenderingMod.AccentColorControls": 1,
  "type": "acrylicblur",
  "AccentBlurBehind": "80000000",
  "ImmersiveDarkTitle": 1,
  "ExtendFrame": 1,
  "CornerOption": "smallround",
  "RainbowSpeed": 1,
  "TitlebarColor.ColorTitlebar": 0,
  "TitlebarColor.RainbowTitlebar": 0,
  "TitlebarColor.titlerbarstyles_active": "0",
  "TitlebarColor.titlerbarstyles_inactive": "0",
  "TitlebarTextColor.ColorTitlebarText": 0,
  "TitlebarTextColor.RainbowTextColor": 0,
  "TitlebarTextColor.titlerbarcolorstyles_active": "FFFFFF",
  "TitlebarTextColor.titlerbarcolorstyles_inactive": "FFFFFF",
  "BorderColor.ColorBorder": 1,
  "BorderColor.RainbowBorder": 0,
  "BorderColor.borderstyles_active": "0",
  "BorderColor.borderstyles_inactive": "0",
  "BorderColor.MenuBorderColor": 1,
  "RenderingMod.TextAlphaBlend": 1,
  "RuledPrograms[0].target": "notepad.exe",
  "RuledPrograms[0].type": "acrylicsystem",
  "RuledPrograms[0].ImmersiveDarkTitle": 1,
  "RuledPrograms[0].ExtendFrame": 0,
  "RuledPrograms[0].BorderColor.ColorBorder": 1,
  "RuledPrograms[0].BorderColor.borderstyles_active": "0",
  "RuledPrograms[0].BorderColor.borderstyles_inactive": "0",
  "RuledPrograms[0].TitlebarTextColor.ColorTitlebarText": 0,
  "RuledPrograms[0].TitlebarTextColor.titlerbarcolorstyles_active": "FFFFFF",
  "RuledPrograms[0].TitlebarTextColor.titlerbarcolorstyles_inactive": "FFFFFF",
  "RuledPrograms[0].AccentBlurBehind": "80000000",
  "RuledPrograms[0].CornerOption": "smallround",
  "RuledPrograms[1].target": "notepad++.exe",
  "RuledPrograms[1].type": "acrylicsystem",
  "RuledPrograms[1].ImmersiveDarkTitle": 1,
  "RuledPrograms[1].ExtendFrame": 0,
  "RuledPrograms[1].BorderColor.ColorBorder": 1,
  "RuledPrograms[1].BorderColor.borderstyles_active": "0",
  "RuledPrograms[1].BorderColor.borderstyles_inactive": "0",
  "RuledPrograms[1].TitlebarTextColor.ColorTitlebarText": 0,
  "RuledPrograms[1].TitlebarTextColor.titlerbarcolorstyles_active": "FFFFFF",
  "RuledPrograms[1].TitlebarTextColor.titlerbarcolorstyles_inactive": "FFFFFF",
  "RuledPrograms[1].AccentBlurBehind": "80000000",
  "RuledPrograms[1].CornerOption": "smallround"
}
```
</details>

---

- Taskbar Background Helper

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "backgroundStyle": "blur",
  "color.red": 255,
  "color.green": 127,
  "color.blue": 39,
  "color.accentColor": 0,
  "color.transparency": 128,
  "onlyWhenMaximized": 1,
  "excludedPrograms[0]": "",
  "styleForDarkMode.use": 0,
  "styleForDarkMode.backgroundStyle": "blur",
  "styleForDarkMode.color.red": 255,
  "styleForDarkMode.color.green": 127,
  "styleForDarkMode.color.blue": 39,
  "styleForDarkMode.color.accentColor": 0,
  "styleForDarkMode.color.transparency": 128
}
```
</details>

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

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Grid#CommandBarControlRootGrid",
  "controlStyles[0].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[0].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[0].styles[2]": "BorderBrush=$CommonBgBrush",
  "controlStyles[1].target": "CommandBar#FileExplorerCommandBar",
  "controlStyles[1].styles[0]": "Background=Transparent",
  "controlStyles[2].target": "Grid#NavigationBarControlGrid",
  "controlStyles[2].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[3].target": "TabViewItem > Grid#LayoutRoot > Canvas > Microsoft.UI.Xaml.Shapes.Path#SelectedBackgroundPath",
  "controlStyles[4].target": "Grid#HomeViewRootGrid",
  "controlStyles[4].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[5].target": "FileExplorerExtensions.GalleryViewControl#GalleryViewControl > Grid",
  "controlStyles[5].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[6].target": "Microsoft.UI.Xaml.Controls.Grid#GalleryRootGrid",
  "controlStyles[6].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[7].target": "ToolTip",
  "controlStyles[7].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[8].target": "Grid#DetailsViewControlRootGrid",
  "controlStyles[8].styles[0]": "Background:=$CommonBgBrush",
  "controlStyles[9].target": "StackPanel#DetailsViewThumbnail > Grid",
  "controlStyles[9].styles[0]": "Background:=$CommonBgBrush",
  "explorerFrameContainerHeight": 0,
  "controlStyles[3].styles[0]": "Fill:=$CommonBgBrush",
  "styleConstants[0]": "CommonBgBrush=<WindhawkBlur BlurAmount=\"18\" TintColor=\"#80000000\"/>",
  "controlStyles[10].target": "TextBlock",
  "controlStyles[10].styles[0]": "Fill=#FFFFFF",
  "resourceVariables[0].variableKey": "",
  "resourceVariables[0].value": ""
}
```
</details>