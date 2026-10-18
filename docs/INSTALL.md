# Installation

## macOS (any version supported by Mousecape)

macOS does not allow system cursors to be replaced on disk (the system volume is sealed and read-only since Big Sur). The cursors are applied at runtime with [Mousecape](https://github.com/alexzielenski/Mousecape), a free and open-source cursor manager.

1. Download and open Mousecape.
2. Double-click `macOS27-GoldenGate.cape`, or use **File → Import** in Mousecape.
3. Select *macOS 27 Golden Gate* and press **⌘↩** (Apply).
4. Optional: **Mousecape → Install Helper Tool** so the cape is re-applied after logging in.

To undo: **Mousecape → Reset to Default**.

## Windows 10 / 11

1. Extract the `macOS27-GoldenGate` folder.
2. Right-click `install.inf` → **Install** (on Windows 11: **Show more options → Install**).
3. Open **Settings → Bluetooth & devices → Mouse → Additional mouse settings → Pointers**.
4. Choose **macOS 27 Golden Gate** in the *Scheme* list and click **Apply**.

The installer copies every cursor to `C:\Windows\Cursors\macOS27-GoldenGate` and registers the scheme for the current user. Cursors that have no Windows role (open/closed hand, copy, alias, zoom, etc.) can be assigned manually with **Browse…**.

Each `.cur`/`.ani` file contains 32, 48, 64, 96 and 128 px images, so the cursors stay sharp at any display scaling and pointer size.

To undo: choose the *Windows Default* scheme and click **Apply**.

## Linux

```sh
cd macOS27-GoldenGate
sh install.sh
```

The script copies the theme to `~/.icons/macOS27-GoldenGate` and activates it on GNOME (`gsettings`) and KDE Plasma (`plasma-apply-cursortheme`). On other desktops, select *macOS27-GoldenGate* in the cursor settings, or set it manually:

```sh
# X11 / XWayland
echo 'Xcursor.theme: macOS27-GoldenGate' >> ~/.Xresources
# Hyprland
hyprctl setcursor macOS27-GoldenGate 24
```

To install for all users, copy the folder to `/usr/share/icons/` instead. Log out and back in if some applications keep the old cursor.
