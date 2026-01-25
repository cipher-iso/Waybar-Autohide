How to Install:
1. git clone https://github.com/cipher-xui/Waybar-Autohide.git
2. drag 'Scripts' into $HOME directory
3 (optional). drag all other contents into '$HOME/.config/' directory
4. add this to your Waybar config
  `"on-sigusr1": "hide",
	"on-sigusr2": "show",
	"start_hidden": true,
	"reload_style_on_change": true,
	"layer": "top",
	"position": "top",
	"gtk-layer-shell": true,
	"exclusive": true,`
5. (optional). add custom module to toggle with mouse
   `"custom/barlock": {
   "exec": "~/.config/waybar/WaybarLockModule",
   "interval": 1,
   "format": "{}",
   "return-type": "json",
   "on-click": "ToggleWaybar"
   }`


Packages needed:

- Hyprland [duh]
- Waybar [duh]
- Kitty Terminal
- SwayOSD
- SwayNC
- Hyprlock
- Hyprsunset
- Pavucontrol-QT
- nmgui-bin
- blueman

[ These are only necessary if you intend to copy the entire Waybar config ]

OOB Install:
`sudo pacman -S --needed waybar kitty swayosd swaync hyprlock hyprsunset pavucontrol-qt blueman`
`yay -S --needed nmgui-bin`
