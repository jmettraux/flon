
# flon worker

A flon worker drives the execution of flon workflow executions.

## worker "behaviours"

### upon receiving a message

```
  - receive message
  - fetch execution
    - if execution not found, queue message for the next cycle
  - execute
    - until no more [inner] messages
    - or until >= 500 ms
  - put execution
    - if fail then return
  - dispatch to participant if necessary
  - queue trackers for the next cycle
```

### upon receiving a cycle

```
  - if cycle's target hash != own map hash then request full cycle
  - read part
    - read list of flon workers
    - copy new trackers
    - copy messages if there is a copy of their execution locally
  - write part
    - put queued messages
    - put queued trackers
  - delete part
    - remove tracker notifications that have completed the cycle
    - remove messages if there is a copy of their execution locally
```

### message emission

When a flon worker emits a message to another flow worker.

```
  - identify executor
  - is executor in ring?
    - yes
      - post message to executor
        - if the post failes, queue message for the next cycle
    - no
      - queue message for the next cycle
```

### at each clock tick

Each flon worker has an integrated clock (is a clockworker?), at each tick, the list of time trackers (timers) is considered

```
  - for each time tracker
    - next timer unless due
    - if due, emit message and discard time tracker
```

