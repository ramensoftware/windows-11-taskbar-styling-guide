# WindowGlass theme for Windows 11 Taskbar Styler

A theme that adds a modern, glassy aesthetic with a compact, floating layout to the Windows 11 taskbar.

**Author**: [Nathaniel4JC](https://github.com/Nathaniel4JC)

![Screenshot](screenshot_large.png)

## Note
- This theme consists of the following backgrounds:
  - Translucent
  - Glass
  - Frosted
  - Acrylic

  In order to switch between these backgrounds, set the value `Background=$Translucent`, `Background=$Glass`, `Background=$Frosted` or `Background=$Acrylic` in the "Style constants" section of the mod's settings.
- The taskbar frame maximum width is limited to 1895px by default. To adjust this, set `TaskbarFrameMaxWidth` to your preferred value in the "Style constants" section of the mod's settings. For example: `TaskbarFrameMaxWidth=800` will cap the taskbar frame at 800px.
- In order to make the taskbar look better, it's best that you install the 'Taskbar height and icon size' mod and use the following settings for the mod:

  <details>
  <summary>Click to expand mod settings</summary>

  ```yaml
  TaskbarHeight: 70
  IconSize: 30
  TaskbarButtonWidth: 44
  IconSizeSmall: 20
  TaskbarButtonWidthSmall: 30
  ```
  </details>

## Bonus
This theme also styles additional parts of Windows 11, including:

- **Volume and Brightness HUD**

  ![Volume HUD](HUD_Volume.png) \
  ![Brightness HUD](HUD_Brightness.png)

- **Window Snap Layout HUD**

  ![Snap Layout Picker 1](Snap_Layout.png) \
  ![Snap Layout Picker 2](Snap_Layout_2.png) \
  ![Snap Layout Picker 3](Snap_Layout_1.png)

## More details about this theme
- Designed for Windows 11 24H2.
- Compatible with both light and dark modes.

## Complete WindowGlass-themed UI

For a complete WindowGlass-themed UI, download the following mods and use the 'WindowGlass' theme:

- Windows 11 Start Menu Styler - for styling the Start menu.
- Windows 11 Notification Center Styler - for styling the Notification Center and Action Center.
- Windows 11 File Explorer Styler - for styling Windows Explorer windows.

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
  - Translucent=<WindhawkBlur BlurAmount="15" TintColor="#10808080"/>
  - Glass=<WindhawkBlur BlurAmount="5" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Frosted=<WindhawkBlur BlurAmount="20" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Acrylic=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.8" />
  - Background=$Glass
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="0.0" /><GradientStop Color="#30404040" Offset="0.25" /><GradientStop Color="#40808080" Offset="1" /></LinearGradientBrush>
  - BorderBrush2=<WindhawkBlur BlurAmount="10" TintColor="#909090" TintOpacity="0.2"/>
  - ElementBG=<SolidColorBrush Color="{ThemeResource SystemChromeLowColor}" Opacity="0.3" />
  - ElementBorderThickness=0.3,0.3,0.3,1
  - ElementBorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="1" /><GradientStop Color="#50606060" Offset="0.15" /></LinearGradientBrush>
  - ElementCornerRadius=12
  - ElementSysColor=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight1}" Opacity="1" />
  - ElementSysColor2=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight2}" Opacity="1" />
  - ElementSysColor3=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="1" />
  - ElementSysColor4=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" Opacity="1" />
  - BorderThickness=0.5,1,0.5,1
  - CornerRadius=25
  - TrayPadding=2,4,2,4
  - Height=70
  - TaskbarFrameMaxWidth=1895
