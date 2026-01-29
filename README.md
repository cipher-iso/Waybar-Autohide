# **💫 PARTIAL INSTALL: [AUTO-HIDE ONLY]<br/>**
> [!NOTE]
**[AUTO-HIDE PREVIEW]:<br/>**
![Preview](https://raw.githubusercontent.com/cipher-xui/Waybar-Autohide/main/Preview.gif)

**STEP 1:</br>** git clone https://github.com/cipher-iso/Waybar-Autohide.git<br/></br>
**STEP 2:</br>** Drag '`Scripts`' into your `$HOME` Directory<br/>*`You will not need the other contents, unless you are doing the FULL INSTALL below.`*</br></br>
**STEP 3:</br>** Create These Lines in your Waybar's 'config.jsonc'<br/>

	"on-sigusr1": "hide",
	"on-sigusr2": "show",
	"start_hidden": false,
	"reload_style_on_change": true,
	"layer": "top",
	"position": "top",
	"gtk-layer-shell": true,
	"exclusive": true,

**STEP 4: Run the Script in Background<br/>**
- `hyprctl dispatch exec ~/Scripts/WaybarAutohide &`<br/>
  OR [In your Hyprland.conf]<br/>
- `exec-once = ~/Scripts/WaybarAutohide`<br/><br/>
	
**STEP 5: [OPTIONAL]** Add Toggle-Module<br/>
Export 'waybar/WaybarLockModule' from the repo into your Waybar's<br/>
config directory, then create the module within your 'config.jsonc'.

	"custom/barlock": {
		"exec": "~/.config/waybar/WaybarLockModule",
   		"interval": 1,
   		"format": "{}",
   		"return-type": "json",
   		"on-click": "~/Scripts/ToggleWaybar"
   	}

> [!WARNING]  
> RESTART WAYBAR AFTER RUNNING THIS SCRIPT,<br/>
> OTHERWISE IT WILL NOT WORK!

 <br/>

# **🌟 FULL INSTALL: [ENTIRE WAYBAR CONFIG]**
> [!IMPORTANT]  
> **If you want to install my entire Waybar config, then follow the steps below.**

**STEP 6:**<br/>
Drag all other contents into your '`$HOME/.config/`' directory<br/>
  
**STEP 7:**<br/>
Install necessary packages<br/>
`sudo pacman -S --needed waybar kitty swayosd swaync hyprlock hyprsunset pavucontrol-qt blueman`<br/>
`yay -S --needed nmgui-bin`

**STEP 8:**<br/>
Create a custom `$PATH` in your `.bashrc`<br/>
	`export PATH="$HOME/Scripts:$PATH"`

## ✨ STAR HISTORY

<a href="https://www.star-history.com/#cipher-iso/Waybar-Autohide&cipher-iso/dotfiles&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=cipher-iso/Waybar-Autohide,cipher-iso/dotfiles&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=cipher-iso/Waybar-Autohide,cipher-iso/dotfiles&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=cipher-iso/Waybar-Autohide,cipher-iso/dotfiles&type=date&legend=top-left" />
 </picture>
</a>
