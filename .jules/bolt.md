## 2024-10-24 - Async Home Assistant Entity Methods
**Learning:** Home Assistant entity platform methods using blocking I/O (like `time.sleep`) block executor threads, severely reducing overall application performance and responsiveness.
**Action:** Always replace blocking entity methods (e.g., `set_cover_tilt_position`) with their async equivalents (e.g., `async_set_cover_tilt_position`) and substitute blocking calls with async ones (e.g., `await asyncio.sleep()`).
