![Preview](screenshot.png)
# Glass DockLike

A glass-effect dock theme with custom blur and centering.

## Style

```xml
<Style Target="Taskbar.TaskbarFrame">
  <Setter Property="Width" Value="Auto" />
  <Setter Property="HorizontalAlignment" Value="Center" />
  <Setter Property="Margin" Value="250,0,250,0" /> <!-- that works for my screen so i didnt touch it -->
</Style>

<Style Target="Taskbar.TaskbarFrame > Grid#RootGrid">
  <Setter Property="Background">
    <Setter.Value>
      <WindhawkBlur BlurAmount="5" TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.05" />
    </Setter.Value>
  </Setter>
  <Setter Property="Padding" Value="6,0,6,0" />
  <Setter Property="CornerRadius" Value="12" />
  <Setter Property="BorderThickness" Value="1.5" />
  <Setter Property="BorderBrush">
    <Setter.Value>
      <SolidColorBrush Color="#88FFFFFF" />
    </Setter.Value>
  </Setter>
</Style>

<Style Target="Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill">
  <Setter Property="Visibility" Value="Collapsed" />
</Style>

<Style Target="Rectangle#BackgroundStroke">
  <Setter Property="Visibility" Value="Collapsed" />
</Style>

<Style Target="Grid#SystemTrayFrameGrid">
  <Setter Property="Background">
    <Setter.Value>
      <WindhawkBlur BlurAmount="5" TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.05" />
    </Setter.Value>
  </Setter>
  <Setter Property="Margin" Value="0" />
  <Setter Property="CornerRadius" Value="12" />
  <Setter Property="BorderThickness" Value="1.5" />
  <Setter Property="BorderBrush">
    <Setter.Value>
      <SolidColorBrush Color="#88FFFFFF" />
    </Setter.Value>
  </Setter>
  <Setter Property="BackgroundSizing" Value="InnerBorderEdge" />
</Style>

<Style Target="SystemTray.ChevronIconView"><Setter Property="Padding" Value="0" /></Style>
<Style Target="SystemTray.NotifyIconView#NotifyItemIcon"><Setter Property="Padding" Value="0" /></Style>
<Style Target="SystemTray.OmniButton"><Setter Property="Padding" Value="0" /></Style>
<Style Target="SystemTray.CopilotIcon"><Setter Property="Padding" Value="0" /></Style>

<Style Target="Taskbar.Gripper#GripperControl">
  <Setter Property="Width" Value="Auto" />
  <Setter Property="MinWidth" Value="24" />
</Style>
