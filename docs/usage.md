# Using mouser-mode-api

Protocol, UI model and SDK for Mouser mode plugins (persistent child process, MessagePack over stdio, shared-memory images).

- API reference: [docs.rs/mouser-mode-api](https://docs.rs/mouser-mode-api).
- The wire protocol, services and events: [protocol.md](protocol.md).
- Versioning: the crate follows semver; the protocol `api` number is separate and changes only when the wire breaks.
