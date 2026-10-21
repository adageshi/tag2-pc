# Changelog

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
