# Setup and launcher guide

## 1. Download and install the launcher

Version **0.16.21 / b37 requires a one-time manual launcher replacement**, including for an existing installation. After this replacement, subsequent updates use the new launcher's update notice.

1. Close **TAG2 and its launcher**.
2. [Download the TAG2 PC launcher 0.16.21](https://github.com/adageshi/tag2-pc/raw/refs/heads/main/TAG2-PC-Launcher-0.16.21.zip).
3. For an existing installation, extract the **entire ZIP into the same folder as your existing Tag2Launcher.exe**. Keep the **launcher-update** subfolder and all other extracted files together. Do not run the installer inside the ZIP or copy files from inside launcher-update by hand.
4. Run **Install-Launcher.cmd** and wait for it to finish.
5. Open **Tag2Launcher.exe**, choose **Install update**, and wait for the remaining components to download. The launcher restarts when installation is complete.

For a fresh installation, extract the complete ZIP to an empty folder on a local, fixed **NTFS** drive and follow the same installer steps. exFAT is not supported by the updater. Internet access is required for initial setup.

Keep the existing installation folder to retain your account, settings and saves. Compatible built games receive an automatic engine patch without a full rebuild or moving the folder. The launcher ZIP is stored directly in the repository. The game, ISO and Title Update are not included.

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
- Use **PLAY** for online play, then create or join rooms through the game's original menus. Both players should update before testing a match. Online stability remains under testing.
- Shader preparation can make startup take longer. Keep the launcher open and wait for it to finish.

## 4. Graphics settings

Open **Play & settings → Graphics...**. Save your changes and **restart the game** to apply them.

| Setting | What it does |
| --- | --- |
| Internal resolution | Selects 1x Native, 2x Standard or 3x High. Higher values need more GPU resources. |
| Resolve readbacks | Full is the default. None - Experimental is available for comparison and can change rendering; see below. |
| Presentation VSync | Can reduce screen tearing, but may increase display latency. |
| Presentation queue | 1 frame favors lower latency; 2 frames adds buffering. |
| Display mode | Borderless fullscreen or Windowed. |
| Texture filtering | Original filtering or an anisotropic filtering override. |

### Slow motion or stutters

Keep **Direct3D 12** and **Full - Default** as the reference when comparing a problem. Change one setting at a time and compare the same scene. The portable benchmark below can record the issue; include your rendering scale and readbacks setting when sharing a capture.

To try the experimental readbacks option when investigating slowdown or stutters:

1. Close the game.
2. Open **Play & settings → Graphics...**.
3. Set **Resolve readbacks → None - Experimental** and click **Save**.
4. Relaunch the game and compare the same Practice scene.

**None - Experimental can cause missing colors, textures or effects.** It is not a guaranteed fix for every PC and does not repair connection problems. If rendering changes after a tweak, restore **Full - Default**, save and restart.

The portable graphics-preparation cache covers tested scenes. The latest first-tag test at 2x was reported smooth; this does not cover every stage or team. See the [changelog](CHANGELOG.md) for the release's scope.

## Practice displays

Use the game's Practice display settings: **Command History** enables the custom vertical history and hides the original bottom bar; **Hit Analysis** controls the frame panel. Rows show actual directions, buttons and held/neutral durations. Verified completed results stay visible at neutral. A whiff has no hit/block advantage, and unsupported reactions show unknown rather than a guessed value.

This update improves frame-data refresh and command-history readability, adds R3/L3 position save and recall shortcuts with Select combinations when those buttons are assigned to moves, and adds conditional CPU responses in Defensive Training using the selected native command-list or recording slot and the game's existing recording controls.

## 5. Updates after the one-time replacement

When the new launcher shows **Update available**, choose **Install update**. The launcher restarts after installation and automatically patches a compatible installed game. You normally do not need to manually rebuild after every update.

If the local game is missing or cannot be patched, the launcher may request **Build game** with your original files. Keep the complete installation folder together; do not replace only the launcher executable.

## 6. Capture a performance problem

1. [Download the portable benchmark](TAG2-Benchmark-Portable.zip) and extract it completely.
2. Start the game and enter the fight or Practice scene you want to measure.
3. Open the benchmark, select the appropriate capture and start it. Keep the game in the foreground and stay in the same scene until it finishes.
4. Share the resulting capture ZIP privately with the project support contact. Include the rendering scale, readbacks setting, whether the test was offline or online, and when slowdown occurred.

The benchmark works across game versions. It does not measure physical button-to-screen latency. Review diagnostics before sharing; do not publish account credentials, tokens or personal information in an Issue.

## Troubleshooting

- **Updating from an older launcher:** install the complete 0.16.21 ZIP once with **Install-Launcher.cmd** in the same installation folder, then use **Install update** in the new launcher.
- **Update fails on exFAT:** use a local fixed NTFS drive and extract the full launcher package there.
- **Compiler/SDK setup fails:** keep the exact error and setup-log location shown by the launcher. Repeatedly starting setup will not explain the underlying failure.
- **Missing colors after a tweak:** restore **Resolve readbacks → Full - Default** and restart.
- **Online freeze or disconnection:** update both clients, note the point where it froze, and collect logs from both players. Online stability remains under testing.
- **Other problems:** use **Collect logs** and report your version and reproduction steps through [Issues](https://github.com/adageshi/tag2-pc/issues), without posting private account data.

## Experimental graphics options

Direct3D 12 and Full readbacks remain the defaults. Vulkan and Full - Grouped readbacks are experimental. Vulkan has known visual errors, and grouped readbacks apply to Direct3D 12 only. Compare with the default settings if colors, textures or effects change. Settings apply on the next game launch. The experimental Vulkan work and performance changes without sufficient validation described in the b37 changelog are not included in this release.
