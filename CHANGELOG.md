# Changelog

## 0.16.21 / b37

- Online: fixes for match-start synchronization and search retries.
- Practice: save your position with R3 and return with L3. Use Select + R3/L3 if those buttons are already assigned.
- CPU training: choose a move or recorded response to play after a hit or block.
- Frame-data refresh fixes and a clearer input history.
- Updated shader cache for the scenes tested.
- Compatible installed games now receive automatic patches without a full rebuild.

**One-time setup:** install the new launcher in your existing folder to keep your account, saves and settings.

## 0.16.20 / b36

- Fixed a startup crash at 2x/3x when using Full - Grouped readbacks. The fix preserves the selected rendering scale and keeps grouped readbacks available.
- Compatible installations update automatically without a full rebuild.

## 0.16.19 / b35

- Fixed a Ranked crash after character selection.
- Fixed an online disconnect caused by a temporary backlog on a slower PC.
- Merged performance, stability and music playback improvements.
- Connected the launcher nickname to the game’s local profile display.
- Added experimental Vulkan and grouped Direct3D 12 readback options. Direct3D 12 remains the default.
- Increased account capacity and preserved automatic engine patching.

Test release: complete online matches and performance across different PCs still need further testing. Vulkan has known visual issues. The separate unresponsive “Begin Search” report remains under investigation.

## 0.16.18 / b34

- Compact vertical Practice input history with actual button/direction states and frame counts; hides the native bottom history.
- Frame results remain visible after returning to neutral; improved startup observation on missed attacks.
- Separate offline P1/P2 controller assignment and bindings, including same-model pads; improved reconnect handling.
- Fixed scrolling over closed mapping dropdowns.
- Corrected music packet continuation that could stop background music.
- Improved online handling of brief packet-consumption stalls without increasing mailbox limits.
- Optimized scaled texture downsampling with matching pixel output; prepared a bounded shader family before gameplay and fixed shader-cache saving/progress.
- Automatic engine patch, update notice and launcher restart preserved. Small launcher download now lives directly in the repository.

Test release: full-move coverage, complete online matches, all-device rendering/performance and exhaustive zero in-game shader work remain under qualification. Vulkan migration is paused.
