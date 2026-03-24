# Borderless Dock/Taskbar for Windhawk
Taskbar Dock-Like Theme with removal of shadows from Hover Flyouts, Tray Flyout, Volume/Brightness Flyouts and Taskbar Overflow.

<img width="1919" height="93" alt="image" src="https://github.com/user-attachments/assets/aeb65e4d-66a5-465f-b063-97218e86d86e" />

## Important Note :
The Theme Might Look Weird on Default Taskbar Height, to Solve this, install the "Taskbar Height and Icon Size" Mod and Set The Taskbar Height to a Minimum of 60.

<img width="1919" height="80" alt="image" src="https://github.com/user-attachments/assets/3c5448f0-00ea-4a53-828c-b1d7a11a14ec" />

# Manual Installation :
The theme styles can be imported manually. To do that, follow these steps:
- Open the Windows 11 Taskbar Styler mod in Windhawk.
- Go to the "Advanced" tab.
- Copy the content below to the text box under "Mod settings" and click "Save".

<details>
<summary>Content to import (click to expand)</summary>
  
```json
{
"controlStyles[0].target":"ScrollViewer > ScrollContentPresenter > Border > Grid",
  "controlStyles[0].styles[0]":"ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width=\"*\"/><ColumnDefinition Width=\"Auto\"/><ColumnDefinition Width=\"Auto\"/><ColumnDefinition Width=\"*\"/></ColumnDefinitionCollection>",
  "controlStyles[0].styles[1]":"HorizontalAlignment=Stretch",
"controlStyles[1].target":"Taskbar.TaskbarFrame#TaskbarFrame",
  "controlStyles[1].styles[0]":"Grid.Column=1",
  "controlStyles[1].styles[1]":"Width=800",
  "controlStyles[1].styles[2]":"Margin=0,0,$IslandHorizontalMargin,0",
  "controlStyles[1].styles[3]":"MaxWidth=800",
"controlStyles[2].target":"SystemTray.SystemTrayFrame",
  "controlStyles[2].styles[0]":"Grid.Column=1",
  "controlStyles[2].styles[1]":"Width=Auto",
  "controlStyles[2].styles[2]":"HorizontalAlignment=Right",
  "controlStyles[2].styles[3]":"Margin=8",
"controlStyles[3].target":"Taskbar.TaskbarFrame#TaskbarFrame > Windows.UI.Xaml.Controls.Grid#RootGrid > Taskbar.TaskbarBackground#BackgroundControl",
  "controlStyles[3].styles[0]":"CornerRadius=8",
  "controlStyles[3].styles[1]":"Margin=0,2,0,2",
"controlStyles[4].target":"Windows.UI.Xaml.Shapes.Rectangle#BackgroundStroke",
  "controlStyles[4].styles[0]":"Visibility=Collapsed",
"controlStyles[5].target":"Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater",
  "controlStyles[5].styles[0]":"Margin=0,6,0,6",
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
  "controlStyles[14].styles[0]":"Margin=400,0,570,0",
  "controlStyles[14].styles[1]":"Shadow:=",
  "controlStyles[14].styles[2]":"BorderThickness:="
}
```
  </details>
