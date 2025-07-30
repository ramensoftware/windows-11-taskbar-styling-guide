# Plasma theme for Windows 11 Taskbar Styler

This theme aims to recreate the default Panel from KDE Plasma.

**Author**: [SandTechStuff](https://github.com/SandTechStuff)

![Screenshot](screenshot.png)

> [!NOTE]
> An internet connection is required to use this theme, as the relevant images are downloaded from this repository. This is also the reason why images may be slow to load on first use.
>
> This theme was designed for 100% display scaling.

> [!TIP]
> This theme will use the Noto Sans font if it is installed. It can be downloaded from here: https://fonts.google.com/noto/specimen/Noto+Sans. 
> 
> Install the `NotoSans-Regular.ttf` version included in the archive.

## Required additional mod configuration

Mod: [Taskbar Height and Icon Size](https://windhawk.net/mods/taskbar-icon-size)

<details>
<summary>Content to import (click to expand)</summary>

```json
{
	"IconSize": 30,
	"TaskbarHeight": 44,
	"TaskbarButtonWidth": 52
}
```

</details>

## Customization options

This theme has two available start button images. You can choose between them by adding a Style Constant in the Windhawk GUI.

* `StartButton=default`
    * The default start button from the Breeze theme.
* `StartButton=kubuntu`
    * The start button available in the Kubuntu Linux distro.

This theme has two available blur options. WindhawkBlur works properly on multiple monitors, while Acrylic is transparency mode aware (e.g. blur is disabled in Battery Saver). You can choose between them by adding a style in the Windhawk GUI.

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
```
Style:
```
Fill:=$WindhawkBlur
```
-- or --
```
Fill:=$Acrylic
```

<!-- ## Theme selection

The theme is integrated into the mod, and can be simply selected from the mod's
settings:

-   Open the Windows 11 Taskbar Styler mod in Windhawk.
-   Go to the "Settings" tab.
-   Select the theme and save the settings. -->

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

-   Open the Windows 11 Taskbar Styler mod in Windhawk.
-   Go to the "Advanced" tab.
-   Copy the content below to the text box under "Mod settings" and click "Save".

<details>
<summary>Content to import (click to expand)</summary>

```json
{
	"controlStyles[0].target": "Taskbar.TaskListButton > Taskbar.TaskListLabeledButtonPanel",
	"controlStyles[0].styles[0]": "Padding=0",
	"controlStyles[1].target": "Taskbar.TaskListButton > Taskbar.TaskListLabeledButtonPanel@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundElement",
	"controlStyles[1].styles[0]": "CornerRadius=0",
	"controlStyles[1].styles[1]": "BorderThickness=1,0,1,0",
	"controlStyles[1].styles[2]": "BorderBrush=Transparent",
	"controlStyles[1].styles[3]": "Background@ActiveNormal:=$taskbandActive",
	"controlStyles[1].styles[4]": "Background@InactiveNormal:=$taskbandInactiveNormal",
	"controlStyles[1].styles[5]": "Background@ActivePointerOver:=$taskbandPointerOver",
	"controlStyles[1].styles[6]": "Background@MultiWindowNormal:=$taskbandInactiveNormal",
	"controlStyles[1].styles[7]": "Background@MultiWindowPointerOver:=$taskbandPointerOver",
	"controlStyles[1].styles[8]": "Background@InactivePointerOver:=$taskbandPointerOver",
	"controlStyles[1].styles[9]": "Background@ActivePressed:=$taskbandPointerOver",
	"controlStyles[1].styles[10]": "Background@InactivePressed:=$taskbandPointerOver",
	"controlStyles[1].styles[11]": "Margin=0",
	"controlStyles[1].styles[12]": "Background@MultiWindowPressed:=$taskbandPointerOver",
	"controlStyles[1].styles[13]": "Background@MultiWindowActive:=$taskbandActive",
	"controlStyles[1].styles[14]": "Background@RequestingAttention:=$taskbandAttention",
	"controlStyles[1].styles[15]": "Background@RequestingAttentionPointerOver:=$taskbandPointerOver",
	"controlStyles[1].styles[16]": "Background@RequestingAttentionPressed:=$taskbandPointerOver",
	"controlStyles[1].styles[17]": "Background@RequestingAttentionMulti:=$taskbandAttention",
	"controlStyles[1].styles[18]": "Background@RequestingAttentionMultiPointerOver:=$taskbandPointerOver",
	"controlStyles[1].styles[19]": "Background@RequestingAttentionMultiPressed:=$taskbandPointerOver",
	"controlStyles[2].target": "Taskbar.TaskListButton > Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Windows.UI.Xaml.Controls.Border#BackgroundElement",
	"controlStyles[2].styles[0]": "Opacity@NoRunningIndicator=0",
	"controlStyles[3].target": "Taskbar.TaskListLabeledButtonPanel#IconPanel > Windows.UI.Xaml.Controls.Image#Icon",
	"controlStyles[3].styles[0]": "RenderTransform:=<TranslateTransform X=\"2\" />",
	"controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Windows.UI.Xaml.Shapes.Rectangle#RunningIndicator",
	"controlStyles[4].styles[0]": "Width=50",
	"controlStyles[4].styles[1]": "RadiusX=0",
	"controlStyles[4].styles[2]": "RadiusY=0",
	"controlStyles[4].styles[3]": "Height=3",
	"controlStyles[4].styles[4]": "VerticalAlignment=Top",
	"controlStyles[4].styles[5]": "RenderTransform:=<TranslateTransform X=\"2\" />",
	"controlStyles[4].styles[6]": "Margin=-1,0,-1,0",
	"controlStyles[4].styles[7]": "Fill@ActiveNormal:=$indicatorActive",
	"controlStyles[4].styles[8]": "Fill@ActivePointerOver:=$indicatorPointerOver",
	"controlStyles[4].styles[9]": "Fill:=$indicatorInactive",
	"controlStyles[4].styles[10]": "Fill@InactivePointerOver:=$indicatorPointerOver",
	"controlStyles[4].styles[11]": "Fill@ActivePressed:=$indicatorPointerOver",
	"controlStyles[4].styles[12]": "Fill@InactivePressed:=$indicatorPointerOver",
	"controlStyles[4].styles[13]": "Fill@MultiWindowNormal:=$indicatorInactive",
	"controlStyles[4].styles[14]": "Fill@MultiWindowPointerOver:=$indicatorPointerOver",
	"controlStyles[4].styles[15]": "Fill@MultiWindowPressed:=$indicatorPointerOver",
	"controlStyles[4].styles[16]": "Fill@MultiWindowActive:=$indicatorActive",
	"controlStyles[4].styles[17]": "Fill@RequestingAttention:=$indicatorAttention",
	"controlStyles[4].styles[18]": "Fill@RequestingAttentionPointerOver:=$indicatorPointerOver",
	"controlStyles[4].styles[19]": "Fill@RequestingAttentionPressed:=$indicatorPointerOver",
	"controlStyles[4].styles[20]": "Fill@RequestingAttentionMulti:=$indicatorAttention",
	"controlStyles[4].styles[21]": "Fill@RequestingAttentionMultiPointerOver:=$indicatorPointerOver",
	"controlStyles[4].styles[22]": "Fill@RequestingAttentionMultiPressed:=$indicatorPointerOver",
	"controlStyles[5].target": "Rectangle#BackgroundStroke",
	"controlStyles[5].styles[0]": "Visibility=Collapsed",
	"controlStyles[6].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
	"controlStyles[6].styles[0]": "Fill:=$WindhawkBlur",
	"controlStyles[7].target": "Windows.UI.Xaml.Controls.Border#MultiWindowElement",
	"controlStyles[7].styles[0]": "Visibility=Collapsed",
	"controlStyles[8].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Windows.UI.Xaml.Shapes.Rectangle#DefaultIcon",
	"controlStyles[8].styles[0]": "Fill:=<ImageBrush Stretch=\"Uniform\" ImageSource=\"$plusIndicator\" />",
	"controlStyles[8].styles[1]": "Width=11",
	"controlStyles[8].styles[2]": "Height=11",
	"controlStyles[8].styles[3]": "RadiusX=0",
	"controlStyles[8].styles[4]": "RadiusY=0",
	"controlStyles[8].styles[5]": "VerticalAlignment=Bottom",
	"controlStyles[8].styles[6]": "RenderTransform:=<TranslateTransform X=\"1\" />",
	"controlStyles[8].styles[7]": "Visibility@MultiWindowNormal=Visible",
	"controlStyles[8].styles[8]": "Visibility@MultiWindowActive=Visible",
	"controlStyles[8].styles[9]": "Visibility@MultiWindowPointerOver=Visible",
	"controlStyles[8].styles[10]": "HorizontalAlignment=Center",
	"controlStyles[8].styles[11]": "Visibility@MultiWindowPressed=Visible",
	"controlStyles[8].styles[12]": "Visibility=Collapsed",
	"controlStyles[9].target": "Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel",
	"controlStyles[9].styles[0]": "Padding=0",
	"controlStyles[9].styles[1]": "Width=50",
	"controlStyles[10].target": "Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundElement",
	"controlStyles[10].styles[0]": "CornerRadius=0",
	"controlStyles[10].styles[1]": "BorderThickness=0",
	"controlStyles[10].styles[2]": "Width=32",
	"controlStyles[10].styles[3]": "Background=Transparent",
	"controlStyles[11].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel > Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer#Icon",
	"controlStyles[11].styles[0]": "Visibility=Collapsed",
	"controlStyles[12].target": "Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel@CommonStates",
	"controlStyles[12].styles[0]": "BorderThickness@ActiveNormal=0,3,0,0",
	"controlStyles[12].styles[1]": "Width=50",
	"controlStyles[12].styles[2]": "BorderBrush:=$selectionBorder",
	"controlStyles[12].styles[3]": "BorderThickness@ActivePointerOver=0,3,0,0",
	"controlStyles[12].styles[4]": "BorderThickness@ActivePressed=0,3,0,0",
	"controlStyles[13].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel > Border#BackgroundElement",
	"controlStyles[13].styles[0]": "Background:=<ImageBrush Stretch=\"Uniform\" ImageSource=\"https://raw.githubusercontent.com/SandTechStuff/windows-11-taskbar-styling-guide/refs/heads/theme/Themes/Plasma/ThemeResources/$StartButton.png\" />",
	"controlStyles[14].target": "Taskbar.AugmentedEntryPointButton[AutomationProperties.AutomationId=WidgetsButton] > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel",
	"controlStyles[14].styles[0]": "Width=Auto",
	"controlStyles[15].target": "SystemTray.Stack#NotifyIconStack",
	"controlStyles[15].styles[0]": "Grid.Column=5",
	"controlStyles[16].target": "SystemTray.NotificationAreaIcons#NotificationAreaIcons",
	"controlStyles[16].styles[0]": "Grid.Column=0",
	"controlStyles[17].target": "SystemTray.OmniButton#ControlCenterButton",
	"controlStyles[17].styles[0]": "Grid.Column=1",
	"controlStyles[18].target": "SystemTray.OmniButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
	"controlStyles[18].styles[0]": "Background=Transparent",
	"controlStyles[18].styles[1]": "Margin=1,0,1,0",
	"controlStyles[18].styles[2]": "CornerRadius=0",
	"controlStyles[19].target": "Windows.UI.Xaml.Controls.Grid#ContainerGrid@ > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
	"controlStyles[19].styles[0]": "BorderBrush@CheckedNormal:=$selectionBorderExtended",
	"controlStyles[19].styles[1]": "BorderThickness@CheckedNormal:=0,3,0,0",
	"controlStyles[19].styles[2]": "BorderBrush@CheckedPointerOver:=$selectionBorderExtended",
	"controlStyles[19].styles[3]": "BorderThickness@CheckedPointerOver:=0,3,0,0",
	"controlStyles[19].styles[4]": "BorderBrush@CheckedPressed:=$selectionBorderExtended",
	"controlStyles[19].styles[5]": "BorderThickness@CheckedPressed:=0,3,0,0",
	"controlStyles[19].styles[6]": "BorderThickness=0",
	"controlStyles[20].target": "SystemTray.OmniButton > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
	"controlStyles[20].styles[0]": "BorderBrush@Checked:=$selectionBorderExtended",
	"controlStyles[20].styles[1]": "BorderThickness@Checked:=0,3,0,0",
	"controlStyles[20].styles[2]": "BorderBrush@CheckedPointerOver:=$selectionBorderExtended",
	"controlStyles[20].styles[3]": "BorderThickness@CheckedPointerOver:=0,3,0,0",
	"controlStyles[20].styles[4]": "BorderBrush@CheckedPressed:=$selectionBorderExtended",
	"controlStyles[20].styles[5]": "BorderThickness@CheckedPressed:=0,3,0,0",
	"controlStyles[20].styles[6]": "BorderThickness=0",
	"controlStyles[21].target": "Windows.UI.Xaml.Controls.TextBlock#TimeInnerTextBlock",
	"controlStyles[21].styles[0]": "FontSize=17.33",
	"controlStyles[21].styles[1]": "TextAlignment=Center",
	"controlStyles[21].styles[2]": "FontFamily=Noto Sans, Segoe UI",
	"controlStyles[21].styles[3]": "Foreground=White",
	"controlStyles[22].target": "Windows.UI.Xaml.Controls.TextBlock#DateInnerTextBlock",
	"controlStyles[22].styles[0]": "FontSize=13.33",
	"controlStyles[22].styles[1]": "TextAlignment=Center",
	"controlStyles[22].styles[2]": "FontFamily=Noto Sans, Segoe UI",
	"controlStyles[22].styles[3]": "Margin=0,-5,0,0",
	"controlStyles[22].styles[4]": "Foreground=White",
	"controlStyles[23].target": "SystemTray.DateTimeIconContent > Windows.UI.Xaml.Controls.Grid#ContainerGrid",
	"controlStyles[23].styles[0]": "Padding=0",
	"controlStyles[24].target": "SystemTray.ChevronIconView > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter > Windows.UI.Xaml.Controls.Grid#ContentGrid > SystemTray.TextIconContent > Windows.UI.Xaml.Controls.Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock",
	"controlStyles[24].styles[1]": "Foreground=White",
	"controlStyles[24].styles[0]": "FontSize=17.33",
	"controlStyles[25].target": "SystemTray.ChevronIconView",
	"controlStyles[25].styles[0]": "Margin=-5,0",
	"controlStyles[26].target": "SystemTray.NotifyIconView#NotifyItemIcon",
	"controlStyles[26].styles[0]": "MinWidth=28",
	"controlStyles[27].target": "SystemTray.Stack#ShowDesktopStack",
	"controlStyles[27].styles[0]": "Width=48",
	"controlStyles[27].styles[1]": "Height=Auto",
	"controlStyles[28].target": "SystemTray.IconView[AutomationProperties.Name=Show Desktop]",
	"controlStyles[28].styles[0]": "Width=48",
	"controlStyles[29].target": "Windows.UI.Xaml.Shapes.Rectangle#ShowDesktopPipe",
	"controlStyles[29].styles[0]": "Width=48",
	"controlStyles[29].styles[1]": "Height=50",
	"controlStyles[29].styles[2]": "Fill:=<ImageBrush Stretch=\"None\" ImageSource=\"$desktopButton\" />",
	"controlStyles[30].target": "SystemTray.ChevronIconView > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
	"controlStyles[30].styles[0]": "Background=Transparent",
	"controlStyles[30].styles[1]": "Margin=1,0,1,0",
	"controlStyles[30].styles[2]": "CornerRadius=0",
	"controlStyles[31].target": "SystemTray.NotifyIconView > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
	"controlStyles[31].styles[0]": "Background=Transparent",
	"controlStyles[31].styles[1]": "Margin=1,0,1,0",
	"controlStyles[31].styles[2]": "CornerRadius=0",
	"controlStyles[32].target": "SystemTray.Stack#MainStack",
	"controlStyles[32].styles[0]": "//Grid.Column=2",
	"controlStyles[33].target": "SystemTray.Stack#NonActivatableStack",
	"controlStyles[33].styles[0]": "Grid.Column=3",
	"controlStyles[34].target": "SystemTray.IconView#SystemTrayIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
	"controlStyles[34].styles[0]": "Background=Transparent",
	"controlStyles[34].styles[1]": "Margin=1,0,1,0",
	"controlStyles[34].styles[2]": "CornerRadius=0",
	"controlStyles[35].target": "SystemTray.StackListView[AutomationProperties.AutomationId=Main]",
	"controlStyles[35].styles[0]": "Margin=-8,0,0,0",
	"controlStyles[36].target": "SystemTray.AdaptiveTextBlock#LanguageInnerTextBlock > Windows.UI.Xaml.Controls.TextBlock",
	"controlStyles[36].styles[0]": "FontFamily=Noto Sans, Segoe UI",
	"styleConstants[0]": "taskbandInactiveNormal=<SolidColorBrush Color=\"Gray\" Opacity=\"0.25\" />",
	"styleConstants[1]": "taskbandPointerOver=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\" Opacity=\"0.4\" />",
	"styleConstants[2]": "taskbandActive=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight1}\" Opacity=\"0.5\" />",
	"styleConstants[3]": "indicatorActive=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight2}\" Opacity=\"0.7\" />",
	"styleConstants[4]": "indicatorInactive=<SolidColorBrush Color=\"Gray\" Opacity=\"0.7\" />",
	"styleConstants[5]": "indicatorPointerOver=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight2}\" Opacity=\"0.8\" />",
	"styleConstants[6]": "taskbandAttention=<SolidColorBrush Color=\"#ce640c\" Opacity=\"0.5\" />",
	"styleConstants[7]": "indicatorAttention=<SolidColorBrush Color=\"#ce640c\" Opacity=\"0.9\" />",
	"styleConstants[8]": "selectionBorder=<LinearGradientBrush StartPoint='0,0' EndPoint='1,0'><GradientStop Color='Transparent' Offset='0.0' /><GradientStop Color='Transparent' Offset='0.2' /><GradientStop Color='{ThemeResource SystemAccentColorLight2}' Offset='0.2' /><GradientStop Color='{ThemeResource SystemAccentColorLight2}' Offset='0.8' /><GradientStop Color='Transparent' Offset='0.8' /><GradientStop Color='Transparent' Offset='1.0' /></LinearGradientBrush>",
	"styleConstants[9]": "selectionBorderExtended=<SolidColorBrush Color=\"{ThemeResource SystemAccentColorLight2}\" />",
	"styleConstants[10]": "desktopButton=https://raw.githubusercontent.com/SandTechStuff/windows-11-taskbar-styling-guide/refs/heads/theme/Themes/Plasma/ThemeResources/desktop.png",
	"styleConstants[11]": "plusIndicator=https://raw.githubusercontent.com/SandTechStuff/windows-11-taskbar-styling-guide/refs/heads/theme/Themes/Plasma/ThemeResources/plus.png",
	"styleConstants[12]": "StartButton=default",
	"styleConstants[13]": "WindhawkBlur=<WindhawkBlur BlurAmount=\"30\" TintColor=\"#cc2a2e32\" />",
	"styleConstants[14]": "Acrylic=<AcrylicBrush TintColor=\"#2a2e32\" TintOpacity=\"0.8\" FallbackColor=\"#2a2e32\" />"
}
```
</details>
