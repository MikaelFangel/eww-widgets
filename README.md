# EWW Widgets
A collection of my EWW widgets all written to work on Wayland with a focus of integration with Hyprland.

## Pop-up/Dialogs
### Brightness Indicator

A Hyprland themed brightness indicator 

![20231105_20h41m40s_grim](https://github.com/MikaelFangel/eww-widgets/assets/34864484/9468db79-70a9-41c0-8e1f-b0565fdb1268)

#### Dependencies
* brightnessctl

### How To

Add the following window to you main `eww.yuck` file and map shortcuts that updates the variable whether it is shown or not

```
(include "./modules/eww-settings/metric-indicator/eww.yuck")

(defvar show_curbright false)

(defwindow brightness-indicator
  :monitor 0
    :geometry (
      geometry
      :anchor "center"
      :x "0"
      :y "0"
      :width "0%"
      :height "0%"
    )

  :stacking "fg"
  :exclusive "false"
  :focusable "false"

  (_metric :value curbright :icon "   " :show_indicator show_curbright)
)
```
AND! Don't forget to import the eww.scss in you main eww.scss file.

### Volume Indicator

A Hyprland themed volume indicator

![20231110_11h26m03s_grim](https://github.com/MikaelFangel/eww-widgets/assets/34864484/dc8512f0-41c0-48ba-a21b-b946350dfccc)


#### Dependencies
* wpctl

## Tray icons
