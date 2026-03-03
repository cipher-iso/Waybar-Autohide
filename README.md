# <p align="center">⚡️ WAYBAR AUTO-HIDE ⚡️</p>
<p align="center"><br>
  <img src="https://github.com/cipher-iso/Waybar-Autohide/blob/main/Waybar%20Demonstration.gif" width="700" alt="WAYBAR AUTO-HIDE PREVIEW"/>
</p>

<p align="center">
  <a href="https://github.com/cipher-iso/Waybar-Autohide?tab=readme-ov-file#-partial-install--auto-hide-only-">PARTIAL-INSTALL</a> •
  <a href="https://github.com/cipher-iso/Waybar-Autohide?tab=readme-ov-file#-full-install--entire-waybar-config-">FULL-INSTALL</a> •
  <a href="https://github.com/cipher-iso/Cipher-OS">DOTFILES</a>
</p>

---

## <p align="center">✨ PARTIAL INSTALL ✨<br>[ AUTO-HIDE ONLY ]</p>

### **👥 | STEP 1: [ CLONE REPO ]**
In Your Terminal:<br>
`git clone https://github.com/cipher-iso/Waybar-Autohide.git`

<br>

### **🧩 | STEP 2: [ COPY MODULES ]**
Copy the [WaybarAutoHide Module](https://github.com/cipher-iso/Waybar-Autohide/blob/main/waybar/Modules/WaybarAutoHide) into your `~/.config/waybar/Modules`<br>

<br>

### **📑 | STEP 3: [ WAYBAR CONFIG ]**
Add the following lines to your Waybar `config.jsonc`:

	"on-sigusr1": "hide",
    "on-sigusr2": "show",
    "start_hidden": false,

### **▶️ | STEP 4: [ AUTO-START MODULE ]**
Add the `"custom/autohide"` module to your `config.jsonc`:<br>
<br>
*EXAMPLE: `"modules-left": ["custom/autohide","cpu","temperature"]`*<br>

Customize the module as follows:

	"custom/autohide": {
	"exec": "~/.config/waybar/Modules/WaybarAutoHide",
	"interval": "once",
	},

Similarly, if you would like it separate from Waybar, you may use an `exec-once` in your Hyprland.conf:

    exec-once: ~/.config/waybar/Modules/WaybarAutoHide

<br>

### **🔁 | STEP 5: [ TOGGLE MODULE - OPT ]**
Create a *`togglewaybar`* module in `waybar/config.jsonc`:<br>
*[ This will allow you to disable AutoHide when not in-use ]*<br>

    "custom/togglwaybar": {
      "exec": "~/.config/waybar/Modules/WaybarAutoHide module",
      "interval": 1,
      "format": "{}",
      "return-type": "json",
      "on-click": "~/.config/waybar/Modules/WaybarAutoHide toggle"
    }

Add this module to your `modules-left`/`center`/`right`,<br>
*Example: `"modules-left": ["custom/togglewaybar"]`*
	
> [!WARNING]  
> **RESTART WAYBAR AFTER COMPLETION!**  
> Otherwise, this will not work.
  
---

## <p align="center">🌟 FULL INSTALL 🌟<br>[ ENTIRE WAYBAR CONFIG ]</p>

### **📥 | STEP 6: [ IMPORT FILES ]**
Drag all remaining contents:<br>

*`[ /swayosd, /swaync, /waybar ]`*<br>

into your `$HOME/.config` directory.

<br>

### **📦 | STEP 7: [ DEPENDENCIES ]**
Install required packages:

    sudo pacman -S --needed waybar kitty swayosd swaync hyprlock hyprsunset pavucontrol-qt blueman

    yay -S --needed nmgui-bin

---

## <p align="center">✨ STAR HISTORY ✨</p>

<a href="https://www.star-history.com/#cipher-iso/Waybar-Autohide&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=cipher-iso/Waybar-Autohide&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=cipher-iso/Waybar-Autohide&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=cipher-iso/Waybar-Autohide&type=date&legend=top-left" />
 </picture>
</a>
