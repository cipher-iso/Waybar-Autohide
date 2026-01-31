# <p align="center">🌘 WAYBAR AUTO-HIDE 🌒<br>[ A SIMPLE BASH SCRIPT ]</p>
<p align="center"><br>
  <img src="https://raw.githubusercontent.com/cipher-xui/Waybar-Autohide/main/Preview.gif" width="700" alt="WAYBAR AUTO-HIDE PREVIEW"/>
</p>

<p align="center">
  <a href="https://github.com/cipher-iso/Waybar-Autohide?tab=readme-ov-file#-partial-install--auto-hide-only-">PARTIAL-INSTALL</a> •
  <a href="https://github.com/cipher-iso/Waybar-Autohide?tab=readme-ov-file#-full-install--entire-waybar-config-">FULL-INSTALL</a> •
  <a href="https://github.com/cipher-iso/Cipher-OS">DOTFILES</a>
</p>

---

## <p align="center">💫 PARTIAL INSTALL 💫<br>[ AUTO-HIDE ONLY ]</p>

### **👥 | STEP 1: [ CLONE REPO ]**
In Your Terminal:<br>
`git clone https://github.com/cipher-iso/Waybar-Autohide.git`

<br>

### **📜 | STEP 2: [ COPY SCRIPTS ]**
Drag the `~/Scripts` directory into your `$HOME` directory.<br>
> [!NOTE]
> *Move all other contents into `~/.config` if you are doing the [Full Installation](#-full-install-entire-waybar-config)*

<br>

### **🧩 | STEP 3: [ WAYBAR CONFIG ]**
Add the following lines to your Waybar `config.jsonc`:

    "on-sigusr1": "hide",
    "on-sigusr2": "show",
    "start_hidden": false,
    "reload_style_on_change": true,
    "layer": "top",
    "position": "top",
    "gtk-layer-shell": true,
    "exclusive": true,

> [!WARNING]  
> **RESTART WAYBAR AFTER THIS STEP!**  
> Otherwise, this will not work.

<br>

### **▶️ | STEP 4: [ RUN SCRIPT ]**
Execute script in background:

    hyprctl dispatch exec ~/Scripts/WaybarAutohide &

***OR*** in `hyprland.conf`:

    exec-once = ~/Scripts/WaybarAutohide

<br>

### **🔁 | STEP 5: [ TOGGLE MODULE - OPT ]**
Export [`WaybarLockModule`](https://github.com/cipher-iso/Waybar-Autohide/blob/main/waybar/WaybarLockModule) into `~/.config/waybar`,  
and create a *toggle* module in `waybar/config.jsonc`:

    "custom/barlock": {
      "exec": "~/.config/waybar/WaybarLockModule",
      "interval": 1,
      "format": "{}",
      "return-type": "json",
      "on-click": "~/Scripts/ToggleWaybar"
    }

---

## <p align="center">🌟 FULL INSTALL 🌟<br>[ ENTIRE WAYBAR CONFIG ]</p>

### **📂 | STEP 6: [ IMPORT FILES ]**
Drag all remaining contents into your<br>
`$HOME/.config` directory.

<br>

### **📦 | STEP 7: [ DEPENDENCIES ]**
Install required packages:

    sudo pacman -S --needed waybar kitty swayosd swaync hyprlock hyprsunset pavucontrol-qt blueman

    yay -S --needed nmgui-bin

<br>

### **📝 | STEP 8: [ PATH EXPORT ]**
Add this to your `.bashrc` or `shell`:

    export PATH="$HOME/Scripts:$PATH"

---

## <p align="center">✨ STAR HISTORY ✨</p>

<a href="https://www.star-history.com/#cipher-iso/Cipher-OS&cipher-iso/Waybar-Autohide&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=cipher-iso/Cipher-OS,cipher-iso/Waybar-Autohide&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=cipher-iso/Cipher-OS,cipher-iso/Waybar-Autohide&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=cipher-iso/Cipher-OS,cipher-iso/Waybar-Autohide&type=date&legend=top-left" />
 </picture>
</a>