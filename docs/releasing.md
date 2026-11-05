# Releasing mouser-mode-api

1. Bump `version` in Cargo.toml, update CHANGELOG.md.
2. Commit, tag `vX.Y.Z`, push the tag.
3. `.github/workflows/release.yml` builds the `.crate` package, adds `FILE.sha256` and `FILE.minisig` (minisign, from the `MINISIGN_SECRET_KEY` and `MINISIGN_PASSWORD` secrets) and publishes the GitHub release.
4. `cargo publish` (crates.io).


Assets are named `mouser-mode-api-VERSION-TARGET.tar.gz`, the layout `mouser engine install gh:WeirdBrains/mouser-mode-api` expects.
