# TAG2 PC

An experimental Windows PC project for Tekken Tag Tournament 2, with a launcher, local game builder, configurable controls and graphics, and online play under development.

This repository is a public project overview. It does not contain the complete engine, game data, a ready-to-run game, or a reproducible full source build.

## Getting started

Use a current project release from the maintainer. Keep the complete launcher package together on a writable, local fixed NTFS drive.

The local builder requires your own original game ISO or supported extracted disc files, plus the matching Xbox 360 Title Update. Game files and Title Updates are not distributed here. The builder applies the supported character changes from the Title Update while retaining the base game.

Windows x64 and .NET Framework 4.8 are required. The full build also requires the supported Microsoft C++ compiler and Windows SDK; the launcher offers their installation. Installation may require administrator approval and additional disk space.

## Launcher features

- Online and offline launch modes.
- Keyboard and controller mapping menus.
- Rendering scale, readbacks, presentation VSync, queue depth, display mode and filtering settings.
- Signed update checks, an update notice and launcher restart after installation.
- Automatic engine patches for compatible installed builds, with a full-build fallback when needed.
- Local diagnostic collection and a separate portable benchmark tool.

Keep all package files together when updating. If an update is incomplete, use the maintainer's repair instructions instead of deleting saves or account files. An existing account belongs to its original launcher credentials; reusing its name in a new installation does not recover the account.

## Current status

The engine uses a hybrid architecture with native host components and recompiled guest code. It is not a complete native engine rewrite.

Performance depends on the machine and scene. Colors and textures at higher rendering scales, Practice frame coverage, and online match synchronization still require testing. Synthetic checks and successful builds do not establish correct behavior for every move, every PC, or a complete online match.

Full readbacks are the default. Disabling readbacks may improve performance on some systems, but can remove required colors or effects. Shader preparation covers known cached pipelines; unseen content can still require compilation.

The portable benchmark accepts different game versions. Presentation rate is not simulation FPS, and CPU-to-display timing is not a physical button-to-screen measurement. Captures are saved locally and are not uploaded automatically.

## Reporting a problem

Include the launcher version, graphics settings, CPU/GPU and driver, whether the issue occurs offline, and steps to reproduce it. For online issues, include the versions and settings of both clients. Review any diagnostic archive or screenshot before sharing it; never publish account credentials, saves, game files or private paths.

## References

- [Tekken Tag Tournament 2 frame documentation](https://tekkendocs.com/tag2/) — community reference; move values are checked against TAG2 documentation, not Tekken 6 data.

This is an unofficial project and is not affiliated with or endorsed by Bandai Namco. Tekken and related names belong to their respective owners. No license for third-party game content is granted by this repository.
