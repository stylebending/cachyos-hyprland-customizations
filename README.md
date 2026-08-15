# CachyOS Hyprland customizations

The files I changed from the default CachyOS Hyprland install.

> Everything else uses the stock CachyOS defaults — repo contains only the
> files I actually edited.

## What's here

- `etc/polkit-1/rules.d/51-systemd-transient.rules` — permission fix for sync between desktop and lock screen wallpaper
- `.config/hypr/config/binds.lua` — Hyprland keybindings (noctalia + UWSM aware)
- `.config/hypr/config/variables.lua` — default apps, monitors, workspaces
- `.config/kitty/kitty.conf` — opacity, padding, keymap
- `.config/kitty/themes/noctalia.conf` — kitty color theme (`included` by kitty.conf)

## Install

The layout mirrors the real config paths so you can copy straight over the
stock CachyOS defaults:

```bash
# polkit
sudo cp etc/polkit-1/rules.d/51-systemd-transient.rules /etc/polkit-1/rules.d/51-systemd-transient.rules

# Hyprland
cp .config/hypr/config/binds.lua     ~/.config/hypr/config/
cp .config/hypr/config/variables.lua ~/.config/hypr/config/

# kitty
cp .config/kitty/kitty.conf          ~/.config/kitty/
mkdir -p ~/.config/kitty/themes
cp .config/kitty/themes/noctalia.conf ~/.config/kitty/themes/
```

Reload Hyprland (or re-login) and kitty after copying.
