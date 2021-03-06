# Introduction
Gwent-daily is a bot for gwent the witcher CCG card game. Its based on robust image detection / OCR. Bot helps complete daily quests and smooth new player experience. Bot farms almost 4 packs and some scraps over night.

# Table of contents
1. [Requirements](#requirements)
2. [Features](#features)
3. [Settings](#settings)
4. [Decks](#decks)
5. [How it works](#how)

# Requirements <a name="requirements"></a>
## Main

* 64 bit OS win7sp1-win10

* 1920x1080 or bigger monitor (720p support may come later)

* Gwent with ENGLISH locale. Check [Settings](#settings)

## Nvidia
Bot is optimized for **Nvidia GPU**. Anything past 2013 should work (Kepler, Maxwell, Pascal, Volta, Turing microarchitecture). Install CUDA from link below to get decent performance boost

*  [CUDA10.0](https://developer.nvidia.com/compute/cuda/10.0/Prod/network_installers/cuda_10.0.130_win10_network "CUDA10")

10.0 exactly. 10.1 wont work

*  410.48 or newer graphical driver (for CUDA)

![alt text](https://media.discordapp.net/attachments/571798162059034628/571882157300121615/unknown.png "CUDA install settings")

# Features <a name="features"></a>
Current
* Monster deck
* Easy to start. Deck costs 3-4k scraps
* No injecting. Its safer to use and harder to detect
* Human like mouse movement
* Random sleep timers and coordinates for clicking
* GG after match
* Random bot window name
* Random bot exe name
* Decent winrate (rank 14, 42% winrate)

Planned
* Casual / ranked switch
* Auto updating
* More decks
* Work in background

# Hotkeys

**F10** or **Tab** - stop bot

**F9** - start bot

# Download <a name="download"></a>
Beta is up. Check link above

# Decks <a name="decks"></a>

https://www.playgwent.com/en/decks/cf4e677e4a60181bf4e698bb1ba8e316

# Gwent settings <a name="settings"></a>
FLUX https://justgetflux.com/ or similar tools should be off

options->graphic->premium : DISABLED

options->general->camera move on turn end : OFF

options->general->auto turn end : ON

options->resolution->fullscreen : DISABLED

Gwent must be in **English** language, 1920x1080 or more, windows 7sp1-10, no cyrillic/special symbols/spaces in windows username, latest vcredist x64, and .NET 4.6, **windowed** mode, sometimes u need to run bot as admin

## scaling (can skip with 100% windows scaling)
1) Find gwent game exe (not gog)

![alt text](https://lh3.googleusercontent.com/-Riow_0Aq0t8/WYNSnp25eTI/AAAAAAAAR3o/n2S9JfBVz1gW3nGxFVOBsaugfoMsUp_gACHMYCw/s0/explorer_2017-08-03_19-43-08.png "scaling1")

2) Change scaling mode 

![alt text](https://lh3.googleusercontent.com/-Bzd5Y2jgwIg/WYNSy0QV1II/AAAAAAAAR3s/57RYhR55x8YaGcx6a_9uKq7kVut7UDAmACHMYCw/s0/explorer_2017-08-03_19-43-53.png "scaling2")

3) Change windows scaling

![alt text](https://lh3.googleusercontent.com/-Fk6Ip4vRqw8/WYNS8FxeqmI/AAAAAAAAR3w/0B8tKmYcF78jFDzcGCX3kiGSG3iLQ-XNwCHMYCw/s0/ApplicationFrameHost_2017-08-03_19-44-30.png "scaling3")

4) Reboot PC

# How it works <a name="how"></a>
Neural net [darknet](https://github.com/AlexeyAB/darknet "darknet") to detect cards

OCR, Pixel color checking and image comparing for detecting game state (card count, scores, leader state, end turn, round, etc)

[CoreRT](https://github.com/dotnet/corert "CoreRT") compiller for .NET code