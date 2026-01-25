# **How to Install:<br/>**
**[PREVIEW]:<br/>**
![Preview](https://raw.githubusercontent.com/cipher-xui/Waybar-Autohide/main/Preview.gif)

**STEP 1:</br>** git clone https://github.com/cipher-xui/Waybar-Autohide.git<br/></br>
**STEP 2:</br>** drag '`Scripts`' into your `$HOME` directory<br/></br>
**STEP 3:</br>** add this to your Waybar config<br/>

	"on-sigusr1": "hide",
	"on-sigusr2": "show",
	"start_hidden": true,
	"reload_style_on_change": true,
	"layer": "top",
	"position": "top",
	"gtk-layer-shell": true,
	"exclusive": true,
	
**STEP 4: [OPTIONAL]<br/>** Add custom module to toggle with mouse<br/>

	"custom/barlock": {
		"exec": "~/.config/waybar/WaybarLockModule",
   		"interval": 1,
   		"format": "{}",
   		"return-type": "json",
   		"on-click": "~/Scripts/ToggleWaybar"
   	}

**STEP 5: Run the script via hyprctl or exec-once<br/>**
- `hyprctl dispatch exec ~/Scripts/WaybarAutohide &`<br/>
  OR [In your Hyprland.conf]<br/>
- `exec-once = ~/Scripts/WaybarAutohide`<br/>

**[Note: Remember to restart Waybar after all these steps, otherwise it will not work]**

 <br/>
 <br/>

# FULL INSTALL:
**If you want to install my entire Waybar config, then follow the steps below.**<br/>

**STEP 6:**<br/>
Drag all other contents into your '`$HOME/.config/`' directory<br/>
  
**STEP 7:**<br/>
Install necessary packages<br/>
`sudo pacman -S --needed waybar kitty swayosd swaync hyprlock hyprsunset pavucontrol-qt blueman`<br/>
`yay -S --needed nmgui-bin`

**STEP 8:**<br/>
Create a custom `$PATH` in your `.bashrc`<br/>
	`export PATH="$HOME/Scripts:$PATH"`
