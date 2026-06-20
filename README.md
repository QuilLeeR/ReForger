# ReForger

ReForger is a WinUI 3 / .NET 8 desktop tool for creating, editing, installing, and reverting mods for
**Assassin's Creed Shadows**. It focuses on the game's Anvil Pipeline v42 `.forge` containers and uses
ReForger's own compact binary mod package format, RFGB (`.rfgb`).

The app is under active development. Compatibility and authoring features may change between releases.

## Features

- Create and edit RFGB mod packages with metadata, banners, notes, embedded files, and tweak lists.
- Apply and revert enabled tweaks safely by restoring backups before rebuilding the active mod state.
- Patch Shadows `.forge` containers with byte overwrites, splices, replacements, and choice-driven values.
- Manage Choice Sets for selectable mod variants and preview images.
- Use a readable TweakScript patch sheet for inspecting and editing mod target data.
- Keep local toggle and selected-choice state separate from clean exported mod definitions.
- Package protected RFGB mods with device-bound, time-limited installation support.
- Browse and inspect game forge data through the built-in explorer and texture viewer.

## Screenshots

### Overview

![ReForger overview](https://i.imgur.com/UoAgLEy.png)

### Install and Use Mods

![Install a mod](https://imgur.com/nsE0E42.png)

![Use a mod](https://imgur.com/ukK6JQ2.png)

### Patch Editor

![Patch editor](https://imgur.com/xCLFZA3.png)

### Choice Sets

![Choice Sets](https://imgur.com/lCheXWX.png)

## Project Status

ReForger is experimental software for mod authors and advanced users. Always keep backups of game files
and test mods carefully before sharing them.

## Requirements

- Windows 10 version 1809 or newer, Windows 11 recommended.
- .NET 8 SDK for development.
- Windows App SDK runtime.
- Visual Studio with WinUI/MSIX tooling recommended for debugging and packaging.

The app is a single-project MSIX WinUI 3 application. Running the unpackaged `.exe` directly may fail
because WinUI depends on the Windows App SDK runtime registration.

Supported platforms are `x64`

## Repository Layout

```text
Core/        Mod model, RFGB I/O, TweakScript, syntax helpers
Engine/      Shadows forge/container patching, backups, mod installation
Controls/    Code editor and reusable UI controls
Converters/  XAML value converters
ViewModels/  UI view models
Assets/      App images, fonts, documentation screenshots
docs/        Internal implementation and file-format notes
```

## Disclaimer

ReForger is an unofficial community tool. It is not affiliated with, endorsed by, or sponsored by
Ubisoft. Assassin's Creed is a trademark of Ubisoft Entertainment.

## License

This project is proprietary. All rights are reserved by QuilLeeR. See [LICENSE](LICENSE).
