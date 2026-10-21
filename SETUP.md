# Setup and launcher guide

## 1. Download and extract

1. [Download the TAG2 PC launcher 0.16.18](https://github.com/adageshi/tag2-pc/raw/refs/heads/main/TAG2-PC-Launcher-0.16.18.zip).
2. Extract the **entire ZIP** into a folder on a local, fixed **NTFS** drive. Do not run the launcher inside the ZIP. exFAT is not supported by the updater.
3. Keep all extracted files and folders together, then run **Tag2Launcher.exe**.
4. On a fresh installation, choose **Install update** and wait for the remaining components to download. The launcher restarts when installation is complete. Internet access is required for this first setup.

The launcher ZIP is stored directly in the repository. Use the download link above, then extract the inner launcher folder completely. The game, ISO and Title Update are not included.

## 2. Build your game the first time

You need your own original **Tekken Tag Tournament 2 ISO** (or supported extracted disc files) and the matching **Xbox 360 Title Update**. Neither is included in the download.

1. Open **Updates → Build game**.
2. Browse to your game ISO or extracted game, then select the Title Update file.
3. Start the build. The launcher offers installation of the required C++ tools and Windows SDK if they are missing. Follow the Windows prompts and let setup finish.
4. Wait for the build to complete before launching. Keep the original files available in case a full rebuild is requested later.

Only the supported character changes from the Title Update are applied. If setup or building fails, keep the displayed error and use **Collect logs** when available. Do not delete your existing game or saves to retry.

## 3. Name, controls and play

- Set your player name and use **Save name**. Keep your existing launcher folder to preserve your local account. A name already belonging to an account cannot simply be claimed again from a fresh installation.
- Open **Keyboard controls** to bind keys. In **Controllers**, choose **Player 1** or **Player 2**, select the connected controller for that player, and choose each binding from its list or use **Bind**. **Add** retains an alternative input. Save and restart the game. For offline two-player play, assign a different controller to each player, then join through the game menus. Devices with no stable identifying information may need reselection if identical pads are reconnected in a different order.
- Use **Play Offline** for offline modes such as Practice.
- Use **PLAY** for online play, then create or join rooms through the game's original menus. Both players should update before testing a match.
- Shader preparation can make startup take longer. Keep the launcher open and wait for it to finish.

## 4. Graphics settings

Open **Play & settings → Graphics...**. Save your changes and **restart the game** to apply them.

| Setting | What it does |
| --- | --- |
| Internal resolution | Selects 1x Native, 2x Standard or 3x High. Higher values need more GPU resources. |
| Resolve readbacks | Full is the default. None is an experimental performance workaround; see below. |
| Presentation VSync | Can reduce screen tearing, but may increase display latency. |
| Presentation queue | 1 frame favors lower latency; 2 frames adds buffering. |
| Display mode | Borderless fullscreen or Windowed. |
| Texture filtering | Original filtering or an anisotropic filtering override. |

### Slow motion or stutters

One tester reported persistent slowdown with the default readbacks setting and normal speed with **None**. To try the same workaround without changing resolution:

1. Close the game.
2. Open **Play & settings → Graphics...**.
3. Set **Resolve readbacks → None - Experimental**.
4. Click **Save** and relaunch the game.
5. Test the same Practice fight to compare.

**None can cause missing colors, textures or effects.** If that happens, return to **Full - Default**, save and restart. It is not a guaranteed fix for every PC and does not repair connection problems. Change one option at a time when comparing results.

## Practice displays

Use the game’s Practice display settings: **Command History** enables the custom vertical history and hides the original bottom bar; **Hit Analysis** controls the frame panel. Rows show actual directions, buttons and held/neutral durations. Verified completed results stay visible at neutral. A whiff has no hit/block advantage, and unsupported reactions show unknown rather than a guessed value.

## 5. Updates

When **Update available** appears, choose **Install update**. The launcher restarts after installation and automatically patches a compatible installed game. You normally do not need to manually rebuild after every update.

If the local game is missing or cannot be patched, the launcher may request **Build game** with your original files. Keep the complete installation folder together; do not replace only the launcher executable.

## 6. Capture a performance problem

1. [Download the portable benchmark](TAG2-Benchmark-Portable.zip) and extract it completely.
2. Start the game and enter the fight or Practice scene you want to measure.
3. Open the benchmark, select the appropriate capture and start it. Keep the game in the foreground and stay in the same scene until it finishes.
4. Share the resulting capture ZIP privately with the project support contact. Include the rendering scale, readbacks setting, whether the test was offline or online, and when slowdown occurred.

The benchmark works across game versions. It does not measure physical button-to-screen latency. Review diagnostics before sharing; do not publish account credentials, tokens or personal information in an Issue.

## Troubleshooting

- **Update fails on exFAT:** use a local fixed NTFS drive and extract the full launcher package there.
- **Compiler/SDK setup fails:** keep the exact error and setup-log location shown by the launcher. Repeatedly starting setup will not explain the underlying failure.
- **Missing colors after a tweak:** restore **Resolve readbacks → Full - Default** and restart.
- **Online freeze or disconnection:** update both clients, note the point where it froze, and collect logs from both players. Online stability remains under testing.
- **Other problems:** use **Collect logs** and report your version and reproduction steps through [Issues](https://github.com/adageshi/tag2-pc/issues), without posting private account data.
