


# Sway Menu

A script to use [sway](https://github.com/swaywm/sway) with a dmenu-like application to choose between windows/workspaces. The purpose is to avoid having workspace-specific bindings like `$mod+1 workspace 1` and never worry about how many workspaces exist or what their names are.

## Actions

Call as `swaymenu action` where `action` may be:

```
new      create a new workspace and focus it
moveout  go with the focused window to a new workspace
focus    focus a hidden window
change   focus a hidden workspace
bring    move a workspace to the focused output
swap     swap the focused window with another window
permute  permute all visible workspaces
give     send the focused window to a hidden workspace
take     take a window from another workspace
hide     hide all floating windows into the scratchpad
unhide   bring forward a scratchpad window
rename   set name of the focused workspace
```

If the window/workspace/scratchpad window in question is ambiguous, `$MENU` is called to choose between the candidates. Bind the desired actions in the sway config and you are good to go.

## Demo

https://github.com/ivomac/swaymenu/assets/45886067/39019a8b-298c-4a9f-bcd8-50ecc71b9951

## Config

It uses `$MENU` (default: dmenu) as the menu program. The output names (like eDP-1) can be remapped to an expression of your choice by modifying `OUTMAP` or with an env. variable:

```
SWAYMENU_OUTPUTS="eDP-1:Laptop;DP-4:Monitor"
```

