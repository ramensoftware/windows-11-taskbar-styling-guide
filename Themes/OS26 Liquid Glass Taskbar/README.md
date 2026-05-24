# OS26 Liquid Glass Taskbar

This theme styles the Windows 11 Taskbar into a floating, premium OS26-inspired "Liquid Glass" dock. It introduces heavily padded floating margins, pill-shaped rounded elements, custom running indicators, and tailored system tray styling.

## Taskbar Previews
![Taskbar Preview](taskbar_preview.png)

## System Tray & Elements Detail
![System Tray Preview](system_tray_preview.png)

---

## Design Features
* **Floating Dock Layout:** Padded margins (`150px` left/right) transform the taskbar into a distinct floating deck with a `20px` corner radius.
* **Liquid Glass Blur:** Embedded custom `<WindhawkBlur>` styling applied across individual blocks (Start Button, Search Box, Task List, Tray).
* **Cyberpunk Clock Accent:** Configured for the high-tech `Quantico` font face, enlarged text, and cleanly hidden date layouts.
* **Polished Micro-Borders:** Linear gradient accent strokes mimicking glass edge reflections.

## Prerequisites & Requirements

To achieve the intended look, make sure you meet the following setup requirements:

1. **Windhawk Mod:** This configuration is meant directly for the [Windows 11 Taskbar Styler](https://windhawk.net/mods/windows-11-taskbar-styler) mod.
2. **Clock Typography (Optional but Recommended):** To render the clock correctly as designed, ensure you have the `Quantico` font family installed on your system.

---

## Theme Installation

To apply this theme layout manually:
1. Open the **Windows 11 Taskbar Styler** mod dashboard inside Windhawk.
2. Head to the **Settings** tab and change the viewing layout interface to **"Textual mode"**.
3. Clear out everything in the box, copy the full JSON configuration code block below, paste it inside, and click **"Save settings"**.

<details>
<summary> 🌌 Click to expand Taskbar configuration code</summary>

```json
{
  "controlStyles[0].target": "Taskbar.TaskbarFrame > Grid#RootGrid",
  "controlStyles[0].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"15\" TintColor=\"{ThemeResource SystemChromeAltHighColor}\" TintOpacity=\"0.2\" />",
  "controlStyles[0].styles[1]": "Margin=150,1,150,4",
  "controlStyles[0].styles[2]": "CornerRadius=20",
  "controlStyles[0].styles[3]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#50ffffff\" Offset=\"0.0\" /><GradientStop Color=\"#10ffffff\" Offset=\"0.5\" /><GradientStop Color=\"#30ffffff\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[0].styles[4]": "BorderThickness=1.2",
  "controlStyles[0].styles[5]": "Padding=10,0",
  "controlStyles[1].target": "Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[1].styles[0]": "CornerRadius=20",
  "controlStyles[1].styles[1]": "Background:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#35ffffff\" />",
  "controlStyles[1].styles[2]": "Background@InactivePointerOver:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#45ffffff\" />",
  "controlStyles[1].styles[3]": "Background@ActivePointerOver:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#45ffffff\" />",
  "controlStyles[1].styles[4]": "Background@ActiveNormal:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#30ffffff\" />",
  "controlStyles[1].styles[5]": "Background@InactiveNormal:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#25ffffff\" />",
  "controlStyles[1].styles[6]": "Background@InactivePressed:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#30ffffff\" />",
  "controlStyles[1].styles[7]": "Background@ActivePressed:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#25ffffff\" />",
  "controlStyles[1].styles[8]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#E0ffffff\" Offset=\"0.0\" /><GradientStop Color=\"#20ffffff\" Offset=\"0.5\" /><GradientStop Color=\"#A0ffffff\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[1].styles[9]": "BorderThickness=1.2",
  "controlStyles[2].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[2].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"15\" TintColor=\"#25ffffff\" />",
  "controlStyles[2].styles[1]": "CornerRadius=14",
  "controlStyles[2].styles[2]": "Margin=60,10,-280,10",
  "controlStyles[2].styles[3]": "RenderTransform:=<TranslateTransform X=\"-435\" Y=\"-2\"/>",
  "controlStyles[2].styles[4]": "Padding=10",
  "controlStyles[2].styles[5]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#50ffffff\" Offset=\"0.0\" /><GradientStop Color=\"#10ffffff\" Offset=\"0.5\" /><GradientStop Color=\"#30ffffff\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[2].styles[6]": "BorderThickness=1.2",
  "controlStyles[3].target": "Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Rectangle#RunningIndicator",
  "controlStyles[3].styles[0]": "Fill:=#90ffffff",
  "controlStyles[3].styles[1]": "RadiusX=4",
  "controlStyles[3].styles[2]": "RadiusY=4",
  "controlStyles[3].styles[3]": "Height=3",
  "controlStyles[3].styles[4]": "Width=10",
  "controlStyles[3].styles[5]": "Width@ActiveRunningIndicator=20",
  "controlStyles[3].styles[6]": "Fill@ActiveRunningIndicator=#60CDFF",
  "controlStyles[4].target": "Taskbar.TaskListLabeledButtonPanel > TextBlock#LabelControl",
  "controlStyles[4].styles[0]": "Margin=4,0,0,0",
  "controlStyles[4].styles[1]": "Foreground=White",
  "controlStyles[5].target": "Taskbar.SearchBoxButton",
  "controlStyles[5].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#35ffffff\" />",
  "controlStyles[5].styles[1]": "CornerRadius=20",
  "controlStyles[5].styles[2]": "Margin=2,6,2,6",
  "controlStyles[5].styles[3]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#E0ffffff\" Offset=\"0.0\" /><GradientStop Color=\"#20ffffff\" Offset=\"0.5\" /><GradientStop Color=\"#A0ffffff\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[5].styles[4]": "BorderThickness=1.2",
  "controlStyles[6].target": "TextBlock#SearchBoxTextBlock",
  "controlStyles[6].styles[0]": "FontSize=12",
  "controlStyles[6].styles[1]": "Foreground=White",
  "controlStyles[7].target": "Grid",
  "controlStyles[7].styles[0]": "RequestedTheme=2",
  "controlStyles[8].target": "Taskbar.TaskListButton#TaskListButton[AutomationProperties.Name=Copilot] > Taskbar.TaskListLabeledButtonPanel#IconPanel > Border#BackgroundElement",
  "controlStyles[8].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"10\" TintColor=\"#10ffffff\" />",
  "controlStyles[9].target": "Taskbar.StartButton#StartButton",
  "controlStyles[9].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#35ffffff\" />",
  "controlStyles[9].styles[1]": "CornerRadius=20",
  "controlStyles[9].styles[2]": "Margin=2,6,2,6",
  "controlStyles[9].styles[3]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#E0ffffff\" Offset=\"0.0\" /><GradientStop Color=\"#20ffffff\" Offset=\"0.5\" /><GradientStop Color=\"#A0ffffff\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[9].styles[4]": "BorderThickness=1.2",
  "controlStyles[10].target": "Border#MultiWindowElement",
  "controlStyles[10].styles[0]": "Visibility=Collapsed",
  "controlStyles[11].target": "TextBlock#TimeInnerTextBlock",
  "controlStyles[11].styles[0]": "Foreground=White",
  "controlStyles[11].styles[1]": "FontSize=18",
  "controlStyles[11].styles[2]": "FontFamily=Quantico",
  "controlStyles[11].styles[3]": "Margin=0",
  "controlStyles[11].styles[4]": "Padding=0",
  "controlStyles[11].styles[5]": "RenderTransform:=<TranslateTransform X=\"0\" Y=\"1\" />",
  "controlStyles[12].target": "TextBlock#DateInnerTextBlock",
  "controlStyles[12].styles[0]": "Foreground=White",
  "controlStyles[12].styles[1]": "Visibility=Collapsed",
  "controlStyles[12].styles[2]": "RenderTransform:=<TranslateTransform X=\"0\" Y=\"-9\" />",
  "controlStyles[12].styles[3]": "FontSize=11",
  "controlStyles[12].styles[4]": "FontFamily=vivo Sans EN VF",
  "controlStyles[13].target": "SystemTray.TextIconContent > Grid > SystemTray.AdaptiveTextBlock#Base > TextBlock",
  "controlStyles[13].styles[0]": "Foreground=White",
  "controlStyles[14].target": "Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton",
  "controlStyles[14].styles[0]": "Margin=-12,0,0,0",
  "controlStyles[15].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.Name=Task View]",
  "controlStyles[15].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#35ffffff\" />",
  "controlStyles[15].styles[1]": "CornerRadius=20",
  "controlStyles[15].styles[2]": "Margin=2,6,2,6",
  "controlStyles[15].styles[3]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#E0ffffff\" Offset=\"0.0\" /><GradientStop Color=\"#20ffffff\" Offset=\"0.5\" /><GradientStop Color=\"#A0ffffff\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[15].styles[4]": "BorderThickness=1.2",
  "controlStyles[16].target": "taskbar:TaskListLabeledButtonPanel@RunningIndicatorStates > Border",
  "controlStyles[16].styles[0]": "Background@InactiveRunningIndicatorPointerOver:=<WindhawkBlur BlurAmount=\"40\" TintColor=\"#10ffffff\" />",
  "controlStyles[16].styles[1]": "CornerRadius=12",
  "controlStyles[16].styles[2]": "BorderBrush@InactiveRunningIndicatorPointerOver:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#80ffffff\" Offset=\"0.0\" /><GradientStop Color=\"{ThemeResource SurfaceStrokeColorDefault}\" Offset=\"0.55\" /><GradientStop Color=\"#80ffffff\" Offset=\"1\" /></LinearGradientBrush>",
  "controlStyles[16].styles[3]": "BorderThickness@InactiveRunningIndicatorPointerOver=1",
  "controlStyles[17].target": "Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement",
  "controlStyles[17].styles[0]": "CornerRadius=20",
  "controlStyles[17].styles[1]": "Background:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#35ffffff\" />",
  "controlStyles[17].styles[2]": "Background@InactivePointerOver:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#45ffffff\" />",
  "controlStyles[17].styles[3]": "Background@ActivePointerOver:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#45ffffff\" />",
  "controlStyles[17].styles[4]": "Background@ActiveNormal:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#30ffffff\" />",
  "controlStyles[17].styles[5]": "Background@InactiveNormal:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#25ffffff\" />",
  "controlStyles[17].styles[6]": "Background@InactivePressed:=<WindhawkBlur BlurAmount=\"60\" TintColor=\"#30ffffff\" />",
  "controlStyles[17].styles[7]": "Margin=0",
  "controlStyles[17].styles[8]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,1\"><GradientStop Color=\"#E0ffffff\" Offset=\"0.0\" /><GradientStop Color=\"#20ffffff\" Offset=\"0.5\" /><GradientStop Color=\"#A0ffffff\" Offset=\"1.0\" /></LinearGradientBrush>",
  "controlStyles[17].styles[9]": "BorderThickness=1.2",
  "controlStyles[18].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundStroke",
  "controlStyles[18].styles[0]": "Visibility=Collapsed",
  "controlStyles[19].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[19].styles[0]": "Fill=Transparent",
  "controlStyles[20].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[20].styles[0]": "Background:=<WindhawkBlur BlurAmount=\"10\" TintColor=\"#40ffffff\" />",
  "controlStyles[20].styles[1]": "CornerRadius=12",
  "controlStyles[20].styles[2]": "Margin=2",
  "controlStyles[20].styles[3]": "Padding=2",
  "controlStyles[20].styles[4]": "BorderBrush:=<LinearGradientBrush StartPoint=\"0,0\" EndPoint=\"1,0\"><GradientStop Color=\"#80ffffff\" Offset=\"0.0\" /><GradientStop Color=\"{ThemeResource SurfaceStrokeColorDefault}\" Offset=\"0.55\" /><GradientStop Color=\"#80ffffff\" Offset=\"1\" /></LinearGradientBrush>",
  "controlStyles[20].styles[5]": "BorderThickness=2",
  "theme": ""
}
