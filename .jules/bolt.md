## 2024-05-15 - Home Assistant Synchronous Blockers
**Learning:** Using `time.sleep` in Home Assistant custom components blocks executor threads, which can severely degrade performance or cause deadlocks in the integration.
**Action:** Always replace synchronous sleep calls like `time.sleep` with `await asyncio.sleep()` and use asynchronous methods (e.g., `async_set_cover_tilt_position`) instead of their synchronous equivalents.
