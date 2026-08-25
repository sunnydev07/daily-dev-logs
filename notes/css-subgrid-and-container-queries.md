# 🎨 Modern CSS: Subgrid & Container Queries

Unlocking responsive component design without relying solely on viewport media queries.

## Container Queries
`css
.card-container {
  container-type: inline-size;
}

@container (min-width: 450px) {
  .card {
    display: grid;
    grid-template-columns: 1fr 2fr;
  }
}
`

## CSS Subgrid
Aligns nested child elements directly with parent grid tracks:
`css
.card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.card-item {
  display: grid;
  grid-template-rows: subgrid;
  grid-row: span 3;
}
`
"@
    },
    @{
        File = "notes/node-event-loop-architecture.md"
        Msg = "docs(notes): add Node.js event loop architecture breakdown"
        Content = @"
# 🔄 Node.js Event Loop Architecture

Understanding libuv phases and execution order in Node.js runtime.

## Event Loop Phases
1. **Timers**: Executes callbacks scheduled by setTimeout() and setInterval().
2. **Pending Callbacks**: Executes I/O callbacks deferred to the next loop iteration.
3. **Idle, Prepare**: Internal libuv operations.
4. **Poll**: Retrieves new I/O events; executes I/O related callbacks.
5. **Check**: Executes setImmediate() callbacks.
6. **Close Callbacks**: Executes close events (e.g. socket.on('close')).

> process.nextTick() and microtasks (Promise.then) run immediately between each phase!
