## 2023-10-27 - Home Assistant Thread Blocking
**Learning:** Synchronous `time.sleep` in entity methods blocks the Home Assistant thread pool executor.
**Action:** Always replace blocking synchronous sleeps with `asyncio.sleep` by utilizing the `async_` prefixed versions of Home Assistant entity methods (e.g., `async_set_cover_tilt_position` instead of `set_cover_tilt_position`).
