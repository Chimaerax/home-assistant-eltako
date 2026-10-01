## 2024-05-18 - Replacing Blocking sleep calls in HA
**Learning:** Blocking calls like `time.sleep` in entity state changes block HA executor threads, crippling performance.
**Action:** Always prefer non-blocking async `await asyncio.sleep()` alongside `async_` prefixed methods.
