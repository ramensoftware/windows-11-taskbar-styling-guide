# "Oversimplified & Accentuated" Theme for "Windows 11 Taskbar Styler"

A cleaner, more refined Windows taskbar theme - removing unnecessary elements and offering better **Accent Color** integration.

> ⚠️ **Note:** This theme is optimized for Windows in **Dark Mode** and may not display correctly in **Light Mode**.

### ✨ Features
- Removed unnecessary text and lines
- Enlarged icons  
- Enhanced Accent Color Presence (Automatically Updates with Windows Accent Color)  
- Improved Transparency Effects
- Added Subtle, Neat Border Reveal Effects
- Took Fallback Colors (Colors in Battery Mode) into consideration

**Author:** [OsamaJT](https://github.com/OsamaHJT)

![Screenshot](Taskbar.png)

---

## 🎨 Elements Modified
- Taskbar
- Control Center icons in Taskbar
- Tray Menu
- Tray Menu icons
- Context Menu
- Active App Indicators & Progress Bar  in Taskbar
- Volume & Brightness Popups  
- Task Switcher (Alt + Tab)  
- Task View (Windows + Tab)
  
---

## 🧩 Installation

1. Download **[Windhawk](https://windhawk.net/)**.  
2. Install the **“[Windows 11 Taskbar Styler](https://windhawk.net/mods/windows-11-taskbar-styler)”** plugin.  
3. Choose the **“Oversimplified & Accentuated”** theme from the integrated themes list.  
   **OR**  
   Copy the JSON code below and go to:  
   **Windows 11 Taskbar Styler → Details → Advanced → Mod Settings**  
   Paste the code into the "**Mod settings**" box and click **Save**.


---

## 🛠️ Modification Notes

I added an extra comment line at the end of each style group to indicate the target object with common language.  
The aim is to make it easier to modify or debug the theme in the future.


<details>
<summary>Content to import (click to expand)</summary>

```json
{
"controlStyles[0].target": "MenuFlyoutPresenter",
"controlStyles[0].styles[0]": "Background:=$DarkAccent",
"controlStyles[0].styles[1]": "//Target= Context Menu",

"controlStyles[1].target": "Rectangle#BackgroundFill",
"controlStyles[1].styles[0]": "Fill:=$Alt",
"controlStyles[1].styles[1]": "//Target= Taskbar",

"controlStyles[2].target": "Rectangle#BackgroundStroke",
"controlStyles[2].styles[0]": "Visibility=Collapsed",
"controlStyles[2].styles[1]": "//Target= Taskbar Upper Border",

"controlStyles[3].target": "SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter#ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock",
"controlStyles[3].styles[0]": "FontSize=22",
"controlStyles[3].styles[1]": "//Target= Taskbar > Control Center Taskbar icons",

"controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Rectangle#RunningIndicator",
"controlStyles[4].styles[0]": "Fill@ActiveRunningIndicator:=$SolidAccent",
"controlStyles[4].styles[1]": "Height=4",
"controlStyles[4].styles[2]": "Width@ActiveRunningIndicator=25",
"controlStyles[4].styles[3]": "//Target= Taskbar > App Running Indicator",

"controlStyles[5].target": "Taskbar.TaskListButton > Taskbar.TaskListLabeledButtonPanel > Microsoft.UI.Xaml.Controls.ProgressBar#ProgressIndicator",
"controlStyles[5].styles[0]": "MinHeight=4",
"controlStyles[5].styles[1]": "Width=25",
"controlStyles[5].styles[2]": "//Target= Taskbar > App Progress Bar > Track Container",

"controlStyles[6].target": "Grid#LayoutRoot@CommonStates > Border#ProgressBarRoot > Border > Grid > Rectangle#DeterminateProgressBarIndicator",
"controlStyles[6].styles[0]": "Fill@Updating:= <SolidColorBrush Color=\"Green\" Opacity=\"1\" />",
"controlStyles[6].styles[1]": "Fill@Determinate:= <SolidColorBrush Color=\"Green\" Opacity=\"1\" />",
"controlStyles[6].styles[2]": "Fill@Paused:= <SolidColorBrush Color=\"Orange\" Opacity=\"1\" />",
"controlStyles[6].styles[3]": "Fill@Error:= <SolidColorBrush Color=\"Red\" Opacity=\"1\" />",
"controlStyles[6].styles[4]": "Fill@UpdatingError:= <SolidColorBrush Color=\"Red\" Opacity=\"1\" />",
"controlStyles[6].styles[5]": "//Target= Taskbar > App Progress Bar > Fill Track",

"controlStyles[7].target": "Rectangle#ProgressBarTrack",
"controlStyles[7].styles[0]": "Fill=Transparent",
"controlStyles[7].styles[1]": "//Target= Taskbar > App Progress Bar > Empty Track",

"controlStyles[8].target": "Grid#OverflowRootGrid",
"controlStyles[8].styles[0]": "Padding:=",
"controlStyles[8].styles[1]": "//Target= System Tray Menu Container",

"controlStyles[9].target": "Border#OverflowFlyoutBackgroundBorder",
"controlStyles[9].styles[0]": "Background:=$Alt",
"controlStyles[9].styles[1]": "Shadow:=",
"controlStyles[9].styles[2]": "BorderThickness:=",
"controlStyles[9].styles[3]": "//Target= System Tray Menu",

"controlStyles[10].target": "SystemTray.ImageIconContent > Windows.UI.Xaml.Controls.Grid#ContainerGrid > Windows.UI.Xaml.Controls.Image",
"controlStyles[10].styles[0]": "Height=20",
"controlStyles[10].styles[1]": "Width=20",
"controlStyles[10].styles[2]": "//Target= System Tray icons",

"controlStyles[11].target": "Grid#ConfirmatorMainGrid",
"controlStyles[11].styles[0]": "Background:=$DarkAccent",
"controlStyles[11].styles[1]": "BorderBrush=Transparent",
"controlStyles[11].styles[2]": "CornerRadius=15",
"controlStyles[11].styles[3]": "Margin=0,0,0,5",
"controlStyles[11].styles[4]": "Padding=4,0,0,0",
"controlStyles[11].styles[5]": "Shadow:=",
"controlStyles[11].styles[6]": "//Target= Volume & Brightness Popups > Plate",

"controlStyles[12].target": "Grid#BrightnessConfirmator",
"controlStyles[12].styles[0]": "Padding=6,0,16,0",
"controlStyles[12].styles[1]": "//Target= Brigtness Popup Container",

"controlStyles[13].target": "Microsoft.UI.Xaml.Controls.AnimatedIcon#BrightnessIcon",
"controlStyles[13].styles[0]": "Height=30",
"controlStyles[13].styles[1]": "Width=30",
"controlStyles[13].styles[2]": "Margin=0,-1,12,0",
"controlStyles[13].styles[3]": "//Target= Brigtness Popup > Brightness icon",

"controlStyles[14].target": "Microsoft.UI.Xaml.Controls.AnimatedIcon#VolumeIcon",
"controlStyles[14].styles[0]": "Height=30",
"controlStyles[14].styles[1]": "Width=30",
"controlStyles[14].styles[2]": "//Target= Volume Popup > Volume icon",

"controlStyles[15].target": "TextBlock#volumeLevelText",
"controlStyles[15].styles[0]": "FontSize=15",
"controlStyles[15].styles[1]": "//Target= Volume Popup > Volume Degree Text",

"controlStyles[16].target": "Rectangle#HorizontalDecreaseRect",
"controlStyles[16].styles[0]": "Height=6",
"controlStyles[16].styles[1]": "//Target= Volume & Brightness Popups > Track Container",

"controlStyles[17].target": "Rectangle#HorizontalTrackRect",
"controlStyles[17].styles[0]": "Fill=Transparent",
"controlStyles[17].styles[1]": "Height=6",
"controlStyles[17].styles[2]": "//Target= Volume & Brightness Popups > Empty Track",

"controlStyles[18].target": "Grid#HorizontalTemplate > Rectangle#HorizontalDecreaseRect",
"controlStyles[18].styles[0]": "Fill:= <AcrylicBrush TintColor=\"{ThemeResource SystemAccentColor}\" TintOpacity=\"1\" TintLuminosityOpacity=\"1\" FallbackColor=\"{ThemeResource SystemAccentColorDark2}\" />",
"controlStyles[18].styles[1]": "//Target= Volume & Brightness Popups > Fill Track",

"controlStyles[19].target": "Grid#ModalRootGrid > Border#BackgroundElement",
"controlStyles[19].styles[0]": "Background:=$DarkAccent",
"controlStyles[19].styles[1]": "BorderBrush=Transparent",
"controlStyles[19].styles[2]": "CornerRadius=20",
"controlStyles[19].styles[3]": "Shadow:=",
"controlStyles[19].styles[4]": "//Target= Alt+Tab Window Background",

"controlStyles[20].target": "Border#BackgroundDimmingLayer",
"controlStyles[20].styles[0]": "Background:= <WindhawkBlur BlurAmount=\"30\" TintColor=\"#00000080\" />",
"controlStyles[20].styles[1]": "//Target= Task View Background (Windows+Tab)",

"controlStyles[21].target": "Border#VirtualDesktopBarBackground",
"controlStyles[21].styles[0]": "Background:= <SolidColorBrush Color=\"{ThemeResource SystemAccentColorDark1}\" Opacity=\"0.4\" />",
"controlStyles[21].styles[1]": "BorderBrush=Transparent",
"controlStyles[21].styles[2]": "//Target= Task View (Windows+Tab) > Virtual Desktops Plate ",

"styleConstants[0]": "Alt= <AcrylicBrush TintColor=\"{ThemeResource SystemAltHighColor}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAltHighColor}\" />",
"styleConstants[1]": "Accent = <AcrylicBrush TintColor=\"{ThemeResource SystemAccentColor}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAccentColor}\" />",
"styleConstants[2]": "DarkAccent = <AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.3\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
"styleConstants[3]": "SolidAccent = <SolidColorBrush Color=\"{ThemeResource SystemAccentColor}\" Opacity=\"1\" />",
"styleConstants[4]": "Reveal= <RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\" />"
}
```
