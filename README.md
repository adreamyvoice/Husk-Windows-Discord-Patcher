# Discord Voice Node Patcher

Better Discord voice quality: **48 kHz, 384 kbps, true stereo**, with adjustable gain (1x–10x).

## How it works

Discord's voice module ships with hard-coded limits — 24 kHz mono at a low bitrate. This patcher edits a handful of bytes inside `discord_voice.node` to flip those limits to studio-grade settings. The original file is backed up first, so you can roll back any time.

Step by step:
1. Closes Discord.
2. Backs up the existing `discord_voice.node`.
3. Compiles a tiny C++ helper using your installed compiler.
4. Patches 19 specific offsets inside the voice module.
5. Restarts Discord.

## Run it

1. Download `Discord_voice_node_patcher.ps1`.
2. Right-click → **Run with PowerShell** (it auto-elevates to admin).
3. Pick your client, set the gain, click **Patch**.

## Requirements

- Windows
- A C++ compiler — Visual Studio with the "Desktop development with C++" workload (recommended), MinGW-w64, or LLVM/Clang. If none is found, the patcher pops up a download link.

## Restore

Run the patcher again and click **Restore** in the GUI.

## Credits

Made by **Voice**.

> ⚠️ Modifies Discord files. Use at your own risk. Re-run after Discord updates. Not affiliated with Discord Inc.
