
# flon messages

Messages are sent from one flon execution node to another.

Messages are sent from one flon worker to the other or from a flon client to a flon worker.

There are two kind of messages: orders and notifications. Orders are unconjugated verbs like "apply" or "cancel". Notifications are verbs in the past participle form: "terminated" or "error_intercepted".

Orders are meant to be followed by some execution, while notifications are followed by (indirect) execution only when there are trackers watching them.


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


## _thought dump_

* Join cancel and kill into a single kill + level message (like nix signals)

