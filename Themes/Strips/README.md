theme: ''
styleConstants:
  - mainRadius = 6
  - transparent = <SolidColorBrush Color="Transparent"/>
  - base = <WindhawkBlur BlurAmount="2" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.3" TintLuminosityOpacity="0.3" NoiseOpacity="0.1" NoiseDensity="0.5" />
  - active = <WindhawkBlur BlurAmount="2" TintColor="{ThemeResource SystemChromeLowColor}" TintOpacity="0.55" TintLuminosityOpacity="0.3" NoiseOpacity="0.1" NoiseDensity="0.5" />
  - overlay = <WindhawkBlur BlurAmount="2" TintColor="{ThemeResource SystemChromeMediumLowColor}" TintOpacity="0.35" TintLuminosityOpacity="0.3" NoiseOpacity="0.1" NoiseDensity="0.5" />
  - MultiWindowIndicatorAccent = <AcrylicBrush TintColor="{ThemeResource SystemAccentColor}"/>
  - BorderThicknessBase=1
  - BorderThicknessActive=2,2,2,1
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,2"><GradientStop Color="{ThemeResource AdaptiveLight}" Offset="0.0" /><GradientStop Color="{ThemeResource AdaptiveFade}" Offset="1" /></LinearGradientBrush>
controlStyles:
  - target: Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill
    styles:
      - Fill := $transparent
  - target: Rectangle#BackgroundStroke
    styles:
      - Fill := $transparent
  - target: Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl
    styles:
      - Fill:=$base
      - CornerRadius = $mainRadius
  - target: Taskbar.TaskListButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - CornerRadius = $mainRadius
      - Background :=$base
      - Background@InactivePointerOver :=$overlay
      - Background@ActivePointerOver:=$overlay
      - Background@ActiveNormal :=$active
      - Margin = 0,7,0,6
  - target: Taskbar.TaskListButton#TaskListButton[AutomationProperties.Name=Copilot] > Taskbar.TaskListLabeledButtonPanel#IconPanel > Border#BackgroundElement
    styles:
      - Visibility = 1
  - target: Taskbar.SearchBoxButton
    styles:
      - Visibility = Collapsed
  - target: Taskbar.TaskListButton#TaskListButton
    styles:
      - Margin = 0,0,10,0
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Border#BackgroundElement
    styles:
      - CornerRadius = $mainRadius
      - Margin = 0,7,0,6
      - Background@InactiveNormal :=$base
      - Background@ActiveNormal :=$active
      - Background@InactivePointerOver :=$overlay
      - Background@ActivePointerOver:=$overlay
      - Background@ActivePressed:=$overlay
      - Background@InactivePressed:=$base
      - Background@MultiWindowNormal:=$base
      - Background@MultiWindowActive:=$active
      - Background@MultiWindowPointerOver:=$overlay
      - Background@MultiWindowPressed:=$overlay
      - BorderBrush:=$BorderBrush
      - BorderBrush@ActiveNormal :=$BorderBrush
      - BorderBrush@ActivePointerOver :=$BorderBrush
      - BorderBrush@InactivePointerOver :=$BorderBrush
      - BorderBrush@MultiWindowActive :=$BorderBrush
      - BorderBrush@MultiWindowPointerOver :=$BorderBrush
      - BorderThickness:=$BorderThicknessBase
      - BorderThickness@ActiveNormal :=$BorderThicknessActive
      - BorderThickness@ActivePointerOver :=$BorderThicknessActive
      - BorderThickness@InactivePointerOver :=$BorderThicknessBase
      - BorderThickness@MultiWindowActive :=$BorderThicknessActive
  - target: Border#MultiWindowElement
    styles:
      - Visibility=Collapsed
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > TextBlock#LabelControl
    styles:
      - Margin=0,0,5,2
      - HorizontalAlignment = 1
      - FontWeight = Normal
      - FontWeight@InactiveNormal = Normal
      - FontWeight@InactivePointerOver = Bold
      - FontWeight@InactivePressed = Normal
      - FontWeight@ActiveNormal = Bold
      - FontWeight@ActivePointerOver = Bold
      - FontWeight@ActivePressed = Bold
      - FontWeight@MultiWindowNormal = Normal
      - FontWeight@MultiWindowPointerOver = Bold
      - FontWeight@MultiWindowActive = Bold
  - target: Grid#SystemTrayFrameGrid
    styles:
      - CornerRadius = $mainRadius
      - Margin=-55,11,10,10
      - Padding=5,0,-5,0
      - BorderThickness:=$BorderThicknessBase
      - Background:=$base
      - BorderBrush:=$BorderBrush
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton
    styles:
      - Margin=0,0,2,0
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid[2] > Grid > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Border > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Grid > Border#LargeTicker2 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > TextBlock[1]
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="8" />
      - ActualWidth=>WeatherCondWidth
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid > Grid[2] > Grid > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Border > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > Grid > Border#LargeTicker2 > AdaptiveCards.Rendering.Uwp.WholeItemsPanel > TextBlock[2]
    styles:
      - RenderTransform:=<TranslateTransform X="{{WeatherCondWidth+7}}" Y="-8" />
      - ActualWidth=>WeatherTempWidth
  - target: Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Grid#AugmentedEntryPointContentGrid
    styles:
      - HorizontalAlignment=0
      - TextAlignment=0
      - Width = {{WeatherTempWidth+WeatherCondWidth+50}}
  - target: Grid#AugmentedEntryPointContentGrid > Grid > Grid
    styles:
      - Width = 300
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Width = {{WeatherTempWidth+WeatherCondWidth+50}}
      - Margin = 10,4,0,4
      - Padding = 0,0,0,0
  - target: Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement
    styles:
      - BorderThickness:=$BorderThicknessBase
      - BorderBrush:=$BorderBrush
  - target: Grid#AugmentedEntryPointContentGrid
    styles:
      - Margin = 5,0,0,0
  - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Image#OverlayIcon
    styles:
      - Width=15
      - Height=15
      - Margin=10,4,0,0
  - target: Taskbar.TaskListLabeledButtonPanel#IconPanel > Taskbar.Badge#BadgeControl
    styles:
      - Width=15
      - Height=15
      - Margin=0,2,0,0
      - HorizontalAlignment= 1
      - VerticalAlignment= 1
      - RenderTransform := <TranslateTransform X="4" Y="2" />
  - target: Grid#OverflowRootGrid > Border
    styles:
      - Shadow :=
  - target: Taskbar.TaskListLabeledButtonPanel@CommonStates > Rectangle#RunningIndicator
    styles:
      - Width=4
      - Height=4
      - Margin=13,33,0,0
      - StrokeThickness=1
      - VerticalAlignment=0
      - HorizontalAlignment=0
      - Fill@MultiWindowNormal:=$MultiWindowIndicatorAccent
      - Fill@MultiWindowActive:=$MultiWindowIndicatorAccent
      - Fill@MultiWindowPointerOver:=$MultiWindowIndicatorAccent
      - Fill@MultiWindowPressed=Transparent
      - Fill=transparent
      - Canvas.ZIndex=1
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid > Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.ExperienceToggleButton#LaunchListButton
    styles:
      - Margin=0,0,10,0
  - target: ScrollViewer > ScrollContentPresenter > Border > Grid > Taskbar.TaskbarFrame#TaskbarFrame > Grid#RootGrid > Microsoft.UI.Xaml.Controls.ItemsRepeater#TaskbarFrameRepeater > Taskbar.ExperienceToggleButton#LaunchListButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel
    styles:
      - Visibility=Collapsed
themeResourceVariables:
  - AdaptiveLight@Light=#DCDCDC
  - AdaptiveLight@Dark=#CC646464
  - AdaptiveFade@Light=#00ffffff
  - AdaptiveFade@Dark=#00000000
xamlDiagnosticsHandling: ''