controlStyles:
  - target: Taskbar.TaskbarFrame
    styles:
      - MaxWidth:=$TaskbarFrameMaxWidth
      - Width=Auto
      - MinWidth:=100
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Margin=10,2,10,2
      - BorderThickness=$BorderThickness
      - //BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - Background:=$Background
      - Padding=10,0,235,0
  - target: Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Margin=0,8,0,8
      - Background:=Transparent
      - CornerRadius=0
      - BorderThickness=0,0,1,0
      - BorderBrush:=#20808080
      - Padding=2,0,5,0
      - MaxWidth:=200
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Margin=-240,10,0,10
      - Background:=Transparent
      - BorderBrush:=#20808080
      - BorderThickness=1,0,0,0
      - CornerRadius=0
      - Padding=0,0,10,0
  - target: SystemTray.ChevronIconView
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
      - Margin=5,0,0,0
  - target: SystemTray.NotifyIconView#NotifyItemIcon
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
      - Margin=5,0,0,0
  - target: SystemTray.OmniButton
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
  - target: SystemTray.CopilotIcon
    styles:
      - Padding=$TrayPadding
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > systemtray:IconView#SystemTrayIcon > Grid
    styles:
      - Padding=$TrayPadding
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid
    styles:
      - Padding=10
      - CornerRadius=10
  - target: SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon
    styles:
      - Padding=0
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Visibility=Visible
  - target: Taskbar.Gripper#GripperControl
    styles:
      - Width=Auto
      - MinWidth=24
  - target: Windows.UI.Xaml.Controls.Grid#AugmentedEntryPointContentGrid
    styles:
      - Margin=4,0,0,0
  - target: TextBlock#TimeInnerTextBlock
    styles:
      - FontSize=13
      - FontFamily=vivo Sans EN VF
      - Margin=0
      - Padding=0
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: TextBlock#DateInnerTextBlock
    styles:
      - Visibility=Collapsed
      - RenderTransform:=<TranslateTransform X="0" Y="-9" />
      - FontSize=11
      - FontFamily=vivo Sans EN VF
  - target: TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - CornerRadius=22
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
  - target: TextBlock#SearchBoxTextBlock
    styles:
      - Text=Search
      - FontSize=10
      - FontFamily=vivo Sans EN VF
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Button
    styles:
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background=Transparent
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList
    styles:
      - Background:=$Background
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar > Grid > Border
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar
    styles:
      - Width=Auto
      - Visibility=Visible
      - HorizontalAlignment=1
  - target: Windows.UI.Xaml.Controls.Border#BackgroundDimmingLayer
    styles:
      - Background:=Transparent
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - CornerRadius=10
  - target: Taskbar.TaskListButton#TaskListButton
    styles:
      - CornerRadius=10
  - target: Windows.UI.Xaml.Controls.Border#SnapBarBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - RenderTransform:=<TranslateTransform X="0" Y="10" />
      - Margin=0,0,0,-10
  - target: Windows.UI.Xaml.Controls.Border#SnapPickerBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Border#SearchPillBackgroundElement
    styles:
      - BorderBrush:=$ElementBorderBrush
      - CornerRadius=$ElementCornerRadius
      - BorderThickness=$ElementBorderThickness
      - MaxWidth:=100
      - Width=Auto
  - target: Taskbar.TaskbarExtensionElement
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius=12
  - target: SearchUx.SearchUI.SearchButtonControl
    styles:
      - MaxWidth:=300
      - MinWidth:=10
      - Width=Auto
      - Margin=0
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement > Windows.UI.Xaml.Controls.Grid#GridElement > Windows.UI.Xaml.Controls.Border#VirtualDesktopSwitcherBackground
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill
    styles:
      - Fill:=$Background
  - target: SystemTray.SystemTrayFrame
    styles:
      - Grid.Column=2
  - target: Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Grid#HoverFlyoutGrid > Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground
    styles:
      - Background:=Transparent
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.ScrollContentPresenter > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.Grid
    styles:
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
  - target: Taskbar.TaskbarFrame
    styles:
      - Grid.Column=1
      - Width=Auto
      - MaxWidth=$TaskbarFrameMaxWidth
