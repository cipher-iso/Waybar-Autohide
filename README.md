# **How to Install:<br/>**

**STEP 1: git clone https://github.com/cipher-xui/Waybar-Autohide.git<br/>**
**STEP 2: drag 'Scripts' into $HOME directory<br/>**
**STEP 3 [OPT]: drag all other contents into '$HOME/.config/' directory<br/>**
**STEP 4: add this to your Waybar config<br/>**

	"on-sigusr1": "hide",<br/>
	"on-sigusr2": "show",<br/>
	"start_hidden": true,<br/>
	"reload_style_on_change": true,<br/>
	"layer": "top",<br/>
	"position": "top",<br/>
	"gtk-layer-shell": true,<br/>
	"exclusive": true,<br/>
	
**STEP 5 [OPT]: add custom module to toggle with mouse<br/>**

	"custom/barlock": {<br/>
		"exec": "~/.config/waybar/WaybarLockModule",<br/>
   		"interval": 1,<br/>
   		"format": "{}",<br/>
   		"return-type": "json",<br/>
   		"on-click": "~/Scripts/ToggleWaybar"<br/>
   	}

**STEP 6: Run the script via hyprctl or exec-once<br/>**
- `hyprctl dispatch exec ~/Scripts/WaybarAutohide &`<br/>
  OR [In your Hyprland.conf]<br/>
- `exec-once = ~/Scripts/WaybarAutohide`<br/>
 <br/>
 <br/>

# FULL INSTALL:
**Packages needed:**<br/>
*[Only if you are installing the entire bar - via 'Step 3']*<br/>

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

**Quick Package Install:**<br/>
*[Only if you are installing the entire bar - via 'Step 3']*<br/>
`sudo pacman -S --needed waybar kitty swayosd swaync hyprlock hyprsunset pavucontrol-qt blueman`<br/>
`yay -S --needed nmgui-bin`

**Custom .bashrc Path':**<br/>
*[This is necessary to have Waybar work OOB - all Waybar functions are defined via Path to ~/Scripts]*<br/>

	export PATH="$HOME/Scripts:$PATH"
