# Dr.Player

A desktop video player you can draw on, for Windows. Open a video, draw on
the picture, step it frame by frame.

**Version 3.2.0** (read from `Cargo.toml` in the
[Dr.Player](https://github.com/Babar-Meet/Dr.Player) repo at the time of
writing — check the
[releases page](https://github.com/Babar-Meet/Dr.Player/releases) for the
newest published release)

## Download

- **[Installer (Setup)](https://github.com/Babar-Meet/Dr.Player/releases/latest/download/DrPlayer-Setup.exe)**
  Installs per user. No administrator rights needed. Puts Dr.Player in the
  Open with menu for `.mp4`, `.m4v`, `.mov` and `.webm`.
- **[Standalone](https://github.com/Babar-Meet/Dr.Player/releases/latest/download/dr-player-3.2.0.exe)**
  No install at all. One file, just run it.

Those two links always serve the newest published release. Older builds are on the
[releases page](https://github.com/Babar-Meet/Dr.Player/releases).

Download it from [drplayer.pages.dev](https://drplayer.pages.dev).

## What it does

**Play**
Opens `.mp4`, `.m4v`, `.mov` and `.webm` from Explorer's Open with menu.
Play, pause, seek and volume. It becomes the default only when you pick it
in Windows' own UI.

**Waveform seek bar**
A thin live bar from the first frame, with the file's own audio waveform
filling in left to right behind it. Finished decodes are cached on disk, so
reopening is instant. Audio the extractor cannot decode keeps the working
thin bar with no error.

**Frame stepping**
Steps at the file's own rate (24 to 120 fps), falling back to 1/60 s where
the engine stays silent. A measured step, not a frame-accurate seek.

**Resume**
A `Continue from HH:MM:SS` chip, up for ten seconds. Written on pause and
on close, cleared at the end, never written while loop is on.

**Draw**
6 tools: Pen, Line, Arrow, Rectangle, Circle, Hand. 50-level undo and redo,
6 swatches plus a picker, stroke 1–20, draggable toolbar.

**Speed**
Hold Space to fast-forward, with a floating speed pill. Glass panel with a
0.06x–16x slider plus direct entry, presets 1.5x, 2x, 3x and 4x, remembered.

**Window**
Loop, fullscreen, frameless chrome with drag and resize. Hide with H, fill
with C, auto-hide after 3 s. Size and position remembered.

**Keys & CLI**
Bare-key shortcuts with a full panel on `/`. Draw mode keeps its own keys
apart from playback. Single-file launch: `dr-player <file>`.

## What you need

- Windows 10 or newer, 64-bit
- WebView2 runtime (usually pre-installed on Windows 10+)

Download and installed sizes are not listed yet. They will be measured from
a published release, never estimated.

macOS and Linux builds do not exist yet. The download page shows them as
Coming soon.

## Good to know

**It will not ask for administrator rights.** The installer writes to your own
user profile. If it ever did ask, something is wrong.

**Installing does not change your defaults.** Windows keeps that choice
itself. Dr.Player appears in Open with, and becomes the default only once
you pick it in Windows' own UI.

**It does not phone home.** No analytics, no telemetry, no tracking. The only
network traffic the app makes is one optional update check per launch, which
opens the releases page and stays silent otherwise.

## Reporting a problem

Say which version you are on. It is shown next to each release on the
download page.

## About this repo

This is the public distribution channel: the download page and the published
releases. Application source is public at
[github.com/Babar-Meet/Dr.Player](https://github.com/Babar-Meet/Dr.Player);
only the page-plus-releases pattern mirrors PDEA-dist.

The landing page is a single hand-written `index.html` with no build step. Its
design system and the rules for editing it are in [DESIGN.md](DESIGN.md) — read
that first. Any claim on the page must be checked against the app before it is
written down.

© 2026 Babariya Meet. Dr.Player is proprietary software. All rights reserved.
