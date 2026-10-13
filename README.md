# Tray: Click for Menu

Omarchy's system tray, with one change: clicking or tapping an app's tray
icon shows its menu instead of opening the app. On a touchscreen there's no
right click, so the stock tray had no way to reach an app's menu, and a tap on
something like 1Password opened its full window.

- **Click / tap:** shows the app's menu. Apps without a menu still open, as
  before.
- **Right click:** shows the menu (unchanged).
- **Middle click:** the app's secondary action (unchanged).

Everything else, including pinning and hiding icons and the overflow drawer, is
Omarchy's stock tray. It replaces the built-in `omarchy.tray` while enabled
and keeps its settings.

## Install

```bash
omarchy plugin add https://github.com/yeutterg/omarchy-tray-menu --enable
```

## Remove

```bash
omarchy plugin remove io.github.yeutterg.tray-menu
```

Omarchy's tray comes back.

## Keeping up with Omarchy

`Tray.qml` and `TrayModel.js` are copies of Omarchy's (Quattro) with the click
handler changed in one place (search for `omarchy-tray-menu`). After Omarchy
updates its tray, copy the new files and reapply that line.

## License

MIT. `Tray.qml` and `TrayModel.js` are derived from Omarchy's system tray
(MIT, Copyright (c) David Heinemeier Hansson); that notice is kept in
`LICENSE`.
