# Frost's Studio

Where MX Bikes content is made — the paint Designer, Paint Studio, Track Studio and the
rider rig.

**This repository holds releases only.** The source lives with its sibling in
[`Frostn1/mxb-app`](https://github.com/Frostn1/mxb-app), under `apps/studio`, because the two
applications share a great deal: one copy of the game's file formats (`crates/core`), one 3D
viewer and UI kit (`packages/shared`), and one config folder — so a bike the Studio paints is
a bike [Frost's Mod Manager](https://github.com/Frostn1/mxb-app) already knows about.

## Why releases are here and not there

A Tauri updater endpoint reads `releases/latest`, which resolves to **one release per
repository**. The mod manager's endpoint points at `mxb-app` and is baked into every copy
already installed. Publishing a Studio build there would hand every manager install a Studio
build as its next update — so the Studio gets its own repository, its own `releases/latest`,
and its own signing key.

Releases are cut by `.github/workflows/release-studio.yml` in the source repo, from tags
named `studio-v*` there, which land as `v*` here.

## Downloads

See [Releases](https://github.com/Frostn1/frost-studio/releases). Windows is the primary
build — MX Bikes runs on Windows — with macOS and Linux builds alongside it.
