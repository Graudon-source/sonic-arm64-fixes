# Sonic ARM64 Fixes

# DISCLAIMER:
Every package in this repo and all instructions were made by AI (Claude Code). I am not a developer and have no coding skills, I turned to AI in order to fix the issues listed below because I couldn’t find any fixes on the internet. I will report these issues to the competent developers of the Mesa drivers, dxvk layer and the Hedgemodmanager. So that these problems may be permanently fixed for everyone. I do not claim to be the author of these fixes as I merely prompted the AI to find a solution. Unfortunately these patches only work on ArmadaOS (and I assume other similar Linux distros), they do not work on Android via apps such as GameNative. If anyone wants to adapt such fixes to Android, feel free to do so.

# Description 
Fixes for the Hedgehog Engine 2 Sonic games on ARM64 Linux with Steam, Proton and FEX. Tested on a Retroid Pocket 6 (Snapdragon 8 Gen 2, Adreno 740) with ArmadaOS.

**Download:** https://github.com/Graudon-source/sonic-arm64-fixes/releases/tag/Initial Release

Each package has an installer, uninstaller and a full guide in English (`README.md`) and Italian (`LEGGIMI.md`).

| Package | What it fixes | Games |
|---|---|---|
| `he2-adreno-fix-FINAL.zip` | Black characters, foliage and shadows on Adreno, and colored noise in Sonic Forces on ArmadaOS | Sonic Forces, Sonic Frontiers, Sonic X Shadow Generations |
| `hmm-arm64-fix-FINAL.zip` | Hedge Mod Manager breaks the game on ARM64, and the mod loader can't start | Sonic Forces, Sonic X Shadow Generations, Sonic Origins |
| `sonic-origins-arm64-fix-FINAL.zip` | Sonic Origins crashes near the title screen, and its mods can't load | Sonic Origins |

## Which package do I need?

- **Black lighting:** `he2-adreno-fix-FINAL`.
- **Mods in Forces or Shadow Generations:** `hmm-arm64-fix-FINAL`, on Proton-CachyOS 11. Use it with the lighting fix if your GPU is an Adreno.
- **Sonic Origins:** `sonic-origins-arm64-fix-FINAL`, on Valve's Proton 11.0 (ARM64). It already includes the mod loader repair.

## Test status

| Game | Lighting fix | Mods | Proton used for mods |
|---|---|---|---|
| Sonic Forces | Works | Works, Sonic Forces Overclocked | Proton-CachyOS 11 |
| Sonic X Shadow Generations | Works | Works, 5 mods | Proton-CachyOS 11 |
| Sonic Origins | Not needed | Works, 6 mods | Proton 11.0-2 (ARM64) |
| Sonic Frontiers | Works | Not tested on a standard copy yet (the AI says this because I applied a crack to my legitimate Steam copy to remove Denuvo)| |

Only this device has been tested. Please open an issue with your game, device and result.

## Removing a fix

Each package has `uninstall.sh`, so you can remove a fix once DXVK, Mesa or Hedge Mod Manager handle the problem themselves. Its guide explains the order to follow.

## Good to know

- **Denuvo:** after trying several Proton versions and new prefixes in one day, I got a temporary lockout on Sonic Origins. Change one thing at a time.
- **Game Mode:** if a game stays below the frame limit, turn the limit off in Steam's side panel. In Sonic Frontiers this made frame pacing much better.
- **Desktop mode:** Xwayland crashed twice while Frontiers ran in KDE, closing the game without saving. Game Mode is safer for long sessions.
- **Android launchers:** these fixes do not work in Winlator or GameHub.

## Upstream reports

- DXVK: link to be added
- Mesa (Turnip): link to be added
- ArmadaOS: link to be added
- Hedge Mod Manager: link to be added

![Black lighting before and after](images/black-lighting-before-after.jpg)

## Licence

MIT, see `LICENSE`. These are unofficial fixes, not made by SEGA, Valve or the Hedge Mod Manager team.
