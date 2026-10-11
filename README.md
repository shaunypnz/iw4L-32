# IW4L-32

**IW4L-32 is the 32-player edition of [IW4L](https://github.com/vladtrc/iw4L)**, the open-source Rust runtime for
Call of Duty: Modern Warfare 2 (2009). It is made by the team behind
[IW4x-32](https://github.com/shaunypnz/iw4x-32), the 32-player patch for IW4x, and brings that mod to IW4L.

> **Status: in development, no release yet.** Until the first IW4L-32 release, the source in this fork is
> unmodified upstream IW4L. The 32-player build and its launcher will be published here as release builds.

## What this fork is

- **A fork of [vladtrc/iw4L](https://github.com/vladtrc/iw4L).** Upstream is credited and its license kept (see below).
- **32 players.** Upstream IW4L caps a match at 18 players. IW4L-32 raises the cap to 32 (lobby, master, scoreboard,
  networking and bots) and ports the IW4x-32 server behaviour where IW4L has the same systems.
- **Release builds, not a source mirror.** This repository is where IW4L-32 builds are published: the game
  executable, the IW4L-32 launcher, the license files and the update manifest.
- **Self-updating launcher.** The IW4L-32 launcher (written in Rust) checks this repository on every start,
  downloads changed files, verifies their SHA-256 checksums, and then starts the game.
- **Tracks upstream.** New IW4L commits are watched for and merged into IW4L-32 after the same tests as every release.

## Playing (once released)

1. Download the IW4L-32 release from this repository and extract it into an empty writable folder.
   Only use builds from this repository. IW4L-32 builds are never shipped as password-protected archives.
2. Launch `iw4l32.exe`. It updates itself, finds MW2 in your Steam libraries and creates a
   `Modern Warfare 2.lnk` shortcut next to itself. For an install outside Steam, create that shortcut to your
   MW2 folder yourself.
3. For online play, put the `.iw4l-server` file you received from a server operator next to the executable.
   With it the game finds that master and updates itself on launch.

You need your own installed copy of MW2 Multiplayer. Neither IW4L nor IW4L-32 distributes game assets; the
installation is read, never patched or replaced.

## Upstream acknowledgements and license

Thank you to all contributors for code, bug reports, testing and feedback.
Special thanks to **ju1cedr1nker** and **silvernote03** for QA testing weapons,
maps, attachments and other gameplay features.

[OpenAssetTools](https://github.com/Laupetin/OpenAssetTools) and its [iw4x-x64
fork](https://github.com/iw4x-x64/oat) informed asset layouts;
[IW4x](https://github.com/iw4x/iw4x-client) informed asset and protocol behavior;
[KisakCOD](https://github.com/SwagSoftware/KisakCOD) informed engine structure.
[Ghidra](https://github.com/NationalSecurityAgency/ghidra) was used to inspect the
original binaries.

Movement implementation history and source boundaries are recorded in
[its provenance note](docs/provenance/movement-iw4.md).

IW4L's source is licensed under [Apache 2.0](LICENSE). Preserve required attribution and
bundled font license texts when redistributing; see [NOTICE](NOTICE). Original game
assets and trademarks belong to their owners. IW4L is unaffiliated with them.

IW4L-32 is not affiliated with Activision, Infinity Ward or the upstream IW4L authors.
