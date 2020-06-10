<div align="center">
<h3>dmenu-bluetooth</h3>
<img src="https://github.com/ClydeDroid/rofi-bluetooth/raw/master/.meta/menu.gif">

`bluetoothctl` `rofi` `dmenu`

</div>

## Installation

<!--- Install from [AUR (rofi-bluetooth-git)](https://aur.archlinux.org/packages/rofi-bluetooth-git/), or: -->

1. Install dependencies: dmenu and bluetoothctl (provided by `bluez-utils` in Arch)
1. `wget "https://raw.githubusercontent.com/Layerex/dmenu-bluetooth/master/dmenu-bluetooth"`
1. `chmod +x dmenu-bluetooth`
1. `./dmenu-bluetooth`
1. (Optional) For easy access, add the script somewhere in your `$PATH`.

### Polybar configuration

`NOTE:` In order to properly display the bluetooth icon, you will need to use an iconic font in your bar, e.g. [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts)

```
[module/bluetooth]
type = custom/script
exec = dmenu-bluetooth --status
interval = 1
click-left = dmenu-bluetooth &
```

### i3 keybinding

```
bindsym $mod+b exec --no-startup-id dmenu-bluetooth
```

### Thanks for the inspiration!

- [firecat53/networkmanager-dmenu](https://github.com/firecat53/networkmanager-dmenu)
- [x70b1's bluetoothctl polybar script](https://github.com/polybar/polybar-scripts/tree/master/polybar-scripts/system-bluetooth-bluetoothctl)
