# The Windows 11 taskbar styling guide

## Table of contents

* [Introduction](#introduction)
  * [Finding targets](#finding-targets)
  * [Missing customizations](#missing-customizations)
  * [Contributing](#contributing)
* [Themes](#themes)
* [General](#general)
  * [Taskbar size](#taskbar-size)
  * [Taskbar background](#taskbar-background)
  * [Taskbar border](#taskbar-border)
* [Task list](#task-list)
  * [Start button image](#start-button-image)
  * [Hide the start button](#hide-the-start-button)
  * [Task list buttons size](#task-list-buttons-size)
  * [Task list buttons corner radius](#task-list-buttons-corner-radius)
  * [Task list labels](#task-list-labels)
  * [Task list labels font](#task-list-labels-font)
  * [Task list running indicator](#task-list-running-indicator)
* [Notification area (system tray)](#notification-area-system-tray)
  * [Tray icons size](#tray-icons-size)
  * [Tray icons size (system icons)](#tray-icons-size-system-icons)
  * [Tray icons spacing](#tray-icons-spacing)
  * [Tray icons padding](#tray-icons-padding)
  * [Tray icons padding (system icons)](#tray-icons-padding-system-icons)
  * [Hide the network icon](#hide-the-network-icon)
  * [Hide the volume icon](#hide-the-volume-icon)
  * [Chevron icon width](#chevron-icon-width)
  * [Clock](#clock)
  * [Hide the notification bell icon](#hide-the-notification-bell-icon)
  * [Copilot button image](#copilot-button-image)
  * [Hide the "Show Desktop" button](#hide-the-show-desktop-button)
* [Colors](#colors)
  * [Solid color](#solid-color)
  * [Accent colors](#accent-colors)
  * [Transparent color](#transparent-color)
  * [Acrylic effect as color](#acrylic-effect-as-color)
  * [Mica effect as color](#mica-effect-as-color)
  * [Gradient as color](#gradient-as-color)
  * [Image as color](#image-as-color)

## Introduction

This is a collection of commonly requested taskbar styling customizations for
Windows 11. It is intended to be used with the [Windows 11 Taskbar
Styler](https://windhawk.net/mods/windows-11-taskbar-styler) Windhawk mod.

If you're not familiar with Windhawk, here are the steps for installing the mod:

* Download Windhawk from [windhawk.net](https://windhawk.net/) and install it.
* Go to "Mods" in the upper right menu.
* Find and install the "Windows 11 Taskbar Styler" mod.

After installing the mod, open its Settings tab and adjust the styles according
to your preferences.

Some customizations are best to be adjusted with other Windhawk mods. Links to
those mods are provided where applicable.

**See also**: [The Windows 11 start menu styling
guide](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/blob/main/README.md),
[The Windows 11 notification center styling
guide](https://github.com/ramensoftware/windows-11-notification-center-styling-guide/blob/main/README.md).

### Finding Targets

[How to find targets using UWPSpy](https://github.com/bbmaster123/FWFU/blob/main/uwpspy.md).

### Missing customizations

If you're looking for a customization that is not listed here, please [open an
issue](https://github.com/ramensoftware/windows-11-taskbar-styling-guide/issues/new).

### Contributing

If you have a taskbar styling customization or theme that you would like to
share, please submit a pull request.

## Themes

Themes are collections of styles that can be imported into the Windows 11
Taskbar Styler mod. The following themes are available:

| Link  | Screenshot
| ----- | ----------
| [WinXP](Themes/WinXP/README.md) | [![WinXP](Themes/WinXP/screenshot-small.png)](Themes/WinXP/screenshot.png)
| [Bubbles](Themes/Bubbles/README.md) | [![Bubbles](Themes/Bubbles/screenshot.png)](Themes/Bubbles/screenshot.png)
| [TranslucentTaskbar](Themes/TranslucentTaskbar/README.md) | [![TranslucentTaskbar](Themes/TranslucentTaskbar/screenshot.png)](Themes/TranslucentTaskbar/screenshot.png)
| [Squircle](Themes/Squircle/README.md) | [![Squircle](Themes/Squircle/screenshot.png)](Themes/Squircle/screenshot.png)
| [RosePine](Themes/RosePine/README.md) | [![RosePine](Themes/RosePine/screenshot.png)](Themes/RosePine/screenshot.png)
| [DockLike](Themes/DockLike/README.md) | [![DockLike](Themes/DockLike/screenshot.png)](Themes/DockLike/screenshot.png)
| [WinVista](Themes/WinVista/README.md) | [![WinVista](Themes/WinVista/screenshot.png)](Themes/WinVista/screenshot.png)
| [CleanSlate](Themes/CleanSlate/README.md) | [![CleanSlate](Themes/CleanSlate/screenshot.png)](Themes/CleanSlate/screenshot.png)
| [BottomDensy](Themes/BottomDensy/README.md) | [![BottomDensy](Themes/BottomDensy/screenshot.png)](Themes/BottomDensy/screenshot.png)
| [Lucent](Themes/Lucent/README.md) | [![Lucent](Themes/Lucent/screenshot.png)](Themes/Lucent/screenshot.png)
| [21996Taskbar](Themes/21996Taskbar/README.md) | [![21996Taskbar](Themes/21996Taskbar/screenshot.png)](Themes/21996Taskbar/screenshot.png)
| [TaskbarXII](Themes/TaskbarXII/README.md) | [![TaskbarXII](Themes/TaskbarXII/screenshot.png)](Themes/TaskbarXII/screenshot.png)
| [xdark](Themes/xdark/README.md) | [![xdark](Themes/xdark/screenshot.png)](Themes/xdark/screenshot.png)
## General

### Taskbar size

Use the [Taskbar height and icon
size](https://windhawk.net/mods/taskbar-icon-size) mod.

### Taskbar background

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
```

To set a solid color background, use the following style:
```
Fill=<color>
```

Replace `<color>` with the desired color. See [colors section](#colors) for all
options (e.g. if you want blurred background effect).

> [!NOTE]  
> For some themes, a different target has to be used to customize the taskbar
> background:
> * The [WinXP](Themes/WinXP/README.md) theme spans the taskbar border over the
>   full taskbar height. To customize the background, use the
>   `Rectangle#BackgroundStroke` target.
> * The [DockLike](Themes/DockLike/README.md) theme hides the standard taskbar
>   background element. To customize the background, use the `Grid#RootGrid`
>   target and the `Background=<color>` style.

> [!NOTE]  
> There's [a known
> limitation](https://github.com/ramensoftware/windhawk-mods/issues/742) which
> makes some styles, such as an acrylic background, only work if there's a
> single taskbar. The [Taskbar Background
> Helper](https://windhawk.net/mods/taskbar-background-helper) mod can be used
> as a workaround.

### Taskbar border

Target:
```
Rectangle#BackgroundStroke
```

It can be customized in the same way as the background, see [Taskbar
background](#taskbar-background).

## Task list

### Start button image

Target:
```
Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel > Border#BackgroundElement
```
Style:
```
Background:=<ImageBrush Stretch="Uniform" ImageSource="<image>" />
```
Target:
```
Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel > Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer#Icon
```
Style:
```
Visibility=Collapsed
```

Replace `<image>` with your own image, a local file path or a URL, for example:
* Windows 10: `https://i.imgur.com/lEvZStx.png`.
* Windows XP: `https://i.imgur.com/RX5DqT3.png` (use with `Stretch="None"`).

To set a different image for each Start button state - normal, hovered, pressed -
refer to [this
comment](https://github.com/ramensoftware/windows-11-taskbar-styling-guide/issues/153#issuecomment-2569892017).

### Hide the start button

Target:
```
Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton]
```
Style:
```
Visibility=Collapsed
```

### Task list buttons size

Use the [Taskbar height and icon
size](https://windhawk.net/mods/taskbar-icon-size) mod.

### Task list buttons corner radius

Targets:
```
Taskbar.ExperienceToggleButton
```
```
Taskbar.SearchBoxButton
```
```
Taskbar.TaskListButton
```
Style:
```
CornerRadius=<radius>
```

Replace `<radius>` with the desired radius. A larger value will make the corners
more rounded. Default: 4.

### Task list labels

Various task list label customizations are available in the [Taskbar Labels for
Windows 11](https://windhawk.net/mods/taskbar-labels) mod.

### Task list labels font

Target:
```
TextBlock#LabelControl
```
Style:
```
FontFamily=<font>
```

Replace `<font>` with the desired font. For a list of fonts that are shipped
with Windows 11, refer to [this page](
https://learn.microsoft.com/en-us/typography/fonts/windows_11_font_list).

### Task list running indicator

Target:
```
Taskbar.TaskListLabeledButtonPanel@RunningIndicatorStates > Rectangle#RunningIndicator
```

Various styles can be applied to the running indicator. Here are some examples:

Styles:
```
Fill=#FFED7014
```
```
Height=2
```
```
Width=12
```
```
Fill@ActiveRunningIndicator=Red
```
```
Width@ActiveRunningIndicator=20
```

The following visual states[^1] can be used:
* `ActiveRunningIndicator`
* `InactiveRunningIndicator`
* `RequestingAttentionRunningIndicator`

Some customizations for the running indicator are available in the [Taskbar
Labels for Windows 11](https://windhawk.net/mods/taskbar-labels) mod.

## Notification area (system tray)

### Tray icons size

Target:
```
SystemTray.ImageIconContent > Grid#ContainerGrid > Image
```
Styles:
```
Width=<size>
```
```
Height=<size>
```

Replace `<size>` with the desired size. Default: 16.

### Tray icons size (system icons)

Target:
```
SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock
```
Style:
```
FontSize=<size>
```

Replace `<size>` with the desired size. Default: 32.

### Tray icons spacing

Target:
```
SystemTray.NotifyIconView#NotifyItemIcon
```
Style:
```
MinWidth=<width>
```

Replace `<width>` with the desired width for the icon and the spacing. Default:
32.

### Tray icons padding

Target:
```
SystemTray.ImageIconContent > Grid#ContainerGrid
```
Style:
```
Padding=<padding>
```

To reduce the spacing even more, replace `<padding>` with the desired padding.
Default: `4,0`.

### Tray icons padding (system icons)

Target:
```
SystemTray.TextIconContent > Grid#ContainerGrid
```
Style:
```
Padding=<padding>
```

Replace `<padding>` with the desired padding. Default: `4,0`.

### Hide the network icon

Target:
```
SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[1] > SystemTray.IconView > Grid > Grid
```
Style:
```
Visibility=Collapsed
```

### Hide the volume icon

Target:
```
SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[2] > SystemTray.IconView > Grid > Grid
```
Style:
```
Visibility=Collapsed
```

### Chevron icon width

Target:
```
SystemTray.ChevronIconView
```
Style:
```
MinWidth=<width>
```

Replace `<width>` with the desired width. Default: 32.

### Clock

Clock customizations are available in the [Taskbar Clock
Customization](https://windhawk.net/mods/taskbar-clock-customization) mod.

### Hide the notification bell icon

Target:
```
SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent
```
Style:
```
Visibility=Collapsed
```

### Copilot button image

Target:
```
ContentPresenter#ContentPresenter > Grid#ContentGrid > Microsoft.UI.Xaml.Controls.AnimatedVisualPlayer#LottieIcon
```
Style:
```
Visibility=Collapsed
```
Target:
```
SystemTray.CopilotIcon#CopilotIcon > Grid#ContainerGrid > Border#BackgroundBorder
```
Style:
```
Background:=<ImageBrush Stretch="None" ImageSource="<image>" />
```

* Copilot icon without preview label: `https://i.imgur.com/lfwEWzI.png`.
* Old Copilot icon: `https://i.imgur.com/Z6eCNH3.png`.

### Hide the "Show Desktop" button

Target:
```
SystemTray.Stack#ShowDesktopStack
```
Style:
```
Visibility=Collapsed
```

# Colors

In the following examples we're gonna use `Fill` as an example, but this also
works for other properties that accept colors like `Background`.

### Solid color

```
Fill=<color>
```

Replace `<color>` with the desired color.

A color can be a name (e.g. `Red`) or a hex code (e.g. `#FF0000`).

The color can be semi-transparent (e.g. `#80FF0000`). To have a fully
transparent background, use `Transparent`.

### Accent colors

A Color can also be a `ThemeResource` or `StaticResource`. There are many such
styles built into Windows.

```
Fill:=<SolidColorBrush Color="{ThemeResource SystemAccentColor}" Opacity="0.8" />
```

Accent colors have different lightness available, like `SystemAccentColorLight2`
or `SystemAccentColorDark1`. The word `Light` or `Dark` is appended at end with
a number ranging from 1-3. Check out [the official Microsoft
docs](https://learn.microsoft.com/en-us/windows/apps/design/style/color#accent-color-palette)
for all variations.

```
Fill:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark2}" Opacity="0.5" />
```

### Transparent color

To have a fully transparent background, use the following style:

```
Fill=Transparent
```

### Acrylic effect as color

In order to have an acrylic effect (a blurred background) you can use
`AcrylicBrush`, this comes with `TintOpacity` which defines how much of the
color needs to be applied.

```
Fill:=<AcrylicBrush TintColor="Black" TintOpacity="0.8" />
```

You can also mix acrylic with a variation of an accent color for a more dynamic
look that fits current theme.

```
Fill:=<AcrylicBrush TintColor="{ThemeResource SystemAccentColorDark2}" TintOpacity="0.3" />
```

### Mica effect as color

> [!NOTE]
> Unfortunately I haven't figured this out yet. If you have any info please
> contribute by making a pull request.

### Gradient as color

The background can also be a gradient. For example, to have a gradient from
yellow to red to blue to lime green, use the following style:

```
Fill:=<LinearGradientBrush StartPoint="0,0.5" EndPoint="1,0.5"><GradientStop Color="Yellow" Offset="0.0" /><GradientStop Color="Red" Offset="0.25" /><GradientStop Color="Blue" Offset="0.75" /><GradientStop Color="LimeGreen" Offset="1.0" /></LinearGradientBrush>
```

### Image as color

The background can also be an image:

```
Fill:=<ImageBrush Stretch="UniformToFill" ImageSource="<image>" />
```

Replace `<image>` with your own image, a URL or a local file path.

[^1]: See [Finding Targets](#finding-targets) on how to use UWPSpy to find all of the available visual states for an element
