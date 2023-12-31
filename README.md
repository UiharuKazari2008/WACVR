<div align="center">
	<br/>
	<p>
    <img src="https://github.com/UiharuKazari2008/WACVR/blob/main/PreviewImages/WACVR-LOGO.png?raw=true" width="546" />
	</p>
  <br/>
  <p>
    <h2><i>
      an open source vr arcade simulator
    </i></h2>
  </p>
  <p>
    <a href="https://github.com/UiharuKazari2008/WACVR/actions"><img src="https://github.com/UiharuKazari2008/WACVR/actions/workflows/build.yml/badge.svg" alt="Build status"/></a>
</div>

## Notice
This is a personal build and is mainly for LTS support and archival for when its removed again

## Preview
<img src="https://github.com/UiharuKazari2008/WACVR/blob/main/PreviewImages/Preview.jpg?raw=true" width="350" />

## About this project
- Model is almost 1:1 to physical cabinet
- Supports every game version
- Supports native touch input via serial (com0com required)
- Supports lights/LEDs (via hook)
- Customizable haptic feedback
- 4 customizable buttons
- 3rd person and smoothed 1st person cameras

## About this fork
Please note that you should refer to the parent fork for the latest updates, I will pull as needed but I would prefer my fork to considered custom
- Updated Enviorment to make it feel like your not in a void
- Moved Controls behind (Once configured you really are not touching them again)
- Panel Locked by Default
- Added posters on the walls
- Updated lighting
- Avatar with hands
- Modified colider to be hand shaped for more accuracy
- LIV was removed for in engine avatar
- This fork may contrain purchaced assets and or copyrighted material
  - Note to self: Please check assets before making a pull request
- May not be as 100$ performant as the parent as im focusing more on immersion

Also this fork will be a mess for a while as i work my trough all my ideas

## Planned Changes
- Use VRChat Avatars for streaming
- Adjustable colider depth
- Needs a lot of IK work
- Add options to things been added

## Supported platforms
- All SteamVR devices (Index, HTC, Oculus, etc.)
- All Oculus devices (Oculus Desktop App)
> Tested on: Quest 2 through Oculus Link (Native and via SteamVR), ALVR and Virtual Desktop (via SteamVR).

## Repositories used
- [Brokenithm-iOS](https://github.com/esterTion/Brokenithm-iOS)
- [IL2cppStartProcess](https://github.com/josh4364/IL2cppStartProcess)
- [MaiDXR](https://github.com/xiaopeng12138/MaiDXR)
- [uWindowCapture](https://github.com/hecomi/uWindowCapture)

## Disclaimers
- This project is not-for-profit and some resources came from the Internet!
- Although this repository is under the GPL-3.0 license, do not use any content of this repo in commercial/profitable scenarios without permission!
- Please support your local arcade if you can!

## How to use
- Obtain the game
- You have 2 ways to setup the game, Automated (recommended) or Manual.

### Automated (recommended)
[Video Tutorial](https://www.youtube.com/watch?v=bViY68ltIz8)<br/>
Automated setup configures the game and downloads WACVR, xxxxtools, and other files for you.  
Thank you to Glub Glub for releasing this!
- Download [Glub Glub setup environment](https://mega.nz/file/cBhh3ZZC#HpifcOQiHdxvMOJCwVPuRXtSuPoRPCsycciZ2_awD_0) and extract it to a folder.
- Then, follow the `README.txt` file inside to add and setup your game.
- Add a server in `Game\app\bin\xxxxtools.ini` to connect to.
- Once done, run `Launch` shortcut to start both WACVR and the game.

---

### Manual
- Make sure the game properly and uses latest xxxxtools.
- Download [the nightly version of WACVR](https://nightly.link/UiharuKazari2008/WACVR/workflows/build/main/artifact.zip).
- You have 2 ways to connect touch to the game. Please only choose one of them:

#### mercuryio
  - Download [GlubGlub](https://mega.nz/file/cBhh3ZZC#HpifcOQiHdxvMOJCwVPuRXtSuPoRPCsycciZ2_awD_0).
  - Put ``mercuryio.dll`` into ``bin`` folder.
  - Add ``[touch] enable=1`` to .ini file
  - Add ``[mercuryio] path=mercuryio.dll`` to .ini file.
  - Start the game and WACVR.

#### Serial (not recommended)
  - Download and install [com0com](https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/powersdr-iq/setup_com0com_W7_x64_signed.exe).
  - Configure com0com to bind COM3 and COM5, COM4 and COM6.
  - Enable the ``enable buffer overrun`` option in com0com on both ports of all pairs. Otherwise, your WACVR will crash after the logo.
  - Add ``[touch] enable=0`` to .ini file
  - Start WACVR first then start the game.
  - If your touch is not working, try to somehow go to Test mode then exit Test mode.

- The lighting requires ``mercuryio.dll``. You must set it up to get the lights from the game. If you don't have the lights, please check if you are using the latest xxxxtools and if your LED hook works.

## Configuration
A ``config.json`` file is automatically created in WACVR's root directory on startup.

- You can change this file via the in-game config panel. Please take a step back: the controller pointer will automatically be disabled when the controller is too close to the cabinet.
- You can change ``batFileLocation`` in ``config.json`` to the location of your start.bat file. The start.bat will automatically run when you start WACVR. 
- Some options in ``config.json`` are only the index of the dropdown in the panel.
- You can use the pointer to point the 3rd-person camera and move it to the position you want it to be.

## Building guide
- Current Unity version: 2021.3.12f1
- for mercuryio, just replace files in mercuryio folder with files in this repo.

## Known issues
- Display white screen issue
	- **Solution:** Set game priority in the task manager to real-time may solve this issue. But the best way is just by capturing the entire screen.

Huge thanks to everyone that helped with this project!
If you want to add any features or change anything, please commit a pull request. I will accept it as soon as possible!
