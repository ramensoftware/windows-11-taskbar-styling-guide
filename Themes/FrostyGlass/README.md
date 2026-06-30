# ❄️ Windows 11 Taskbar Styler: Frosty Glass Edition
> A refined, translucent "Dock" experience for Windows 11 via Windhawk.

[![Windhawk](https://img.shields.io/badge/Requires-Windhawk-blue?style=flat-square)](https://windhawk.net/)
[![Style](https://img.shields.io/badge/Style-Frosty_Glass-lightgrey?style=flat-square)](#)

This configuration provides a modern **Frosty Glass** aesthetic for your Windows 11 taskbar. It utilizes custom translucent `AcrylicBrush` effects and manual layout adjustments to create a soft, blurred interface that feels perfectly integrated with the desktop environment.

---

## 📋 Prerequisites

1. Download and install [Windhawk](https://windhawk.net/).
2. Inside Windhawk, search for and install the **Windows 11 Taskbar Styler** mod by Ramen Software.
3. For the complete aesthetic and functionality shown in this repository, search for and install the following additional Windhawk mods:
   * **Taskbar tray system icon tweaks**
   * **Taskbar tray auto-hide (show on hover)**
   * **Taskbar height and icon size**
   * **Taskbar auto-hide when maximized**
   * **Taskbar Auto-Hide Instant Show**
   
---

## 🎨 Design Philosophy & Recommendations
This theme is crafted for a pure, minimal "Dock" aesthetic. To maintain the visual integrity and prevent layout breakage, please follow these recommendations:

* **Centralized Taskbar:** This theme is engineered specifically for a centered taskbar layout. Left-aligned taskbars are not supported and will break the aesthetic.
* **Minimalist Tray:** For the best results, keep the taskbar free of clutter. 
    * **Search:** If you must use Search, enable only the **Search box** (`Settings > Personalization > Taskbar > Taskbar items > Search > Search box`). Other search modes may cause UI inconsistencies.
    * **Widgets & Task View:** It is recommended to disable **Widgets** to maintain a clean layout. The **Task view** button is fully supported and works perfectly within this design.

## 📐 Screen Compatibility & Reference Setup
This configuration will work on **any device or resolution**. However, depending on your physical screen size and scaling, you may want to tweak certain values (like taskbar height or icon sizes) in the mods to perfectly align with your display.

For reference, the default values in this config and the screenshots below are based on my personal setup:
* **Device:** 14" Laptop (ROG Zephyrus G14 - 2024)
* **Resolution & Scaling:** 2880 x 1800 at 200%

---

## 🛠️ The Full Setup
For the complete minimal and smooth "Frosty Glass" experience, I use the following Windhawk mod ecosystem:

| Mod Name | Key Configuration Settings |
| :--- | :--- |
| **Taskbar tray system icon tweaks** | `Hide location icon` \| `Hide bell icon` \| `Show desktop width: 12` |
| **Taskbar tray auto-hide (show on hover)** | `Hidden opacity: 0` \| `Hide delay: 0` \| `Fade duration: 100` |
| **Taskbar height and icon size** | `Height: 54` \| `Icon Size: 31` \| `Button Width: 44` \| `Small Icon Size: 31` \| `Small Button Width: 44` |
| **Taskbar auto-hide when maximized** | `Mode: Auto-hide when maximized or intersects taskbar` |
| **Taskbar Auto-Hide Instant Show** | *See configuration below* |

Paste this into the **Advanced** tab of the **Taskbar Auto-Hide Instant Show** mod:

```json
{"animationType":"slideFade","showSpeedup":400,"hideSpeedup":400,"showDuration":100,"hideDuration":100,"frameRate":120,"unhideDelay":1,"hideDelay":1,"oldTaskbarOnWin11":0,"edgeDetection":0}

```

---

## 📦 Manual Installation

The theme styles can be imported manually by following these steps:

1. Open the **Windows 11 Taskbar Styler** (or relevant mod) in Windhawk.
2. Go to the **Settings** tab and select **Textual mode**.
3. Copy the content below and click **Save settings**.

<details>
<summary>Content to import (click to expand)</summary>

```yaml
theme: ''
styleConstants:
  - Background=<AcrylicBrush TintColor="#10000020"/>
  - BorderBrush2=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="{ThemeResource SystemChromeHighColor}" Offset="0.0" /><GradientStop Color="{ThemeResource SystemChromeLowColor}" Offset="0.25" /><GradientStop Color="{ThemeResource SystemChromeHighColor}" Offset="1" /></LinearGradientBrush>
  - BorderThickness=1
  - CornerRadius=10
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.25" /><GradientStop Color="#50808080" Offset="1" /></LinearGradientBrush>
  - Background2=<AcrylicBrush TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.3" FallbackColor="{ThemeResource SystemChromeAltHighColor}" />
  - TrayPadding=4.5,4,4.5,4
  - ElementBG=<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="0.3" />
  - ElementBorderThickness=1
  - ElementBorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="1" /><GradientStop Color="#50606060" Offset="0.15" /></LinearGradientBrush>
  - ElementCornerRadius=10
  - Background3=Transparent
  - BorderBrush3=Transparent
controlStyles:
  - target: Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid
    styles:
      - Margin=0,0,0,4
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - Background:=$Background
      - Padding=2,0,1.5,0
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Margin=3.5
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Margin=12,0,12,4
      - Background:=$Background
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - Padding=-1,0,-1,0
  - target: SystemTray.ChevronIconView
    styles:
      - Padding=$TrayPadding
      - CornerRadius=7
  - target: SystemTray.NotifyIconView#NotifyItemIcon
    styles:
      - Padding=$TrayPadding
      - CornerRadius=7
  - target: SystemTray.OmniButton
    styles:
      - Padding=$TrayPadding
      - CornerRadius=7
      - MaxWidth=Auto
  - target: SystemTray.CopilotIcon
    styles:
      - Padding=$TrayPadding
      - CornerRadius=7
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > systemtray:IconView#SystemTrayIcon > Grid
    styles:
      - Padding=2,2,5,4
      - CornerRadius=7
      - HorizontalAlignment=Center
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid
    styles:
      - Padding=$TrayPadding
      - CornerRadius=7
  - target: SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon
    styles:
      - Padding=$TrayPadding
      - CornerRadius=7
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Visibility=1
  - target: Taskbar.Gripper#GripperControl
    styles:
      - Width=Auto
      - MinWidth=Auto
  - target: SystemTray.SystemTrayFrame
    styles:
      - HorizontalAlignment=Right
      - CornerRadius=$CornerRadius
      - Width=Auto
  - target: Windows.UI.Xaml.Controls.Grid#AugmentedEntryPointContentGrid
    styles:
      - Margin=4,0,0,0
      - HorizontalAlignment=Auto
  - target: TextBlock#TimeInnerTextBlock
    styles:
      - FontSize=13
      - FontFamily=Segoe UI
      - Margin=0
      - Padding=0
      - RenderTransform:=<TranslateTransform X="4" Y="2" />
      - Width=Auto
      - MinWidth=Auto
      - HorizontalAlignment=Left
  - target: TextBlock#DateInnerTextBlock
    styles:
      - Visibility=1
      - RenderTransform:=<TranslateTransform X="4" Y="0" />
      - FontSize=11
      - FontFamily=Segoe UI
  - target: TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: TextBlock#SearchBoxTextBlock
    styles:
      - Text=Search
      - FontSize=10
      - FontFamily=vivo Sans EN VF
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
    styles:
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.Button
    styles:
      - BorderThickness=1
      - CornerRadius=7
  - target: Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
      - CornerRadius:=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Border
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar
    styles:
      - //RenderTransform:=<TranslateTransform X="0" Y="60" />
      - CornerRadius=$CornerRadius
      - Background:=$Background
  - target: Windows.UI.Xaml.Controls.Border#BackgroundDimmingLayer
    styles:
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Border#SnapBarBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - RenderTransform:=<TranslateTransform X="0" Y="10" />
      - Margin=0,0,0,-10
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Border#SnapPickerBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Border#SearchPillBackgroundElement
    styles:
      - BorderBrush:=$ElementBorderBrush
      - CornerRadius=$ElementCornerRadius
      - BorderThickness=$ElementBorderThickness
      - Margin=0
  - target: Taskbar.TaskbarExtensionElement
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
      - Padding=1.5,4,1.5,4
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius:=$CornerRadius
  - target: SearchUx.SearchUI.SearchButtonControl
    styles:
      - MaxWidth=130
      - Margin=-1,0,-1,0
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement > Windows.UI.Xaml.Controls.Grid#GridElement > Windows.UI.Xaml.Controls.Border#VirtualDesktopSwitcherBackground
    styles:
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid > Border
    styles:
      - Background:=$Background
      - CornerRadius=$CornerRadius
      - BorderThickness:=$BorderThickness
      - BorderBrush:=$BorderBrush
  - target: Border#VirtualDesktopBarBackground
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
      - Margin=0,0,0,-3
  - target: Border#HoverFlyoutBackground
    styles:
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - Background:=$Background
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=Transparent
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid
    styles:
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - Background:=$Background
  - target: Taskbar.TaskListButton#TaskListButton
    styles:
      - CornerRadius=7
      - Padding=$TrayPadding
      - Visibility=0
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - CornerRadius=7
      - Padding=$TrayPadding
      - Visibility=0
  - target: Taskbar.TaskbarFrame#TaskbarFrame
    styles:
      - HorizontalAlignment=Auto
      - Width=Auto
      - MinWidth:=500
      - MaxWidth:=900
      - Padding=1,0,1,0
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Visibility=0
  - target: Taskbar.TaskListLabeledButtonPanel > Border#BackgroundElement
    styles:
      - Visibility=0
  - target: Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton]
    styles:
      - Visibility=0
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: Taskbar.TaskItemThumbnailView > Grid@CommonStates > Border#BackgroundBorder
    styles:
      - CornerRadius:=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Windows.UI.Xaml.Controls.Grid#MainGrid > Windows.UI.Xaml.Controls.Border#MainBorder
    styles:
      - CornerRadius:=$CornerRadius
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - Background:=$Background
      - Margin=0,0,0,0
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Windows.UI.Xaml.Controls.Grid#MainGrid > Windows.UI.Xaml.Controls.Border#BorderHighlight
    styles:
      - CornerRadius:=$CornerRadius
      - Visibility=1
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Windows.UI.Xaml.Controls.Grid#MainGrid > Windows.UI.Xaml.Controls.Border#ActiveDesktopPill
    styles:
      - CornerRadius:=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed#NewVirtualDesktopButtonThemed > Windows.UI.Xaml.Controls.Grid#MainGrid > Windows.UI.Xaml.Controls.Border#MainBorder
    styles:
      - CornerRadius:=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed#NewVirtualDesktopButtonThemed > Windows.UI.Xaml.Controls.Grid#MainGrid > Windows.UI.Xaml.Controls.Border#BorderHighlight
    styles:
      - CornerRadius:=$CornerRadius
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$Background
      - CornerRadius:=$CornerRadius
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
  - target: Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - Background:=$Background
      - BorderThickness:=$BorderThickness
      - BorderBrush:=$BorderBrush
      - CornerRadius:=$CornerRadius
  - target: Taskbar.TaskbarFrame
    styles:
      - Width=Auto
      - HorizontalAlignment=Center
      - Margin=Auto
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius:=10
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Visibility=Collapsed
  - target: Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Margin=0
  - target: Taskbar.Gripper#GripperControl
    styles:
      - Width=Auto
      - MinWidth=24
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Background:=$Background
      - CornerRadius:=10
      - BorderThickness:=$BorderThickness
      - BorderBrush:=$BorderBrush
      - BackgroundSizing=InnerBorderEdge

```

</details>

---

## 📸 Showcase
*Here is the Frosty Glass dock taskbar in action:*

**Video Demonstration:**

https://github.com/user-attachments/assets/d1448b78-aadb-4d16-bca2-853ece6e96a7

https://github.com/user-attachments/assets/4e61b37f-efa9-460c-858c-0d7f0b29154d

**Theme Gallery:**

<img width="2876" height="1799" alt="Screenshot 2026-04-30 150608" src="https://github.com/user-attachments/assets/6db309dc-db2a-44a9-9343-6adcfe3cc2f0" />
<img width="1043" height="651" alt="Screenshot 2026-04-30 150622" src="https://github.com/user-attachments/assets/05a923bb-b7a9-4b3f-8739-b7c81d7dfbbf" /><img width="553" height="600" alt="image" src="https://github.com/user-attachments/assets/9e23aeae-22e4-4736-99cd-44c280004d8e" />
<img width="873" height="307" alt="image" src="https://github.com/user-attachments/assets/b0d3ff24-55cb-4cd0-b151-91cdf72bc46c" />
<img width="1066" height="553" alt="image" src="https://github.com/user-attachments/assets/d85aa313-ea82-4bf8-849b-cf001370b06d" />


---

## 🔗 Related Projects

Complete the look across your entire UI! Check out my other Frosty Glass styling repositories:
* [❄️ Frosty Glass Start Menu Styler](https://github.com/guidolamanna/win11-startmenu-styler-frostyglass-windhawk) to apply this exact same aesthetic to your Start Menu and Lock Screen!
* [❄️ Frosty Glass Notification Center Styler](https://github.com/guidolamanna/win11-notificationcenter-styler-frostyglass-windhawk) to theme your Notifications, Calendar, and Control Center flyouts!

---

## 🙌 Credits & Inspiration
A huge thank you to [Ramen Software](https://github.com/ramensoftware) for creating Windhawk. This configuration was heavily inspired by the official [Windows 11 Taskbar Styling Guide](https://github.com/ramensoftware/windows-11-taskbar-styling-guide) and the Windhawk modding community.

---
*Created by [Guido Lamanna](https://github.com/guidolamanna)*
