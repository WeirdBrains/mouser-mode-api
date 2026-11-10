# Changelog

## [Unreleased]

## [0.3.0] - 2026-11-10

### Added

- `PanelStyle::Frame { focused }` (a rounded outline with its title in the top edge) and `PanelStyle::Bubble { mine }` (a rounded message background); a dock item with the action `mouser.dock_full` toggles the host's fullscreen panel. Mouser draws them from 1.5.
- `complete`: Tab completion for text fields (paths relative to a folder with `~`, commands then arguments, known values), with `PathSource` for remote listings.
- `Context.reduce_motion` (default false when the host omits it), `dock_chrome_height` (keep footers above the host's dock chrome), `services::permission_for` (the capability a host service needs), and `codec::write_named` (structs as MessagePack maps keyed by field name, what Mouser sends).
- Panel styles Mouser already drew for its own modes: `Dim(u8)` (a veil and click target), `FontOption`, `ThemePreview`.
- Services: `agent.revoke_all`, `models.hf_search`, `models.hf_details`, `models.hf_install`, `models.hf_cancel` and the `models.download` event; `agent.state` carries `allow_all`.

### Changed

- Docs: Mouser writes its messages as MessagePack maps keyed by field name, so a plugin built against an older mode-api skips fields added since; decoders should accept both shapes.

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
