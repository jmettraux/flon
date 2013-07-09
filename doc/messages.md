
# flon messages

Messages are sent from one flon execution node to another.

Messages are sent from one flon worker to the other or from a flon client to a flon worker.


## messages by name

### "apply"
### "reply"

### "dispatch"
### "dispatch_cancel"
### "dispatch_kill"

### "cancel"
### "kill"

### "error_intercepted"
### "terminated"
### "ceased"


## thought dump

* Join cancel and kill into a single kill + level message (like nix signals)

