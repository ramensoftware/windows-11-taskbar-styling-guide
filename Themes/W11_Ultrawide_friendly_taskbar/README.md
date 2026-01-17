# W11-CenteredTaskBar theme for Windows 11 Taskbar Styler

A minimal, floating dual-island taskbar inspired by macOS dock aesthetics. Separates the app icons and system tray into two distinct rounded islands with a semi-transparent ghost bar behind them.

![Screenshot](<img width="2467" height="482" alt="image" src="https://github.com/user-attachments/assets/46129402-fb97-4d20-85ba-194ccb331ddd" />)

## Features

- **Dual Islands**: App icons and system tray float as separate rounded containers
- **Ghost Bar**: Semi-transparent backdrop ties the composition together
- **Centered Layout**: Both islands center automatically using flexible grid columns
- **Floating Effect**: Small vertical margin creates a subtle lift from screen edge
- **Clean Aesthetic**: Dark backgrounds (#202020) with rounded corners (10px radius)

## Installation

The theme is integrated into the mod and can simply be selected from the mod's settings:

1. Open the **Windows 11 Taskbar Styler** mod in Windhawk.
2. Go to the "Settings" tab.
3. Select the theme and save the settings.

The theme styles can also be imported manually. To do that, follow these steps:

1. Open the **Windows 11 Taskbar Styler** mod in Windhawk.
2. Go to the "Advanced" tab.
3. Copy the content below to the text box under "Mod settings" and click "Save".
```json
{
  "controlStyles[0].target": "ScrollViewer > ScrollContentPresenter > Border > Grid",
  "controlStyles[0].styles[0]": "ColumnDefinitions:=<ColumnDefinitionCollection><ColumnDefinition Width=\"*\"/><ColumnDefinition Width=\"Auto\"/><ColumnDefinition Width=\"Auto\"/><ColumnDefinition Width=\"*\"/></ColumnDefinitionCollection>",
  "controlStyles[0].styles[1]": "HorizontalAlignment=Stretch",
  "controlStyles[0].styles[2]": "Background:=<SolidColorBrush Color=\"#66000000\"/>",
  "controlStyles[1].target": "Taskbar.TaskbarFrame#TaskbarFrame",
  "controlStyles[1].styles[0]": "Grid.Column=1",
  "controlStyles[1].styles[1]": "Width=Auto",
  "controlStyles[1].styles[2]": "HorizontalAlignment=Right",
  "controlStyles[1].styles[3]": "Margin=0,0,5,0",
  "controlStyles[2].target": "Taskbar.TaskbarFrame#TaskbarFrame > Grid",
  "controlStyles[2].styles[0]": "Background:=<SolidColorBrush Color=\"#FF202020\"/>",
  "controlStyles[2].styles[1]": "CornerRadius=10",
  "controlStyles[2].styles[2]": "Padding=25,0,25,0",
  "controlStyles[2].styles[3]": "Margin=0,3,0,3",
  "controlStyles[3].target": "SystemTray.SystemTrayFrame",
  "controlStyles[3].styles[0]": "Grid.Column=2",
  "controlStyles[3].styles[1]": "Width=Auto",
  "controlStyles[3].styles[2]": "HorizontalAlignment=Left",
  "controlStyles[3].styles[3]": "Margin=5,0,0,0",
  "controlStyles[4].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[4].styles[0]": "Background:=<SolidColorBrush Color=\"#FF202020\"/>",
  "controlStyles[4].styles[1]": "CornerRadius=10",
  "controlStyles[4].styles[2]": "Padding=5,0,5,0",
  "controlStyles[4].styles[3]": "Margin=0,3,0,3",
  "controlStyles[5].target": "Taskbar.TaskbarBackground#BackgroundControl",
  "controlStyles[5].styles[0]": "Visibility=Collapsed",
  "controlStyles[6].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[6].styles[0]": "Fill=Transparent"
}
```

## Customization

### Adjust Island Float (Vertical Gap)

Change the `Margin` values on the island Grid targets. The format is `left,top,right,bottom`:
"Margin=0,3,0,3"  → 3px float (default)
"Margin=0,6,0,6"  → 6px float (more dramatic)
"Margin=0,0,0,0"  → No float

### Change Ghost Bar Opacity

Modify the background color's alpha channel:
#66000000  → 40% opacity (default)
#99000000  → 60% opacity
#33000000  → 20% opacity
Transparent → No ghost bar

### Adjust Island Gap

Change the horizontal margins between islands:
"Margin=0,0,5,0" (app) + "Margin=5,0,0,0" (tray) → 10px gap (default)
"Margin=0,0,10,0" + "Margin=10,0,0,0" → 20px gap

### Island Background Color

Replace `#FF202020` with your preferred color:
#FF202020  → Dark gray (default)
#FF000000  → Pure black
#FF1a1a2e  → Dark navy

## Notes

- Designed for Windows 11 with taskbar icons centered
- Works with both light and dark system themes
- The app island has wider padding (25px) for more clickable area; tray has tighter padding (5px)

## Credits

Created by [CryptoProgenitor](https://github.com/CryptoProgenitor)
