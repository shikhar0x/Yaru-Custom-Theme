## Installation

### Extract the Theme

Create the local icons directory if it does not already exist:

```bash
mkdir -p ~/.local/share/icons/
```

Extract the theme archive:

```bash
tar -xvzf /path/to/Yaru-Custom-Theme.tar.gz -C ~/.local/share/icons/
```

> [!NOTE]
> Replace `/path/to/Yaru-Custom-Theme.tar.gz` with the actual path to the archive.

### Apply the Theme

Set Yaru as the active icon theme:

```bash
gsettings set org.gnome.desktop.interface icon-theme "Yaru"
```

The custom Yaru icon theme should now be active.

---

## Portability

### Include Custom GNOME Shell CSS

If you have also modified the `gnome-shell.css` file or created a custom `Yaru-Fedora` shell theme, you can include both the icon theme and shell theme in a single archive:

```bash
tar -cvzf MyCustomThemePack.tar.gz \
    -C ~/.local/share/icons/ Yaru/ \
    -C ~/.local/share/themes/ Yaru-Fedora/
```

This keeps all theme customizations together in a single portable archive.

### Automate Installation

For easier deployment across multiple workstations, consider adding an `install.sh` script to the theme pack.

The script can automatically:

* Create the required directories
* Install the icon theme
* Install the GNOME Shell theme
* Apply the required `gsettings` configuration

The entire theme can then be installed with:

```bash
./install.sh
```

> [!TIP]
> An installation script makes the theme pack easier to maintain, share, and deploy consistently across multiple workstations.
