# 🔄 Node.js Event Loop Architecture

Understanding libuv phases and execution order in Node.js runtime.

## Event Loop Phases
1. **Timers**: Executes callbacks scheduled by `setTimeout()` and `setInterval()`.
2. **Pending Callbacks**: Executes I/O callbacks deferred to the next loop iteration.
3. **Idle, Prepare**: Internal libuv operations.
4. **Poll**: Retrieves new I/O events; executes I/O related callbacks.
5. **Check**: Executes `setImmediate()` callbacks.
6. **Close Callbacks**: Executes close events (e.g. `socket.on('close')`).

> `process.nextTick()` and microtasks (`Promise.then`) run immediately between each phase!