```
</details>

### Split variant
This theme includes an alternate split variant with a separated taskbar and system tray.

![Split variant](screenshot_split.png)

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - Translucent=<WindhawkBlur BlurAmount="15" TintColor="#10808080"/>
  - Glass=<WindhawkBlur BlurAmount="5" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Frosted=<WindhawkBlur BlurAmount="20" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Acrylic=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.8" />
  - Background=$Glass
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="0.0" /><GradientStop Color="#30404040" Offset="0.25" /><GradientStop Color="#40808080" Offset="1" /></LinearGradientBrush>
  - BorderBrush2=<WindhawkBlur BlurAmount="10" TintColor="#909090" TintOpacity="0.2"/>
  - ElementBG=<SolidColorBrush Color="{ThemeResource SystemChromeLowColor}" Opacity="0.3" />
  - ElementBorderThickness=0.3,0.3,0.3,1
  - ElementBorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="1" /><GradientStop Color="#50606060" Offset="0.15" /></LinearGradientBrush>
  - ElementCornerRadius=12
  - ElementSysColor=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight1}" Opacity="1" />
  - ElementSysColor2=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight2}" Opacity="1" />
  - ElementSysColor3=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="1" />
  - ElementSysColor4=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" Opacity="1" />
  - BorderThickness=0.5,1,0.5,1
  - CornerRadius=25
  - TrayPadding=2,4,2,4
  - Height=70
  - TaskbarFrameMaxWidth=1895
controlStyles:
  - target: Taskbar.TaskbarFrame
    styles:
      - MaxWidth:=$TaskbarFrameMaxWidth
      - Width=Auto
      - MinWidth:=100
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Margin=10,2,3,2
      - BorderThickness=$BorderThickness
      - //BorderBrush:=$BorderBrush
      - CornerRadius=25,5,5,25
      - Background:=$Background
      - Padding=10,0,0,0
  - target: Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Margin=0,8,0,8
      - Background:=Transparent
      - CornerRadius=0
      - BorderThickness=0,0,1,0
      - BorderBrush:=#20808080
      - Padding=2,0,5,0
      - MaxWidth:=200
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Margin=0,2,3,2
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=5,25,25,5
      - Padding=0,0,10,0
  - target: SystemTray.ChevronIconView
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
      - Margin=5,0,0,0
  - target: SystemTray.NotifyIconView#NotifyItemIcon
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
      - Margin=5,0,0,0
  - target: SystemTray.OmniButton
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
  - target: SystemTray.CopilotIcon
    styles:
      - Padding=$TrayPadding
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > systemtray:IconView#SystemTrayIcon > Grid
    styles:
      - Padding=$TrayPadding
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid
    styles:
      - Padding=10
      - CornerRadius=10
  - target: SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon
    styles:
      - Padding=0
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Visibility=Visible
  - target: Taskbar.Gripper#GripperControl
    styles:
      - Width=Auto
      - MinWidth=24
  - target: Windows.UI.Xaml.Controls.Grid#AugmentedEntryPointContentGrid
    styles:
      - Margin=4,0,0,0
  - target: TextBlock#TimeInnerTextBlock
    styles:
      - FontSize=13
      - FontFamily=vivo Sans EN VF
      - Margin=0
      - Padding=0
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: TextBlock#DateInnerTextBlock
    styles:
      - Visibility=Collapsed
      - RenderTransform:=<TranslateTransform X="0" Y="-9" />
      - FontSize=11
      - FontFamily=vivo Sans EN VF
  - target: TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - CornerRadius=22
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
  - target: TextBlock#SearchBoxTextBlock
    styles:
      - Text=Search
      - FontSize=10
      - FontFamily=vivo Sans EN VF
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Button
    styles:
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background=Transparent
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList
    styles:
      - Background:=$Background
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar > Grid > Border
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar
    styles:
      - Width=Auto
      - Visibility=Visible
      - HorizontalAlignment=1
  - target: Windows.UI.Xaml.Controls.Border#BackgroundDimmingLayer
    styles:
      - Background:=Transparent
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - CornerRadius=10
  - target: Taskbar.TaskListButton#TaskListButton
    styles:
      - CornerRadius=10
  - target: Windows.UI.Xaml.Controls.Border#SnapBarBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - RenderTransform:=<TranslateTransform X="0" Y="10" />
      - Margin=0,0,0,-10
  - target: Windows.UI.Xaml.Controls.Border#SnapPickerBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Border#SearchPillBackgroundElement
    styles:
      - BorderBrush:=$ElementBorderBrush
      - CornerRadius=$ElementCornerRadius
      - BorderThickness=$ElementBorderThickness
      - MaxWidth:=100
      - Width=Auto
  - target: Taskbar.TaskbarExtensionElement
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius=12
  - target: SearchUx.SearchUI.SearchButtonControl
    styles:
      - MaxWidth:=300
      - MinWidth:=10
      - Width=Auto
      - Margin=0
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement > Windows.UI.Xaml.Controls.Grid#GridElement > Windows.UI.Xaml.Controls.Border#VirtualDesktopSwitcherBackground
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill
    styles:
      - Fill:=$Background
  - target: SystemTray.SystemTrayFrame
    styles:
      - Grid.Column=2
  - target: Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Grid#HoverFlyoutGrid > Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground
    styles:
      - Background:=Transparent
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.ScrollContentPresenter > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.Grid
    styles:
      - ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width="*"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="Auto"/><ColumnDefinition Width="*"/></ColumnDefinitionCollection>
  - target: Taskbar.TaskbarFrame
    styles:
      - Grid.Column=1
      - Width=Auto
      - MaxWidth=$TaskbarFrameMaxWidth
```
</details>

### Full-Length variant

This theme also has a Full-Length variant, which stretches to the corners of the screen.

![Full-Length variant](screenshot_full.png)

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - Translucent=<WindhawkBlur BlurAmount="15" TintColor="#10808080"/>
  - Glass=<WindhawkBlur BlurAmount="5" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Frosted=<WindhawkBlur BlurAmount="20" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Acrylic=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.8" />
  - Background=$Glass
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="0.0" /><GradientStop Color="#30404040" Offset="0.25" /><GradientStop Color="#40808080" Offset="1" /></LinearGradientBrush>
  - BorderBrush2=<WindhawkBlur BlurAmount="10" TintColor="#909090" TintOpacity="0.2"/>
  - ElementBG=<SolidColorBrush Color="{ThemeResource SystemChromeLowColor}" Opacity="0.3" />
  - ElementBorderThickness=0.3,0.3,0.3,1
  - ElementBorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="1" /><GradientStop Color="#50606060" Offset="0.15" /></LinearGradientBrush>
  - ElementCornerRadius=12
  - ElementSysColor=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight1}" Opacity="1" />
  - ElementSysColor2=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight2}" Opacity="1" />
  - ElementSysColor3=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="1" />
  - ElementSysColor4=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" Opacity="1" />
  - BorderThickness=0.5,1,0.5,1
  - CornerRadius=20
  - TrayPadding=2,4,2,4
  - Height=70
