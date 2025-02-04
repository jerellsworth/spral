# Stupid Python RetroArch Launcher

"Let me pick roms with a native file picker FFS."

![screenshot](https://github.com/jerellsworth/spral/blob/ffb14246bced258794d1660b22361940553eb080/spral_screenshot.png)

## Description

Stupid Python RetroArch Launcher (SPRAL) is a cross-platform, single-file Python script that lets you easily pick RetroArch content using a native file picker. It also attempts to guess the correct core based on your previous behavior for a given directory and file extension. That is, if you pick the FCEUMM core for a `.nes` file that's in the `~/nes_roms` folder, then SPRAL will will choose the same core for other `.nes` files in `~/nes_roms` without asking you.

Caveat: as with most programmer tools, the UI and setup process for SPRAL makes sense to the author, but may be extremely confusing to everybody else. Of course, it's designed to simplify the RetroArch user experience, which a lot of people find pretty confusing to begin with so maybe it's an improvement anyway.

## Setup

1. Install [RetroArch](https://www.retroarch.com)
2. Install python3
    1. for MacOS with Homebrew, that's `brew install python3`
3. If needed, install Python tkinter
    1. For MacOS with Homebrew, that's `brew install python-tk`
4. Install git
5. Clone this repo (`git clone https://github.com/jerellsworth/spral.git`)
6. Optionally, add the repo's directory to your `PATH`

## Usage

```
usage: spral [-h] [-g] [ROM]

Launch RetroArch

positional arguments:
  ROM

options:
  -h, --help  show this help message and exit
  -g          Force gui
```

If SPRAL can figure out the path to the RetroArch binary executable, the path to the rom, and the path to the relevant core, then you won't see the gui. If SPRAL needs to know any of those paths (or if you run with the `-g` flag) then the GUI will appear. The GUI contains one entry box for each of the three paths. After specifying these paths, click the `Run` button. The three paths that SPRAL needs to know are:

### RetroArch Path:

This is the path to the RetroArch _binary executable_. On Windows, this will be a `.exe` file. In MacOS, this is `not` the path the the app. This is the path to the executable `embedded in` the app. The path on MacOS is usually: `/Applications/RetroArch.app/Contents/MacOS/RetroArch`, but you'll have to manually specify if you put it somewhere nonstandard.

### Core path

This is the path to the `dynamic library` that implements the core. On Windows, this will be a `.dll` file; on MacOS, it will be a `.dylib` file; on Linux, it will be a `.so` file.

### Rom Path

The path to the rom. Extension varies depending on platform.
