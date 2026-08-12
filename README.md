# CachyOS Hyprland customizations

The files I changed from the default CachyOS Hyprland install. Drop-in
overrides on top of the stock `/etc/skel` config.

> Everything else uses the stock CachyOS defaults — repo contains only the
> files I actually edited.

## What's here

- `hypr/config/binds.lua` — Hyprland keybindings (noctalia + UWSM aware)
- `hypr/config/variables.lua` — default apps, monitors, workspaces
- `kitty/kitty.conf` — opacity, padding, keymap
- `kitty/themes/noctalia.conf` — kitty color theme (`include`d by kitty.conf)

## Install

The layout mirrors the real config paths so you can copy straight over the
stock CachyOS defaults:

```bash
# Hyprland
cp hypr/config/binds.lua     ~/.config/hypr/config/
cp hypr/config/variables.lua ~/.config/hypr/config/

# kitty
cp kitty/kitty.conf          ~/.config/kitty/
mkdir -p ~/.config/kitty/themes
cp kitty/themes/noctalia.conf ~/.config/kitty/themes/
```

Reload Hyprland (or re-login) and kitty after copying.