# Borderless theme for Windows 11 Taskbar Styler

Taskbar dock-like theme with removal of shadows from hover flyouts, tray flyout, volume/brightness flyouts, and taskbar overflow.

**Author**: [Ali Cool](https://github.com/AliCool412)

![Screenshot](screenshot.png)

## Important note
The theme might look different with the default taskbar height. To solve this, install the "Taskbar height and icon size" mod and set the taskbar height to a minimum of 56 (as opposed to the default height being 48).

![Screenshot with default height](screenshot-default-height.png)

## Customization

To apply the customizations below, set the corresponding style constants in the mod settings under "Style constants".

### Taskbar frame width

By default, the taskbar frame is set to 800px. Set `TaskbarFrameWidth` to adjust the width. For example, use `TaskbarFrameWidth=1000` for a wider 1000px taskbar.

## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
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
"controlStyles[0].target":"ScrollViewer > ScrollContentPresenter > Border > Grid",
  "controlStyles[0].styles[0]":"ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width=\"*\"/><ColumnDefinition Width=\"Auto\"/><ColumnDefinition Width=\"Auto\"/><ColumnDefinition Width=\"*\"/></ColumnDefinitionCollection>",
  "controlStyles[0].styles[1]":"HorizontalAlignment=Stretch",
"controlStyles[1].target":"Taskbar.TaskbarFrame#TaskbarFrame",
  "controlStyles[1].styles[0]":"Grid.Column=1",
  "controlStyles[1].styles[1]":"Width=$TaskbarFrameWidth",
  "controlStyles[1].styles[2]":"Margin=0",
  "controlStyles[1].styles[3]":"MaxWidth=$TaskbarFrameWidth",
"controlStyles[2].target":"SystemTray.SystemTrayFrame",
  "controlStyles[2].styles[0]":"Grid.Column=1",
  "controlStyles[2].styles[1]":"Width=Auto",
  "controlStyles[2].styles[2]":"HorizontalAlignment=Right",
  "controlStyles[2].styles[3]":"Height=42",
  "controlStyles[2].styles[4]":"VerticalAlignment=Center",
"controlStyles[3].target":"Taskbar.TaskbarFrame#TaskbarFrame > Windows.UI.Xaml.Controls.Grid#RootGrid > Taskbar.TaskbarBackground#BackgroundControl",
  "controlStyles[3].styles[0]":"CornerRadius=8",
  "controlStyles[3].styles[1]":"Margin=0,2,0,2",
"controlStyles[4].target":"Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke",
  "controlStyles[4].styles[0]":"Visibility=Collapsed",
"controlStyles[5].target":"Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater",
  "controlStyles[5].styles[0]":"Margin=0,4,0,4",
"controlStyles[6].target":"Windows.UI.Xaml.Controls.Border#OverflowFlyoutBackgroundBorder",
  "controlStyles[6].styles[0]":"Shadow:=",
  "controlStyles[6].styles[1]":"BorderThickness:=",
"controlStyles[7].target":"Windows.UI.Xaml.Controls.Grid#ConfirmatorMainGrid",
  "controlStyles[7].styles[0]":"Shadow:=",
  "controlStyles[7].styles[1]":"BorderThickness:=",
"controlStyles[8].target":"Taskbar.OverflowToggleButton#OverflowButton > Taskbar.TaskListButtonPanel#OverflowToggleButtonRootPanel > Windows.UI.Xaml.Controls.FontIcon#FontIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock",
  "controlStyles[8].styles[0]":"Text=",
"controlStyles[9].target":"Windows.UI.Xaml.Shapes.Rectangle#MostRecentlyUsedDivider",
  "controlStyles[9].styles[0]":"Height=32",
  "controlStyles[9].styles[1]":"Width=2",
"controlStyles[10].target":"Windows.UI.Xaml.Shapes.Rectangle#LeftOverflowButtonDivider",
  "controlStyles[10].styles[0]":"Visibility=Collapsed",
"controlStyles[11].target":"Windows.UI.Xaml.Shapes.Rectangle#RightOverflowButtonDivider",
  "controlStyles[11].styles[0]":"Visibility=Collapsed",
"controlStyles[12].target":"Microsoft.UI.Xaml.Controls.ItemsRepeater#OverflowFlyoutListRepeater",
  "controlStyles[12].styles[0]":"Height=48",
"controlStyles[13].target":"WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid > Grid",
  "controlStyles[13].styles[0]":"Background:=",
"controlStyles[14].target":"WindowsInternal.ComposableShell.Experiences.TextInput.Common.InputSwitcher > ContentControl > ContentPresenter > Grid",
  "controlStyles[14].styles[0]":"Margin=380,0,572,12",
  "controlStyles[14].styles[1]":"Shadow:=",
  "controlStyles[14].styles[2]":"BorderThickness:=",
"controlStyles[15].target":"Windows.UI.Xaml.Controls.Border#HoverFlyoutBackground",
  "controlStyles[15].styles[0]":"Shadow:=",
"styleConstants[0]":"TaskbarFrameWidth=800"
}
```
</details>
