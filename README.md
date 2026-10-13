# Tray for Touch

Omarchy's system tray, fixed for touchscreens. The stock tray opens its drawer
on hover, and a finger only "hovers" while it's touching: a tap opened the
drawer for an instant, slid an app's icon under the finger, and the same tap
launched that app (1Password, full screen). Lifting the finger closed the
drawer again, so there was no way to tap an icon on purpose.

- **Tap the arrow (‹):** the drawer opens and stays open.
- **Tap an icon:** opens that app, as usual (right click: its menu; middle
  click: its secondary action). Taps in the first half second after the drawer
  opens are ignored, so the opening tap can't launch anything.
- The drawer closes after you use an icon, after a few idle seconds, or when
  you tap the arrow again. With a mouse, hover still opens it as before.

Everything else, including pinning and hiding icons, is Omarchy's stock tray.
It replaces the built-in `omarchy.tray` while enabled and keeps its settings.

## Install

```bash
omarchy plugin add https://github.com/yeutterg/omarchy-tray-touch --enable
```

## Remove

```bash
omarchy plugin remove io.github.yeutterg.tray-touch
```

Omarchy's tray comes back.

## Keeping up with Omarchy

`Tray.qml` and `TrayModel.js` are copies of Omarchy's (Quattro). The changes
are marked `omarchy-tray-touch`: the `stuckOpen`, `hovering` and `justOpened`
lines. After Omarchy updates its tray, copy the new files and reapply them.

## License

MIT. `Tray.qml` and `TrayModel.js` are derived from Omarchy's system tray
(MIT, Copyright (c) David Heinemeier Hansson); that notice is kept in
`LICENSE`.
