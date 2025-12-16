# The old 21996Taskbar (SunValley (Legacy)) theme for Windows 11 Taskbar Styler

> [!NOTE]
> This theme was superseded by the new [SunValley theme](https://github.com/ramensoftware/windows-11-taskbar-styling-guide/blob/main/Themes/SunValley/README.md)
> 
> this theme will not be updated to support newer versions of Windows 11, and the reason why I decided to keep it here is for archival purposes.
> 
This theme tries to recreate earlier versions of the Windows 11 Taskbar, which includes:
* Windows 10 style system tray and tray overflow
* Windows 10 Window thumbnails (For newer 11 builds which contain the new Window Thumbnails)
* 21370-22000.9-like acrylic with accent color support

#
**Author**: [Tails](https://github.com/milestprower92)

#
**Taskbar**

[![Taskbar](screenshot.png)](screenshot.png)

**Tray Overflow**

[![Overflow](screenshot-overflow.png)](screenshot-overflow.png)

**Window Thumbnails**

[![Thumbnails](screenshot-thumbnails.png)](screenshot-thumbnails.png)
#
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
"controlStyles[0].target":"Taskbar.SearchBoxButton#SearchBoxButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement",
"controlStyles[0].styles[0]":"CornerRadius=4",
"controlStyles[0].styles[1]":"BorderThickness=0",
"controlStyles[1].target":"Taskbar.SearchBoxButton",
"controlStyles[1].styles[0]":"Margin=0",
"controlStyles[2].target":"SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent > Windows.UI.Xaml.Controls.Grid > SystemTray.AdaptiveTextBlock > Windows.UI.Xaml.Controls.TextBlock",
"controlStyles[2].styles[0]":"Visibility=Visible",
"controlStyles[2].styles[1]":"Text=‎ ‎‎‎ ",
"controlStyles[2].styles[2]":"FontSize=16.4",
"controlStyles[2].styles[3]":"FontFamily=Segoe MDL2 Assets",
"controlStyles[2].styles[4]":"Width=30",
"controlStyles[2].styles[5]":"FontWeight=ExtraLight",
"controlStyles[2].styles[6]":"Foreground:=<SolidColorBrush Color=\"{ThemeResource SystemBaseHighColor}\" />",
"controlStyles[3].target":"Windows.UI.Xaml.Controls.FontIcon#SearchBoxFontIcon",
"controlStyles[3].styles[0]":"FontFamily=Segoe Fluent Icons",
"controlStyles[4].target":"Windows.UI.Xaml.Controls.TextBlock#SearchBoxTextBlock",
"controlStyles[4].styles[0]":"Text=Type here to search",
"controlStyles[4].styles[1]":"FontSize=14",
"controlStyles[5].target":"SystemTray.NotifyIconView#NotifyItemIcon",
"controlStyles[5].styles[0]":"CornerRadius=0",
"controlStyles[5].styles[1]":"Height=Auto",
"controlStyles[5].styles[2]":"Margin=0,0,0,0",
"controlStyles[5].styles[3]":"Padding=0",
"controlStyles[5].styles[4]":"BorderThickness=0",
"controlStyles[6].target":"SystemTray.ChevronIconView",
"controlStyles[6].styles[0]":"CornerRadius=0",
"controlStyles[6].styles[1]":"Height=Auto",
"controlStyles[6].styles[2]":"Width=24",
"controlStyles[6].styles[3]":"BorderThickness=0",
"controlStyles[6].styles[4]":"Padding=0",
"controlStyles[7].target":"Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Button#GleamEntryPointButton > Windows.UI.Xaml.Controls.Border",
"controlStyles[7].styles[0]":"CornerRadius=4",
"controlStyles[8].target":"Windows.UI.Xaml.Controls.Grid#DynamicSearchBoxGleamContainer",
"controlStyles[8].styles[0]":"CornerRadius=4",
"controlStyles[9].target":"SystemTray.OmniButton#NotificationCenterButton",
"controlStyles[9].styles[0]":"CornerRadius=0",
"controlStyles[9].styles[1]":"Padding=0,0,0,0",
"controlStyles[9].styles[2]":"Margin=0,0,0,0",
"controlStyles[9].styles[3]":"BorderThickness=0",
"controlStyles[10].target":"SystemTray.Stack#NonActivatableStack",
"controlStyles[10].styles[0]":"Height=Auto",
"controlStyles[10].styles[1]":"CornerRadius=0",
"controlStyles[10].styles[2]":"Margin=0,0,0,0",
"controlStyles[10].styles[3]":"Padding=0",
"controlStyles[10].styles[4]":"BorderThickness=0",
"controlStyles[11].target":"Rectangle#ShowDesktopPipe@CommonStates",
"controlStyles[11].styles[0]":"Width=9",
"controlStyles[11].styles[1]":"Margin=0,0,-10,0",
"controlStyles[11].styles[2]":"Height=500",
"controlStyles[11].styles[3]":"Fill@Active:=<AcrylicBrush TintColor=\"{ThemeResource SystemBaseLowColor}\" TintOpacity=\"0.5\" Opacity=\"0\"/>",
"controlStyles[11].styles[4]":"Stroke:=<SolidColorBrush Color=\"{ThemeResource SystemBaseHighColor}\" Opacity=\"0.5\"/>",
"controlStyles[12].target":"SystemTray.OmniButton#ControlCenterButton",
"controlStyles[12].styles[0]":"Padding=0",
"controlStyles[12].styles[1]":"CornerRadius=0",
"controlStyles[12].styles[2]":"Margin=0,0,0,0",
"controlStyles[12].styles[3]":"BorderThickness=0",
"controlStyles[13].target":"SystemTray.AdaptiveTextBlock#LanguageInnerTextBlock > TextBlock#InnerTextBlock",
"controlStyles[13].styles[0]":"FontFamily=Segoe UI",
"controlStyles[13].styles[1]":"Margin=-8,0,0,0",
"controlStyles[13].styles[2]":"FontSize=12",
"controlStyles[14].target":"SystemTray.SystemTrayFrame > Windows.UI.Xaml.Controls.Grid#SystemTrayFrameGrid > SystemTray.Stack#NotifyIconStack > Windows.UI.Xaml.Controls.Grid#Content > SystemTray.StackListView#IconStack > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.ContentPresenter > SystemTray.ChevronIconView > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter > Windows.UI.Xaml.Controls.Grid#ContentGrid > SystemTray.TextIconContent > Windows.UI.Xaml.Controls.Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock",
"controlStyles[14].styles[0]":"FontFamily=Segoe MDL2 Assets",
"controlStyles[14].styles[1]":"FontSize=12.4",
"controlStyles[14].styles[2]":"Foreground:=<SolidColorBrush Color=\"{ThemeResource SystemBaseHighColor}\" />",
"controlStyles[15].target":"SystemTray.SystemTrayFrame > Windows.UI.Xaml.Controls.Grid#SystemTrayFrameGrid > SystemTray.Stack#NotifyIconStack > Windows.UI.Xaml.Controls.Grid#Content > SystemTray.StackListView#IconStack > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.ContentPresenter",
"controlStyles[15].styles[0]":"Width=30",
"controlStyles[16].target":"SystemTray.AdaptiveTextBlock#Base > Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock",
"controlStyles[16].styles[0]":"FontFamily=Segoe MDL2 Assets",
"controlStyles[16].styles[1]":"Foreground:=<SolidColorBrush Color=\"{ThemeResource SystemBaseHighColor}\" />",
"controlStyles[17].target":"SystemTray.AdaptiveTextBlock#AccentOverlay > Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock",
"controlStyles[17].styles[0]":"FontFamily=Segoe MDL2 Assets",
"controlStyles[18].target":"SystemTray.AdaptiveTextBlock#Underlay > Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock",
"controlStyles[18].styles[0]":"FontFamily=Segoe MDL2 Assets",
"controlStyles[19].target":"SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[1] > SystemTray.IconView > Grid > Grid",
"controlStyles[19].styles[0]":"Margin=-6,0,0,0",
"controlStyles[20].target":"SystemTray.Stack#MainStack > Windows.UI.Xaml.Controls.Grid#Content",
"controlStyles[20].styles[0]":"CornerRadius=0",
"controlStyles[20].styles[1]":"Height=Auto",
"controlStyles[20].styles[2]":"Margin=0,0,0,0",
"controlStyles[20].styles[3]":"Padding=0",
"controlStyles[20].styles[4]":"BorderThickness=0",
"controlStyles[21].target":"Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.TextBlock#TimeInnerTextBlock",
"controlStyles[21].styles[0]":"FontFamily=Segoe UI",
"controlStyles[21].styles[1]":"TextAlignment=0",
"controlStyles[21].styles[2]":"FontSize=12",
"controlStyles[21].styles[3]":"Margin=0,-1,0,0",
"controlStyles[22].target":"Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.TextBlock#DateInnerTextBlock",
"controlStyles[22].styles[0]":"FontFamily=Segoe UI",
"controlStyles[22].styles[1]":"TextAlignment=0",
"controlStyles[22].styles[2]":"FontSize=12",
"controlStyles[22].styles[3]":"Margin=0,2,0,0",
"controlStyles[23].target":"SystemTray.NotificationAreaIcons#NotificationAreaIcons > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.ContentPresenter",
"controlStyles[23].styles[0]":"Width=23",
"controlStyles[23].styles[1]":"Margin=0,-2,0,0",
"controlStyles[24].target":"SystemTray.NotificationAreaIcons#NotificationAreaIcons > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.ContentPresenter > SystemTray.NotifyIconView#NotifyItemIcon > Windows.UI.Xaml.Controls.Grid#ContainerGrid",
"controlStyles[24].styles[0]":"Transform3D:=<CompositeTransform3D TranslateY=\"0\" TranslateX=\"0\" />",
"controlStyles[24].styles[1]":"HorizontalAlignment=0",
"controlStyles[25].target":"SystemTray.Stack#NotifyIconStack",
"controlStyles[25].styles[0]":"Width=24",
"controlStyles[26].target":"SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent > Windows.UI.Xaml.Controls.Grid > SystemTray.AdaptiveTextBlock > Windows.UI.Xaml.Controls.TextBlock",
"controlStyles[26].styles[0]":"FontSize=16",
"controlStyles[26].styles[1]":"Margin=0,-1,-0,0",
"controlStyles[26].styles[2]":"FontWeight=0",
"controlStyles[27].target":"SystemTray.CopilotIcon#CopilotIcon",
"controlStyles[27].styles[0]":"Visibility=Visible",
"controlStyles[27].styles[1]":"Margin=0,-7,0,0",
"controlStyles[27].styles[2]":"Height=61",
"controlStyles[28].target":"SystemTray.NotificationAreaOverflow > Windows.UI.Xaml.Controls.Grid#OverflowRootGrid > Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder",
"controlStyles[28].styles[0]":"CornerRadius=0",
"controlStyles[28].styles[1]":"Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAltHighColor}\" TintOpacity=\"0.7\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
"controlStyles[29].target":"SystemTray.NotificationAreaOverflow > Windows.UI.Xaml.Controls.Grid#OverflowRootGrid > Windows.UI.Xaml.Controls.ItemsControl > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.WrapGrid",
"controlStyles[29].styles[0]":"Margin=0,0,0,0",
"controlStyles[30].target":"SystemTray.NotifyIconView",
"controlStyles[30].styles[0]":"CornerRadius=0",
"controlStyles[31].target":"Windows.UI.Xaml.Controls.ScrollViewer > Windows.UI.Xaml.Controls.ScrollContentPresenter > Windows.UI.Xaml.Controls.Border > SystemTray.NotificationAreaOverflow",
"controlStyles[31].styles[0]":"Transform3D:=<CompositeTransform3D TranslateY=\"13\" />",
"controlStyles[32].target":"SystemTray.OmniButton#ControlCenterButton",
"controlStyles[32].styles[0]":"Visibility=Visible",
"controlStyles[33].target":"Taskbar.TaskbarBackground#BackgroundControl > Grid",
"controlStyles[33].styles[0]":"Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeMediumHighColor}\" TintOpacity=\"0\" TintLuminosityOpacity=\"0.8\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
"controlStyles[34].target":"Taskbar.TaskbarBackground#BackgroundControl > Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill",
"controlStyles[34].styles[0]":"Opacity=0.5",
"controlStyles[35].target":"Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke",
"controlStyles[35].styles[0]":"Visibility=Collapsed",
"controlStyles[36].target":"SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[3] > SystemTray.IconView > Grid > Grid",
"controlStyles[36].styles[0]":"Margin=2,0,-8,0",
"controlStyles[36].styles[1]":"RenderTransform:=<ScaleTransform ScaleX=\"0.86\" /> ",
"controlStyles[37].target":"Windows.UI.Xaml.Controls.ContentPresenter#HoverFlyoutContent",
"controlStyles[37].styles[0]":"CornerRadius=0",
"controlStyles[37].styles[1]":"Margin=0,0,0,-15",
"controlStyles[37].styles[2]":"Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemAltHighColor}\" TintOpacity=\"0.7\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
"controlStyles[38].target":"Taskbar.TaskItemThumbnailView > Grid > TextBlock",
"controlStyles[38].styles[0]":"FontFamily=Segoe UI",
"controlStyles[38].styles[1]":"FontSize=12",
"controlStyles[38].styles[2]":"Margin=3,0,8,8",
"controlStyles[39].target":"Taskbar.TaskItemThumbnailView > Windows.UI.Xaml.Controls.Grid > Microsoft.UI.Xaml.Controls.ItemsRepeater > Windows.UI.Xaml.Controls.Image",
"controlStyles[39].styles[0]":"Margin=0,-7,0,0",
"controlStyles[40].target":"Taskbar.TaskItemThumbnailView > Grid > Button > ContentPresenter > TextBlock",
"controlStyles[40].styles[0]":"FontFamily=Segoe MDL2 Assets",
"controlStyles[41].target":"Taskbar.TaskItemThumbnailView > Grid > Button",
"controlStyles[41].styles[0]":"CornerRadius=0",
"controlStyles[41].styles[1]":"Height=32",
"controlStyles[41].styles[2]":"Margin=0,0,0,9",
"controlStyles[41].styles[3]":"Width=32",
"controlStyles[42].target":"Grid#DetailedViewGrid",
"controlStyles[42].styles[0]":"Margin=0,-7,0,0",
"controlStyles[43].target":"Taskbar.TaskItemThumbnailView > Grid > Border",
"controlStyles[43].styles[0]":"BorderBrush:=<SolidColorBrush Color=\"{ThemeResource SystemBaseHighColor}\" Opacity=\"0.5\" />",
"controlStyles[43].styles[1]":"CornerRadius=0",
"controlStyles[44].target":"SystemTray.OmniButton#NotificationCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.ContentPresenter > SystemTray.IconView > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ContentPresenter > Windows.UI.Xaml.Controls.Grid > SystemTray.TextIconContent > Windows.UI.Xaml.Controls.Grid > SystemTray.AdaptiveTextBlock#Base > Windows.UI.Xaml.Controls.TextBlock",
"controlStyles[44].styles[0]":"Text=‎",
"controlStyles[44].styles[1]":"FontWeight=Light",
"controlStyles[44].styles[2]":"FontSize=16.4",
"controlStyles[45].target":"SystemTray.OmniButton#NotificationCenterButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.ContentPresenter > SystemTray.IconView",
"controlStyles[44].styles[3]":"Foreground:=<SolidColorBrush Color=\"{ThemeResource SystemBaseHighColor}\" />",
"controlStyles[44].styles[4]":"Margin=-1,0,1,0",
"controlStyles[45].styles[0]":"CornerRadius=0",
"controlStyles[45].styles[1]":"Padding=0,0,0,0",
"controlStyles[46].target":"SystemTray.DateTimeIconContent > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.TextBlock",
"controlStyles[46].styles[0]":"FontFamily=Segoe UI",
"controlStyles[46].styles[1]":"TextAlignment=Center",
"controlStyles[47].target":"SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[2] > SystemTray.IconView > Grid > Grid",
"controlStyles[47].styles[0]":"Margin=0,0,-3,0",
"controlStyles[48].target":"Taskbar.ThumbBarButton > ContentPresenter",
"controlStyles[48].styles[0]":"CornerRadius=0",
"controlStyles[48].styles[1]":"Background:=<SolidColorBrush Opacity=\"0.5\" />",
"controlStyles[48].styles[2]":"BorderBrush:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeLowColor}\" FallbackColor=\"{ThemeResource SystemChromeLowColor}\" />",
"controlStyles[49].target":"Taskbar.ThumbBarButton > ContentPresenter > Image",
"controlStyles[49].styles[0]":"Height=15",
"controlStyles[49].styles[1]":"Width=15",
"controlStyles[50].target":"SearchUx.SearchUI.SearchButtonRootGrid > Border",
"controlStyles[50].styles[0]":"CornerRadius=4",
"controlStyles[51].target":"TextBlock#BatteryTextBlock",
"controlStyles[51].styles[0]":"FontFamily=Segoe UI",
"controlStyles[51].styles[1]":"Margin=2,0,-2,0",
"controlStyles[52].target":"SystemTray.BatteryIconContent > Grid > Windows.UI.Xaml.Controls.StackPanel > Grid > TextBlock",
"controlStyles[52].styles[0]":"RenderTransform:=<ScaleTransform ScaleX=\"1\" />",
"controlStyles[53].target":"SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > Border#BackgroundBorder",
"controlStyles[53].styles[0]":"CornerRadius=0",
"controlStyles[53].styles[1]":"Opacity=0",
"controlStyles[54].target":"Windows.UI.Xaml.Controls.Button#GleamEntryPointButton > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ContentPresenter",
"controlStyles[54].styles[0]":"CornerRadius=3",
"controlStyles[55].target":"SearchUx.SearchUI.SearchButtonRootGrid ",
"controlStyles[55].styles[0]":"Margin=2,0,0,0",
"controlStyles[56].target":"SystemTray.ChevronIconView > Grid > ContentPresenter",
"controlStyles[56].styles[0]":"Transform3D:=<CompositeTransform3D TranslateY=\"-1\" TranslateX=\"2\" />",
"controlStyles[56].styles[1]":"HorizontalAlignment=0",
"controlStyles[57].target":"Border#SearchPillBackgroundElement",
"controlStyles[57].styles[0]":"CornerRadius=4",
"controlStyles[58].target":"Grid#ConfirmatorMainGrid",
"controlStyles[58].styles[0]":"Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeMediumHighColor}\" TintOpacity=\"0\" TintLuminosityOpacity=\"0.8\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
"controlStyles[58].styles[1]":"BorderBrush:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeHighColor}\" TintOpacity=\"0\" TintLuminosityOpacity=\"0.3\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
"controlStyles[58].styles[2]":"CornerRadius=6",
"controlStyles[58].styles[3]":"BorderThickness=0,1,0,0",
"controlStyles[59].target":"Slider > Grid > Grid > Grid > Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb",
"controlStyles[59].styles[0]":"Visibility=Visible",
"controlStyles[59].styles[1]":"Height=18",
"controlStyles[59].styles[2]":"Width=18",
"controlStyles[60].target":"Slider > Grid > Grid > Grid > Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb > Border",
"controlStyles[60].styles[0]":"BorderBrush:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeLowColor}\" TintOpacity=\"0.7\" TintLuminosityOpacity=\"0.7\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
"controlStyles[60].styles[1]":"BorderThickness=4",
"controlStyles[60].styles[2]":"Background:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\" />",
"controlStyles[60].styles[3]":"CornerRadius=10",
"controlStyles[61].target":"Slider > Grid > Grid > Grid > Rectangle#HorizontalDecreaseRect",
"controlStyles[61].styles[0]":"Fill:=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\" />",
"controlStyles[62].target":"Slider > Grid > Grid > Grid > Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb",
"controlStyles[62].styles[0]":"BorderBrush:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeHighColor}\" TintOpacity=\"0.7\" TintLuminosityOpacity=\"0.7\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
"controlStyles[62].styles[1]":"BorderThickness=0,1,0,0"
}
```
</details>
