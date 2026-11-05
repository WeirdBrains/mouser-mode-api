# Changelog

## [Unreleased]

## [0.2.0] - 2026-11-05

### Added

- `DockSize` (`view.resized` carries `dock`: the height the user chose, or fullscreen) with `DockSize::height` and `DockSize::from_payload`.
- Context menus: the host sends `menu.open`; a mode answers `Out::Menu { x, y, entries }` (`MenuEntry`: id, arg, label, key, enabled), or `Host::menu` from `serve()`. Backward compatible: older hosts never send `menu.open`, and `Menu` is the last `Out` variant.
- Docs: `ClipboardSet` needs no permission (Mouser 1.4).

### Changed

- Docs: `Effect::Cd` is never typed into the shell; without a shell integration the host shows a notice.

## [0.1.0] - 2026-11-05

### Added

- First release on its own, extracted from [Mouser](https://github.com/WeirdBrains/mouser) with its history. Protocol, UI model and SDK for Mouser mode plugins (persistent child process, MessagePack over stdio, shared-memory images).
