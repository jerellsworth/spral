# Stupid Python RetroArch Launcher

Let me pick roms with a file browser FFS.

## Description

Stupid Python RetroArch Launcher (SPRAL) is a cross-platform, single-file Python script that lets you easily pick RetroArch content using a native file browser. It also attempts to guess the correct core based on your previous behavior for a given directory and file extension. That is, if you pick the FCEUMM core for a `.nes` file that's in the `~/nes_roms` folder, then SPRAL will will choose the same core for other `.nes` files in `~/nes_roms` without asking you.

Caveat: as with most programmer tools, the UI and setup process for SPRAL makes sense to the author, but may be extremely confusing to everybody else. Of course, it's designed to simplify the RetroArch user experience, which a lot of people find pretty confusing to begin with so maybe it's an improvement anyway.

## Install on Macos
brew install python3
brew install python-tk
