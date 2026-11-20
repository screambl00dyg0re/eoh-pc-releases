<div align="center">

# JoJo's Bizarre Adventure: Eyes of Heaven, PC port

An unofficial, free fan port of the PS4 game to Windows. It runs the original game code natively on your PC, at 60 FPS, with modern anti-aliasing and upscaling.

[**Download the latest beta**](../../releases) · [Report a bug](../../issues/new/choose) · [Changelog](../../releases)

</div>

> [!IMPORTANT]
> **No game files are included, and none ever will be.** You need your own dump of your own copy of the European PS4 release, **CUSA04909, version 01.00** (base game, no update). Please don't ask for the game or share it here.

## What this is

Eyes of Heaven never came to PC. This project takes the PS4 version and runs its code directly on your processor (the PS4 uses the same kind of CPU as a PC), with a custom layer standing in for the PS4's system software and the graphics translated to Vulkan. It's not an emulator you load a game into: it's a standalone program built around your copy of the game.

It started from [SpartanPort](https://github.com/FelipePrado0/gow3_pc), the native God of War III port, and uses graphics code from [shadPS4](https://github.com/shadps4-emu/shadPS4).

## Features

**Frame rate**
- 60 FPS, with the game's timing fixed to match: fight speed, the match timer, voice lines, Dual Heat Attacks, Dual Combos, stage intros, story cutscenes and menus all play at their original pace.
- The original 30 FPS is still there if you want it.
- Optional "Fast menus" for quicker menu animations.

**Graphics**
- Anti-aliasing and upscaling: NVIDIA DLSS (RTX cards), AMD FSR 4, FSR 3.1, SMAA or FXAA.
- Render at 1080p (original), 1440p or 4K.
- Up to 16x texture filtering.

**Fixes**
- The voice-line dropouts the game has under emulation are fixed.
- Two start-up freezes (black screen, endless loading icon) are fixed.

**Launcher**
- Checks your game folder and tells you in plain words if it's the wrong region or version.
- Undoes the DLC-loader patch found in some dumps, without touching your files.
- Picks a recommended anti-aliasing setting for your graphics card.
- "Report a problem" saves your logs and PC details as one zip (your Windows user name is removed).
- Tells you when a new version is out.

## Getting started

1. Download `EyesOfHeaven-PC-<version>.zip` from [Releases](../../releases).
2. Extract the whole folder somewhere normal, like `C:\Games\EyesOfHeaven`.
3. Open `Eyes of Heaven.exe` and point it at your game dump. If Windows says "Windows protected your PC", click **More info**, then **Run anyway** (the program isn't digitally signed).

To update, extract the new zip over the old folder. Your saves and settings in the `user` folder stay.

The first start and the first match load slower than later ones while shaders are prepared.

**Needs:** Windows 10 or 11 (64-bit), a graphics card with Vulkan support, and a controller (keyboard works too).

## Status

This is a beta. Story Mode, Free Battle and the menus are playable with a controller, but it has only been tested on a few PCs so far, mostly NVIDIA.

Coming up next:
- Xbox button icons when you play on an Xbox controller
- A mods folder for costume and color mods
- Online multiplayer (working in testing), with rollback planned after
- Smoother story cutscenes at 60 FPS

Known issues are listed with each [release](../../releases).

## Reporting a bug

In the launcher, click **Report a problem**. It saves a zip on your Desktop. Then [open a bug report](../../issues/new/choose), attach the zip, and say what happened and how to make it happen again. A screenshot or short clip helps a lot for anything visual.

Not worth reporting yet: online play not working, other regions or versions being refused, and the Windows "unsigned program" warning. Those are known.

## FAQ

**Is this an emulator?** No. The game's own code runs natively; only the PS4's system libraries and graphics are replaced.

**Can I use the Japanese or US version?** Not yet. Only the European release (CUSA04909, 01.00) is supported for now.

**Does online work?** Not in the public beta yet. It's being tested separately.

**AMD or Intel graphics?** They should work through Vulkan, but they're barely tested. Reports are very welcome.

**Will it cost anything?** No. It's free, there are no donations, and it never will be sold.

## Credits

- [Felipe Prado](https://github.com/FelipePrado0/gow3_pc) for SpartanPort, the God of War III port this builds on
- deadinside28 ([bloodborne_pc](https://github.com/deadinside28/bloodborne_pc)) and Supermedo ([bloodborne_pc for Windows](https://github.com/Supermedo/bloodborne_pc)), whose native ports SpartanPort comes from
- The [shadPS4](https://github.com/shadps4-emu/shadPS4) team for the video core, and cuesta4 for the [shadPS4 fork](https://github.com/cuesta4/shadPS4/tree/eltutz) with its rendering fixes
- Open-source libraries: SDL3, FFmpeg, Dear ImGui, LibAtrac9, sirit, xbyak, Vulkan Memory Allocator, FSR, SMAA and others (full list in each release's source zip)

## Legal

Not affiliated with or endorsed by Bandai Namco, CyberConnect2, Sony or Shueisha. JoJo's Bizarre Adventure belongs to its owners. This port contains no game data.

The port's code is free software under the GNU GPL v2 or later. Each release has its source code attached.
