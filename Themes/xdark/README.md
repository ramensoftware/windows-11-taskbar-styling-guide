# ✦ xdark theme for Windows 11 Taskbar Styler

**Author**: [xscriptorcode](https://github.com/xscriptorcode)

![Demonstration](screenshot.png)

# ✦ Required Windhawk Mods for Full Effect
To achieve the full implementation of the xdark theme, make sure your Windows is set to dark theme and the accent color is set to gold, and install and configure the following Windhawk mods in addition to Taskbar Styler:

- Taskbar Clock Customization – for styling the system clock.

<details>
<summary>Click to expand JSON content</summary>

```json
{
  "ShowSeconds": 1,
  "TimeFormat": "HH':'mm",
  "DateFormat": "dd'/'MM'/'yyyy",
  "WeekdayFormat": "",
  "TopLine": "",
  "MiddleLine": "",
  "BottomLine": "║▌║%date% X %time% ▌│",
  "TooltipLine": "%web1_full%",
  "Width": 180,
  "Height": 60,
  "TextSpacing": 0,
  "TimeStyle.Visible": 1,
  "TimeStyle.TextColor": "#facc15",
  "TimeStyle.TextAlignment": "Center",
  "TimeStyle.FontSize": 12,
  "TimeStyle.FontFamily": "JetBrainsMono NF",
  "TimeStyle.FontWeight": "ExtraLight",
  "TimeStyle.FontStyle": "",
  "TimeStyle.FontStretch": "",
  "TimeStyle.CharacterSpacing": 0,
  "DateStyle.TextColor": "#facc15",
  "DateStyle.TextAlignment": "Center",
  "DateStyle.FontSize": 12,
  "DateStyle.FontFamily": "Times New Roman",
  "DateStyle.FontWeight": "Light",
  "DateStyle.FontStyle": "Normal",
  "DateStyle.FontStretch": "SemiCondensed",
  "DateStyle.CharacterSpacing": 1,
  "oldTaskbarOnWin11": 0,
  "MaxWidth": 0,
  "TimeStyle.Hidden": 1,
  "DateStyle.Hidden": 0
}

```

</details>

---

- Taskbar Height and Icon Size – to adjust the proportions and padding of taskbar items.

<details>
<summary>Click to expand JSON content</summary>

```json

{
  "IconSize": 15,
  "TaskbarHeight": 35,
  "TaskbarButtonWidth": 30
}

```

</details>

---

- Taskbar Labels for Windows 11 – to enable visible labels next to app icons.

<details>
<summary>Click to expand JSON content</summary>

```json

{
  "taskbarItemWidth": 60,
  "minimumTaskbarItemWidth": 50,
  "maximumTaskbarItemWidth": 120,
  "runningIndicatorStyle": "centerFixed",
  "progressIndicatorStyle": "sameAsRunningIndicatorStyle",
  "fontSize": 12,
  "leftAndRightPaddingSize": 8,
  "spaceBetweenIconAndLabel": 8,
  "labelForSingleItem": "%name%",
  "labelForMultipleItems": "[%amount%] %name%",
  "mode": "labelsWithCombining",
  "excludedPrograms[0]": "excluded1.exe",
  "alwaysShowThumbnailLabels": 0,
  "fontFamily": "",
  "runningIndicatorHeight": 0,
  "runningIndicatorVerticalOffset": 0
}

```

</details>

---

# ✦ Manual Installation

You can manually import the styles like this:

* Open the **Windows 11 Taskbar Styler** mod in Windhawk.
* Go to the **Advanced** tab.
* Paste the following JSON content in the "Mod settings" section and click **Save**.

<details>
<summary>Click to expand JSON content</summary>

```json

{
  "controlStyles[0].target": "Taskbar.TaskListButton",
  "controlStyles[0].styles[0]": "CornerRadius=13",
  "controlStyles[0].styles[1]": "Padding=6,0,6,0",
  "controlStyles[0].styles[2]": "HorizontalContentAlignment=Left",
  "resourceVariables[0].variableKey": "",
  "resourceVariables[0].value": "",
  "controlStyles[1].target": "SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock",
  "controlStyles[1].styles[0]": "FontSize=16",
  "controlStyles[1].styles[1]": "Foreground=#facc15",
  "controlStyles[2].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[2].styles[0]": "MinWidth=25",
  "controlStyles[3].target": "SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[1] > SystemTray.IconView > Grid > Grid",
  "controlStyles[3].styles[0]": "Visibility=Collapsed",
  "controlStyles[4].target": "SystemTray.TextIconContent > Grid#ContainerGrid",
  "controlStyles[4].styles[0]": "Padding=2",
  "controlStyles[5].target": "SystemTray.ChevronIconView",
  "controlStyles[5].styles[0]": "MinWidth=27",
  "controlStyles[6].target": "SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent",
  "controlStyles[6].styles[0]": "Visibility=Collapsed",
  "controlStyles[7].target": "Taskbar.TaskListLabeledButtonPanel > Border#BackgroundElement",
  "controlStyles[7].styles[0]": "Background=#000000",
  "controlStyles[8].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[8].styles[0]": "Background=#000000",
  "controlStyles[8].styles[1]": "CornerRadius=13",
  "controlStyles[8].styles[2]": "Margin=0,5,4,5",
  "controlStyles[8].styles[3]": "Padding=2,0,-18,0",
  "controlStyles[9].target": "Taskbar.TaskListButton > Grid > Rectangle#RunningIndicator",
  "controlStyles[9].styles[0]": "Height=3",
  "controlStyles[9].styles[1]": "RadiusX=1.5",
  "controlStyles[9].styles[2]": "RadiusY=1.5",
  "controlStyles[9].styles[3]": "Fill@ActiveNormal=#facc15",
  "controlStyles[9].styles[4]": "VerticalAlignment=Bottom",
  "controlStyles[9].styles[5]": "Margin=16,0,16,4",
  "controlStyles[9].styles[6]": "StrokeThickness=0",
  "controlStyles[10].target": "SystemTray.ImageIconContent > Grid#ContainerGrid > Image",
  "controlStyles[10].styles[0]": "Width=13",
  "controlStyles[11].target": "SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock",
  "controlStyles[11].styles[0]": "FontSize=13",
  "controlStyles[11].styles[1]": "Foreground=#facc15",
  "controlStyles[12].target": "TextBlock#LabelControl",
  "controlStyles[12].styles[0]": "FontFamily=Segoe UI Medium",
  "controlStyles[12].styles[1]": "Foreground=#facc15",
  "controlStyles[12].styles[2]": "Margin=1,0,0,0",
  "controlStyles[12].styles[3]": "VerticalAlignment=Center",
  "controlStyles[12].styles[4]": "TextWrapping=NoWrap",
  "controlStyles[13].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton]",
  "controlStyles[13].styles[0]": "Visibility=Visible",
  "controlStyles[14].target": "Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock[Text=]",
  "controlStyles[14].styles[0]": "Text=",
  "controlStyles[14].styles[1]": "Foreground=#facc15",
  "controlStyles[15].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[15].styles[0]": "Fill=Transparent",
  "controlStyles[16].target": "Rectangle#BackgroundStroke",
  "controlStyles[16].styles[0]": "Fill=Transparent",
  "controlStyles[18].target": "SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock",
  "controlStyles[18].styles[0]": "Foreground=#facc15"
}

```

</details>

# ✦ Notes

- This theme is designed for dark, minimalistic desktop setups.
- Uses rounded corners (`CornerRadius=13`) for taskbar buttons and system tray.
- Accent color is golden yellow `#facc15`, used for text and icons.
- Some tray icons are intentionally hidden for a sleeker look.

# ✦ Highlighted Features

- Fully black background on taskbar buttons and system tray.
- Clean layout with hidden elements and padding adjustments.
- Compact and rounded system tray.

# ✦ Suggested Windows Settings

- Use default (centered) taskbar alignment.
- Set the dark theme.
- Set the gold accent color.
- Set display scale to 100% for best results.
- Hide unnecessary tray icons via Windows settings.

### ✦ Customize Icon-to-Text Spacing

If you'd like to adjust the distance between the app icon and its label (usually the app name), you can modify the following JSON property:

```json
"controlStyles[12].styles[2]": "Margin=1,0,0,0"
```

This Margin follows the format:
Margin=left,top,right,bottom

So, "Margin=1,0,0,0" sets 1 pixel of space between the icon and the text.


