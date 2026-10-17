# omarchy-theme-switcher

A copy of Omarchy's built-in theme switcher, the slanted image carousel you get from the theme menu.

Copied from the `omarchy` package, version 4.0.4-1.

## Layout

| Path | Original location | What it does |
| --- | --- | --- |
| `plugin/` | `/usr/share/omarchy/shell/plugins/image-picker/` | The `omarchy.image-picker` shell overlay: QML carousel, model, and image lister |
| `bin/omarchy-theme-switcher` | `/usr/bin/omarchy-theme-switcher` | Builds the theme preview cache and opens the picker |
| `bin/omarchy-menu-images` | `/usr/bin/omarchy-menu-images` | Sends the picker its images over the shell's `image-selector` IPC and waits for a selection |

The IPC handler that summons the overlay lives in `/usr/share/omarchy/shell/shell.qml` (`IpcHandler { target: "image-selector" }`). It is not copied here.

## License

Omarchy is MIT licensed. See https://github.com/basecamp/omarchy.
