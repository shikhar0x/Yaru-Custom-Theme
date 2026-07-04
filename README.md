# Yaru Custom Fedora Theme

A custom-tailored **Yaru icon and theme pack for Fedora** that brings the polished look of Ubuntu's Yaru aesthetic to Fedora while maintaining system-wide visual and color consistency.

## What's Changed

### Custom App Grid Icon

Replaced the default GNOME **nine-dot App Grid icon** with a high-fidelity, theme-aware Fedora logo.

### Symbolic Icon Optimization

Refactored the Fedora logo to work natively as a symbolic icon, allowing it to adapt automatically to:

* Light mode
* Dark mode
* System accent colors

### Theme-Aware Scaling

Optimized vector assets to ensure that the Fedora logo remains sharp and properly scaled across different display resolutions.

### Fedora Compatibility

Fine-tuned the theme directory structure and assets to integrate seamlessly with Fedora's GNOME Shell environment.

---

## Why Use This Theme?

Fedora's default icons and themes provide a clean desktop experience, but the App Grid icon uses GNOME's standard nine-dot design.

This theme replaces it with a Fedora logo while preserving the visual consistency of the Yaru theme.

The result is a desktop environment with:

* Consistent Fedora branding
* Theme-aware symbolic icons
* Proper light and dark mode integration
* Crisp vector assets
* A unified appearance across multiple workstations

---

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

---

## Troubleshooting

### App Grid Icon Not Showing

If the new App Grid icon does not appear immediately, log out and log back in to refresh the GNOME Shell session and icon cache.

### Incorrect Icon Colors

If the icon colors do not match your current theme, check whether your custom GNOME Shell theme contains conflicting color overrides for the `.app-grid-button` class in `gnome-shell.css`.

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
