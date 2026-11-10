# mouser-mode-api

Protocol, UI model and SDK for Mouser mode plugins (persistent child process, MessagePack over stdio, shared-memory images).

Part of [Mouser](https://github.com/WeirdBrains/mouser), the terminal emulator. Mouser and every plugin are built on this crate.

## Install

```toml
[dependencies]
mouser-mode-api = "0.4"
```

## Build

```sh
cargo build
cargo test
```

## Documentation

- [docs/](docs/README.md)
- Mouser: [plugins](https://github.com/WeirdBrains/mouser/blob/main/docs/plugins.md), [engines](https://github.com/WeirdBrains/mouser/blob/main/docs/engines.md), [installing and updating](https://github.com/WeirdBrains/mouser/blob/main/docs/downloads.md)

## Releases and signatures

Published on [crates.io](https://crates.io/crates/mouser-mode-api). GitHub releases are signed with the WeirdBrains minisign key ([minisign.pub](minisign.pub), `61BA1720747F9146`), the key Mouser pins for official plugins and engines:

```sh
minisign -Vm FILE -P RWRGkX90IBe6YaOypKF9r1wz4OqpCp3Ggb1Ag2omAzxTRaqoHzsNQSdP
```

## License

BSD-3-Clause, see [LICENSE](LICENSE).
