# LumiPill theme for Windows 11 Taskbar Styler

LumiPill is an auto-width single-pill floating dock theme that expands and shrinks
with your open taskbar apps. It pairs a light/dark adaptive translucent blur
backdrop with top-to-bottom specular gradient rim borders, compact clock-only
pills on secondary monitors, and Windows 11 26H2 Search button alignment.

**Author**: [Eureka-o](https://github.com/Eureka-o)

**Credits**: Built upon the floating dock, flyout, and system UI foundations of
[Luminosity](https://github.com/ramensoftware/windows-11-taskbar-styling-guide/tree/main/Themes/Luminosity)
by [mendes.image](https://github.com/mendesimage).

![LumiPill taskbar](screenshot.png)

## Notes

* Tested on **Windows 11 26H2** with **Windows 11 Taskbar Styler** `1.11.2`.
* Enable **Click-through taskbar** in the mod's settings so mouse clicks pass
  through the transparent area outside the floating dock pill.
* Uses standard dock sizing (`DockHeight=58`, `DockTopGap=5`, `DockBottomGap=5`)
  out of the box without requiring extra taskbar-height mods.
* **Tight fit on all monitors**: Set `MinDockWidth=0` under **Style constants**
  if you want the primary monitor dock to shrink strictly to its content instead
  of keeping a `900` DIP minimum width.
* **Hover magnification headroom**: If you pair this theme with **Taskbar Dock
  Animation** and **Taskbar height and icon size** (`TaskbarHeight: 78`), set
  `DockHeight=78` and `DockTopGap=25` under **Style constants** to give magnified
  icons transparent headroom above the pill.
* Companion theme: designed to match **LumiPill** for Windows 11 Start Menu Styler.

## Theme selection

The theme is integrated into the mod and can be selected directly from the
mod's settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select **LumiPill** as the theme, enable **Click-through taskbar**, and save
  the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box, enable **Click-through taskbar**, and
  click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - DockMargin=250
  - DockHeight=58
  - DockTopGap=5
  - DockBottomGap=5
  - WidgetGap=-
  - MenuAnimation=True
  - FadeSpeed=0:0:0.200
  - lumiBackground=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.55" TintLuminosityOpacity="0.40" NoiseOpacity="0.02" FallbackColor="{ThemeResource SystemChromeMediumColor}" />
  - lumiAccentColor=<SolidColorBrush Color="{ThemeResource LumiAccent}" />
  - wcr=20
  - mcr=15
  - bcr=10
  - t=Transparent
  - bb={ThemeResource LumiBorderBrush}
  - bt=1
  - bbb=<LinearGradientBrush x:Key="ShellTaskbarItemGradientStrokeColorSecondaryBrush" MappingMode="Absolute" StartPoint="0,0" EndPoint="0,3"><LinearGradientBrush.GradientStops><GradientStop Offset="0.33" Color="#1AFFFFFF" /><GradientStop Offset="1" Color="#0FFFFFFF" /></LinearGradientBrush.GradientStops></LinearGradientBrush>
  - bbt=2
  - bso=<SolidColorBrush Color="{ThemeResource ControlFillColorDefault}" />
  - bn=Transparent
  - bh=<SolidColorBrush Color="{ThemeResource ControlFillColorSecondary}" />
  - bp=<SolidColorBrush Color="{ThemeResource ControlFillColorTertiary}" />
  - TrayInFrame=(TrayInFrameWidth==``?0:taskbarDock!=`vertical`)
  - LeftAligned=(LumiStartWidth==``?0:LumiStartInnerWidth==``?0:LumiStartInnerWidth<=0?0:LumiStartWidth-LumiStartInnerWidth>8)
  - ClockOnlyDock=max((DockSecondaryClockWidth==``?0:DockSecondaryClockWidth>0),(TrayInFrameWidth==``?0:DockClockButtonWidth==``?0:DockClockButtonWidth>0?TrayInFrameWidth<=DockClockButtonWidth+24:0))
  - MinDockWidth=($ClockOnlyDock?0:900)
  - DockEdgeGap=16
  - DockLeftPad=($ClockOnlyDock?56:40)
  - DockMiddleGap=52
  - DockRightPad=($ClockOnlyDock?2:0)
  - DockReady=(DockContainerWidth==``?0:DockRepeaterWidth==``?0:DockContainerWidth>0?DockRepeaterWidth>0:0)
  - DockNaturalWidth=(DockRepeaterWidth+$DockLeftPad+$DockMiddleGap+$DockRightPad)
  - DockWidth=min(max($DockNaturalWidth,$MinDockWidth),DockContainerWidth-2*$DockEdgeGap)
  - DockSideMargin=max((DockContainerWidth-$DockWidth)/2,$DockEdgeGap)
  - MainIconBalance=($ClockOnlyDock?0:($DockMiddleGap-$DockLeftPad+max($DockWidth-$DockNaturalWidth,0)+9.5)/2)
  - TrayExtraShift=($DockMiddleGap+max($DockWidth-$DockNaturalWidth,0)-$MainIconBalance)
  - DockRepeaterMaxWidth=(DockContainerWidth==``?skip():max(DockContainerWidth-2*$DockEdgeGap-$DockLeftPad-$DockMiddleGap-$DockRightPad,200))
  - IconsShift=($DockSideMargin+$DockLeftPad+$MainIconBalance)
controlStyles:
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=$lumiBackground
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid > Border#BackgroundElement, Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement
    styles:
      - CornerRadius=$bcr
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Taskbar.ExperienceToggleButton#LaunchListButton > Taskbar.TaskListButtonPanel > Grid > Border, Taskbar.ExperienceToggleButton#LaunchListButton > Taskbar.TaskListButtonPanel > Border
    styles:
      - CornerRadius=$bcr
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: SearchUx.SearchUI.SearchButtonRootGrid > Grid > Border, SearchUx.SearchUI.SearchButtonRootGrid > Border
    styles:
      - CornerRadius=$bcr
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: SearchUx.SearchUI.SearchButtonRootGrid > Grid > Border#SearchPillBackgroundElement, SearchUx.SearchUI.SearchButtonRootGrid > Border#SearchPillBackgroundElement
    styles:
      - CornerRadius=$bcr
  - target: SearchUx.SearchUI.SearchPillButton > SearchUx.SearchUI.SearchButtonRootGrid > Grid > Grid > FontIcon > Grid > TextBlock, SearchUx.SearchUI.SearchPillButton > SearchUx.SearchUI.SearchButtonRootGrid > Grid > FontIcon > Grid > TextBlock
    styles:
      - Margin=-2,0,8,0
  - target: SearchUx.SearchUI.SearchButtonRootGrid[Width=220] > Grid > Border, SearchUx.SearchUI.SearchButtonRootGrid[Width=220] > Border
    styles:
      - CornerRadius=$bcr
  - target: SearchUx.SearchUI.SearchButtonRootGrid@ThemeColorStates > Grid > Border, SearchUx.SearchUI.SearchButtonRootGrid@ThemeColorStates > Border
    styles:
      - Background@Wave3_InactiveNormal:=$bso
      - Background@Wave3_InactivePointerOver:=$bh
      - Background@Wave3_Focused:=$bp
      - Background@CustomTheme_InactiveNormal:=$bso
      - Background@CustomTheme_InactivePointerOver:=$bh
      - Background@CustomTheme_InactivePointerOver_BrighterBackground:=$bh
      - Background@CustomTheme_Focused:=$bp
      - Background@SearchActive_Transparent:=$t
      - BorderThickness=$bbt
      - BorderBrush@Wave3_InactiveNormal:=$bbb
      - BorderBrush@Wave3_InactivePointerOver:=$bbb
      - BorderBrush@Wave3_Focused:=$bbb
      - BorderBrush@CustomTheme_InactiveNormal:=$bbb
      - BorderBrush@CustomTheme_InactivePointerOver:=$bbb
      - BorderBrush@CustomTheme_InactivePointerOver_BrighterBackground:=$bbb
      - BorderBrush@CustomTheme_Focused:=$bbb
      - BorderBrush@SearchActive_Transparent:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Taskbar.TaskListButton#TaskListButton > Grid#IconPanel > Border#BackgroundElement, Taskbar.TaskListButton#TaskListButton > Taskbar.TaskListLabeledButtonPanel#IconPanel > Border#BackgroundElement
    styles:
      - CornerRadius=$bcr
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Border#MultiWindowElement
    styles:
      - CornerRadius=$bcr
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Taskbar.TaskListButtonPanel#OverflowToggleButtonRootPanel > Grid > Border#BackgroundElement, Taskbar.TaskListButtonPanel#OverflowToggleButtonRootPanel > Border#BackgroundElement
    styles:
      - CornerRadius=$bcr
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill
    styles:
      - Fill:=$t
  - target: Grid#HoverFlyoutGrid > Border#HoverFlyoutBackground
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Taskbar.TaskItemThumbnailView > Grid@CommonStates > Border#BackgroundBorder
    styles:
      - Background=$t
      - CornerRadius=$mcr
      - BorderThickness@Normal=0
      - BorderThickness@PointerOver=0.05,0,0.05,1
      - BorderBrush@Normal=$t
      - BorderBrush@PointerOver:=$lumiAccentColor
  - target: Taskbar.TaskItemThumbnailView > Grid > Button#CloseButton
    styles:
      - CornerRadius=$mcr
      - Background:=#00000000
  - target: Taskbar.TaskItemThumbnailView > Grid > Button#CloseButton > ContentPresenter
    styles:
      - BorderBrush=$t
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Taskbar.ThumbBarButton#ThumbBarButton > ContentPresenter#BorderElement@CommonStates
    styles:
      - CornerRadius=16
      - Margin=-1.5
      - Background@Normal:=$bn
      - Background@PointerOver:=$bh
      - Background@Pressed:=$bp
      - Background@Disabled:=$bn
      - BorderThickness=$bbt
      - BorderBrush@Normal:=$bn
      - BorderBrush@PointerOver:=$bbb
      - BorderBrush@Pressed:=$bbb
      - BorderBrush@Disabled:=$bn
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: SystemTray.SystemTrayFrame
    styles:
      - Height={{taskbarDock==`vertical`?skip():`Auto`}}
      - VerticalAlignment={{taskbarDock==`vertical`?skip():`Stretch`}}
      - Transitions:=<TransitionCollection><RepositionThemeTransition /></TransitionCollection>
  - target: SystemTray.ChevronIconView > Grid#ContainerGrid
    styles:
      - Margin=0,0,0,0
  - target: SystemTray.ChevronIconView > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - CornerRadius=$bcr
      - Margin=0,4,0,4
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: SystemTray.NotifyIconView > Grid#ContainerGrid
    styles:
      - Margin=0,0,0,0
  - target: SystemTray.NotifyIconView > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - CornerRadius=$bcr
      - Margin=0,4,0,4
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid
    styles:
      - Margin=0,0,0,0
  - target: SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > Border#BackgroundBorder
    styles:
      - CornerRadius=$bcr
      - Margin=0,4,0,4
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: SystemTray.OmniButton#ControlCenterButton > Grid
    styles:
      - Margin=0,0,0,0
  - target: SystemTray.OmniButton#ControlCenterButton > Grid > Border#BackgroundBorder
    styles:
      - CornerRadius=$bcr
      - Margin=0,4,0,4
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid
    styles:
      - Margin=0,0,0,0
      - ActualWidth=>DockClockButtonWidth
  - target: SystemTray.OmniButton#NotificationCenterButton > Grid > Border#BackgroundBorder
    styles:
      - CornerRadius=$bcr
      - Margin=0,4,0,4
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Border#OverflowFlyoutBackgroundBorder
    styles:
      - Background:=$lumiBackground
      - CornerRadius:=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Grid#ConfirmatorMainGrid
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect
    styles:
      - Fill:=<SolidColorBrush Color="{ThemeResource TrackRect}" />
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid
    styles:
      - Background:=$t
      - BorderBrush=$t
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement > Grid > Border
    styles:
      - Background:=$lumiBackground
      - Shadow:=
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement > Grid#GridElement > Border#VirtualDesktopSwitcherBackground
    styles:
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Margin=-2,1,-1,1
  - target: Border#BackgroundDimmingLayer
    styles:
      - Background:=$t
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar > Grid > Border
    styles:
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Margin=-1,2,1,-2
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopBarElement#VirtualDesktopBar
    styles:
      - Width=Auto
      - HorizontalAlignment=1
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopListViewItem > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root
    styles:
      - CornerRadius=$mcr
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Grid#MainGrid > Border#MainBorder
    styles:
      - CornerRadius=$mcr
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopElementThemed > Grid#MainGrid > Border#BorderHighlight
    styles:
      - CornerRadius=$mcr
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed#NewVirtualDesktopButtonThemed > Grid#MainGrid > Border#MainBorder
    styles:
      - CornerRadius=$mcr
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.NewVirtualDesktopElementThemed#NewVirtualDesktopButtonThemed > Grid#MainGrid > Border#BorderHighlight
    styles:
      - CornerRadius=$mcr
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.VirtualDesktopThumbnailButton#ThumbnailButtonElement
    styles:
      - CornerRadius=$bcr
  - target: Button#VirtualDesktopElementCloseButton
    styles:
      - CornerRadius=$bcr
      - Background:=#00000000
  - target: Button#VirtualDesktopElementCloseButton > ContentPresenter
    styles:
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel#DFCPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root@CommonStates > Border#BackgroundBorder
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$mcr,$mcr,$bcr,$bcr
      - Margin:=-5,0,-5,-5
      - BorderThickness=$bt
      - BorderBrush@Normal:=$bb
      - BorderBrush@PointerOver:=$lumiAccentColor
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel#DFCPanel
    styles:
      - Transitions:=<TransitionCollection><AddDeleteThemeTransition /><EntranceThemeTransition FromHorizontalOffset="0" FromVerticalOffset="0" /></TransitionCollection>
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > Grid#TitleGrid > Image#IconImage
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="1" />
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > Grid#TitleGrid > TextBlock#DisplayName
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="1" />
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel#DFCPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root > ContentPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > Grid#TitleGrid > Button#SwitchItemElementCloseButton
    styles:
      - Background:=#00000000
      - RenderTransform:=<TranslateTransform X="5" Y="0" />
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel#DFCPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root > ContentPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > Grid#TitleGrid > Button#SwitchItemElementCloseButton > ContentPresenter#ContentPresenter
    styles:
      - CornerRadius=$mcr
      - Margin=5
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.200" />
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel#DFCPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root > ContentPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > Grid#TitleGrid > Button#SwitchItemElementCloseButton > ContentPresenter#ContentPresenter > TextBlock
    styles:
      - RenderTransform:=<TranslateTransform X="-0.8" Y="-0.6" />
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemElement > Grid#RootGrid > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemThumbnailButton#ThumbnailHost > Grid#RootGrid
    styles:
      - CornerRadius=$bcr
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Grid#ModalRootGrid > Border#BackgroundElement
    styles:
      - Background=$t
      - CornerRadius=$wcr
      - BorderThickness=0
      - Shadow:=
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Grid#ModalRootGrid > Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab
    styles:
      - Transitions:=<TransitionCollection><AddDeleteThemeTransition /><EntranceThemeTransition FromHorizontalOffset="0" FromVerticalOffset="0" /></TransitionCollection>
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Grid#ModalRootGrid > Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList > Border > ScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root@CommonStates > Border#BackgroundBorder
    styles:
      - Background:=<SolidColorBrush Color="{ThemeResource SolidBg}" />
      - CornerRadius=$mcr
      - BorderThickness@Normal=$bbt
      - BorderThickness@PointerOver=$bt
      - BorderBrush@Normal:=$bbb
      - BorderBrush@PointerOver:=$lumiAccentColor
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Grid#ModalRootGrid > Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList > Border > ScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root > ContentPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemControl > Grid#Root > Button#SwitchItemElementCloseButton
    styles:
      - Background:=#00000000
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Grid#ModalRootGrid > Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList > Border > ScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root > ContentPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemControl > Grid#Root > Button#SwitchItemElementCloseButton > ContentPresenter#ContentPresenter
    styles:
      - CornerRadius=$mcr
      - Margin=5
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.AltTab > Grid#ModalRootGrid > Border#BackgroundElement > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemList > Border > ScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.DynamicFlowPanel > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemListViewItem > Grid#Root > ContentPresenter > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemControl > Grid#Root > Button#SwitchItemElementCloseButton > ContentPresenter#ContentPresenter > TextBlock
    styles:
      - RenderTransform:=<TranslateTransform X="-0.8" Y="-0.6" />
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemControl > Grid#Root > WindowsInternal.ComposableShell.Experiences.Switcher.SwitchItemThumbnailButton#ThumbnailHost > Grid#RootGrid
    styles:
      - CornerRadius=$bcr
      - Margin=5
  - target: Border#SnapBarBorder
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
      - Transitions:=<TransitionCollection><AddDeleteThemeTransition /><EntranceThemeTransition FromHorizontalOffset="0" FromVerticalOffset="0" /></TransitionCollection>
  - target: FlyoutPresenter > Border
    styles:
      - Shadow:=
  - target: Border#SnapPickerBorder
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
      - Transitions:=<TransitionCollection><AddDeleteThemeTransition /><EntranceThemeTransition FromHorizontalOffset="0" FromVerticalOffset="0" /></TransitionCollection>
  - target: WindowsInternal.ComposableShell.Experiences.Switcher.SnapAssistList > Grid > Border
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Rectangle#VerticalTrackRect
    styles:
      - Fill:=$lumiBackground
  - target: MenuFlyoutPresenter
    styles:
      - CornerRadius:=$wcr
      - Shadow:=
  - target: MenuFlyoutPresenter > Border
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Transitions:=<TransitionCollection><EntranceThemeTransition FromHorizontalOffset="0" FromVerticalOffset="50" /></TransitionCollection>
  - target: MenuFlyoutItem > Grid@CommonStates
    styles:
      - CornerRadius=$bcr
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: MenuFlyoutSubItem > Grid@CommonStates
    styles:
      - CornerRadius=$bcr
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: ToolTip > ContentPresenter#LayoutRoot
    styles:
      - Background:=$lumiBackground
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel
    styles:
      - ChildrenTransitions:=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled="$MenuAnimation" FromHorizontalOffset="-50" FromVerticalOffset="50" /></TransitionCollection>
  - target: ToggleMenuFlyoutItem > Grid@CommonStates
    styles:
      - CornerRadius=$bcr
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarFrame > Grid#RootGrid@DockingStates
    styles:
      - Tag=horizontal
      - Tag@DockedLeft=vertical
      - Tag@DockedRight=vertical
      - Tag=>taskbarDock
  - target: Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskbarFrame
    styles:
      - Width={{taskbarDock==`vertical`?skip():`Auto`}}
      - HorizontalAlignment=Stretch
      - Margin={{$TrayInFrame?0:`$DockMargin,0,$DockMargin,0`}}
  - target: Taskbar.TaskbarFrame > Grid#RootGrid
    styles:
      - Margin=0,$DockTopGap,0,$DockBottomGap
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid
    styles:
      - Margin={{$TrayInFrame?$DockReady?$DockSideMargin:skip():skip()}},0,{{$TrayInFrame?$DockReady?$DockSideMargin:skip():skip()}},0
      - Background:=$lumiBackground
      - BorderThickness=$bt
      - BorderBrush={ThemeResource LumiDockBorderBrush}
      - CornerRadius=$mcr
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater
    styles:
      - Margin={{$TrayInFrame?0:skip()}},{{-($DockTopGap)}},0,{{-($DockBottomGap)}}
      - HorizontalAlignment={{$TrayInFrame?`Left`:skip()}}
      - MaxWidth={{$TrayInFrame?$DockRepeaterMaxWidth:skip()}}
      - ActualWidth=>DockRepeaterWidth
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.ExperienceToggleButton, Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.OverflowToggleButton
    styles:
      - Margin={{$TrayInFrame?$DockReady?$IconsShift:skip():skip()}},$DockTopGap,{{$TrayInFrame?$DockReady?-($IconsShift):skip():skip()}},$DockBottomGap
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.TaskListButton
    styles:
      - Margin={{$TrayInFrame?$DockReady?$IconsShift:skip():skip()}},0,{{$TrayInFrame?$DockReady?-($IconsShift):skip():skip()}},$DockBottomGap
  - target: Taskbar.TaskListButton > Grid#IconPanel, Taskbar.TaskListButton > Taskbar.TaskListLabeledButtonPanel#IconPanel
    styles:
      - Margin={{$TrayInFrame?0:skip()}},$DockTopGap,0,0
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton
    styles:
      - Margin={{$TrayInFrame?$DockReady?$IconsShift:skip():skip()}},{{$TrayInFrame?$DockTopGap:0}},{{$TrayInFrame?$DockReady?-($IconsShift):skip():skip()}},{{$TrayInFrame?$DockBottomGap:0}}
  - target: Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton]
    styles:
      - Margin={{$TrayInFrame?$DockReady?$IconsShift:skip():skip()}},0,{{$TrayInFrame?$DockReady?-($IconsShift):skip():skip()}},$DockBottomGap
  - target: Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Width=>LumiStartWidth
      - Margin={{$TrayInFrame?0:skip()}},$DockTopGap,0,0
  - target: Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid > Border#BackgroundElement, Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton] > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement
    styles:
      - ActualWidth=>LumiStartInnerWidth
  - target: SystemTray.SystemTrayFrame
    styles:
      - Margin=0,$DockTopGap,$DockMargin,$DockBottomGap
  - target: Taskbar.TaskbarExtensionElement > ContentPresenter > SystemTray.SystemTrayFrame
    styles:
      - ActualWidth=>TrayInFrameWidth
      - Margin={{$TrayInFrame?$DockReady?$TrayExtraShift:skip():skip()}},{{$TrayInFrame?$DockTopGap:0}},{{$TrayInFrame?$DockReady?-($TrayExtraShift):skip():skip()}},{{$TrayInFrame?$DockBottomGap:0}}
      - Transitions:=<TransitionCollection />
  - target: Grid#HoverFlyoutGrid
    styles:
      - Margin=0,0,0,0
  - target: Taskbar.TaskbarFrame
    styles:
      - Height={{taskbarDock==`vertical`?skip():$DockHeight}}
  - target: :root > ScrollViewer > ScrollContentPresenter > Border
    styles:
      - ActualWidth=>DockContainerWidth
  - target: Taskbar.TaskbarExtensionElement
    styles:
      - Margin={{$TrayInFrame?$DockReady?$IconsShift:skip():skip()}},0,{{$TrayInFrame?$DockReady?-($IconsShift):skip():skip()}},0
  - target: SystemTray.Stack#SecondaryClockStack
    styles:
      - ActualWidth=>DockSecondaryClockWidth
  - target: ComposerTaskbarUX.SystemComposerEntryButton
    styles:
      - Margin={{$TrayInFrame?0:skip()}},$DockTopGap,0,$DockBottomGap
      - CornerRadius=$bcr
  - target: ComposerTaskbarUX.SystemComposerTaskbarIconHost > Grid#RootPanel
    styles:
      - MinHeight=0
      - Padding=2,4,2,4
  - target: ComposerTaskbarUX.SystemComposerTaskbarIconHost > Grid#RootPanel > Border#BackgroundElement
    styles:
      - CornerRadius=$bcr
      - BorderThickness=$bbt
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="$FadeSpeed" />
themeResourceVariables:
  - LumiAccent@Dark={ThemeResource SystemAccentColorLight2}
  - LumiAccent@Light={ThemeResource SystemAccentColorDark1}
  - TrackRect@Dark=#10FFFFFF
  - TrackRect@Light=#30202020
  - SolidBg@Dark=#10FFFFFF
  - SolidBg@Light=#90FFFFFF
  - LumiBorderBrush@Light:=<SolidColorBrush Color="#24000000" />
  - LumiBorderBrush@Dark:=<SolidColorBrush Color="#24FFFFFF" />
  - LumiDockBorderBrush@Light:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#55FFFFFF" Offset="0.0" /><GradientStop Color="#14000000" Offset="0.45" /><GradientStop Color="#2B000000" Offset="1.0" /></LinearGradientBrush>
  - LumiDockBorderBrush@Dark:=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#38FFFFFF" Offset="0.0" /><GradientStop Color="#14FFFFFF" Offset="0.45" /><GradientStop Color="#22000000" Offset="1.0" /></LinearGradientBrush>
```
</details>
