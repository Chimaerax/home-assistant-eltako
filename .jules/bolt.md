## 2024-05-15 - Async Optimization in Home Assistant Custom Components
**Learning:** Using synchronous blocking calls like `time.sleep()` in Home Assistant custom components blocks the executor thread pool and impacts overall system performance.
**Action:** Always use asynchronous alternatives such as `asyncio.sleep()` within async methods (e.g., `async_set_cover_tilt_position`) when introducing delays.