controlStyles:
  - target: Taskbar.TaskbarFrame
    styles:
      - //MaxWidth:=1895
      - Width=Auto
      - MinWidth:=100
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Margin=10,2,10,2
      - BorderThickness=$BorderThickness
      - //BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - Background:=$Background
      - Padding=0
  - target: Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarBackground#BackgroundControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Margin=0,10,0,10
      - Background:=Transparent
      - CornerRadius=0
      - BorderThickness=1,0,1,0
      - BorderBrush:=#20808080
      - Padding=2,0,5,0
      - MaxWidth:=200
  - target: Grid#SystemTrayFrameGrid
    styles:
      - Margin=0,8,8,7
      - Background:=Transparent
      - BorderBrush:=Transparent
      - BorderThickness=$ElementBorderThickness
      - CornerRadius=$ElementCornerRadius
  - target: SystemTray.ChevronIconView
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
      - Margin=5,0,0,0
  - target: SystemTray.NotifyIconView#NotifyItemIcon
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
      - Margin=5,0,0,0
  - target: SystemTray.OmniButton
    styles:
      - Padding=$TrayPadding
      - CornerRadius=10
  - target: SystemTray.CopilotIcon
    styles:
      - Padding=$TrayPadding
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > systemtray:IconView#SystemTrayIcon > Grid
    styles:
      - Padding=$TrayPadding
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid
    styles:
      - Padding=10
      - CornerRadius=10
  - target: SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon
    styles:
      - Padding=0
  - target: SystemTray.Stack#ShowDesktopStack
    styles:
      - Visibility=Visible
  - target: Taskbar.Gripper#GripperControl
    styles:
      - Width=Auto
      - MinWidth=24
  - target: Windows.UI.Xaml.Controls.Grid#AugmentedEntryPointContentGrid
    styles:
      - Margin=4,0,0,0
      - HorizontalAlignment=Left
  - target: TextBlock#TimeInnerTextBlock
    styles:
      - FontSize=13
      - FontFamily=vivo Sans EN VF
      - Margin=0
      - Padding=0
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: TextBlock#DateInnerTextBlock
    styles:
      - Visibility=Collapsed
      - RenderTransform:=<TranslateTransform X="0" Y="-9" />
      - FontSize=11
      - FontFamily=vivo Sans EN VF
  - target: TextBlock#InnerTextBlock[Text=]
    styles:
      - Text=
  - target: Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid
    styles:
      - CornerRadius=22
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
  - target: TextBlock#SearchBoxTextBlock
    styles:
      - Text=Search
      - FontSize=10
      - FontFamily=vivo Sans EN VF
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Button
    styles:
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background=Transparent
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Grid#ModalRootGrid > Windows.UI.Xaml.Controls.Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList
    styles:
      - Background:=$Background
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar > Grid > Border
    styles:
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
      - CornerRadius=$CornerRadius
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar
    styles:
      - Width=Auto
      - Visibility=Visible
      - HorizontalAlignment=1
  - target: Windows.UI.Xaml.Controls.Border#BackgroundDimmingLayer
    styles:
      - Background:=Transparent
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - CornerRadius=10
  - target: Taskbar.TaskListButton#TaskListButton
    styles:
      - CornerRadius=10
  - target: Windows.UI.Xaml.Controls.Border#SnapBarBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - RenderTransform:=<TranslateTransform X="0" Y="10" />
      - Margin=0,0,0,-10
  - target: Windows.UI.Xaml.Controls.Border#SnapPickerBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Border#SearchPillBackgroundElement
    styles:
      - BorderBrush:=$ElementBorderBrush
      - CornerRadius=$ElementCornerRadius
      - BorderThickness=$ElementBorderThickness
      - MaxWidth:=100
      - Width=Auto
  - target: Taskbar.TaskbarExtensionElement
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius=12
  - target: SearchUx.SearchUI.SearchButtonControl
    styles:
      - MaxWidth:=300
      - MinWidth:=10
      - Width=Auto
      - Margin=0
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement > Windows.UI.Xaml.Controls.Grid#GridElement > Windows.UI.Xaml.Controls.Border#VirtualDesktopSwitcherBackground
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundFill
    styles:
      - Fill:=$Background
  - target: Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Grid#HoverFlyoutGrid > Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground
    styles:
      - Background:=Transparent
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
```
</details>
