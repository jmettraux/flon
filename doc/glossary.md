
# flon glossary


### cycle

TODO

### execution

An instance of a flon workflow.

Was chosen over _process_, _job_ and _workflow instance_ (or even _task_). Process is heavily used when referring to operating system processes. Job too. Workflow instance is a bit long.

### execution work

The work done to enact the execution of a workflow.

Placed side by side with participant work.

### flon

1. From Latin _flumen_ (river).
2. The name of the project.
3. A web of flon workers

### flon worker

Independent flon execution and/or participant work unit.

See [worker.md](worker.md).

### flon execution

TODO

### flon execution node

(In ruote, this was called a _flow expression_)

TODO

### participant

TODO

### participant work

The work done by a flon worker to hand workitems forth and back to participants. Also comprises the work involved when handing cancellation workitems to participants.

Participant work can be thought as part of the execution work, but since it deals on the boundary of the execution, with participants, it is practical to label it separately.

### tracker

A pair condition + message. When the condition realizes the message is triggered.

There are two kinds of trackers, message trackers and time trackers.

Message trackers watch the in-worker activity and trigger whenever a message match the condition.

Timer trackers trigger whenever a given point in time is reached.

Message trackers let workflows observe themselves and each others. Time trackers are used to implement timers and timeouts.

### workflon

Contraction of _workflow_ and _flon_. Not yet used.

### workflow

Could be thought of as _routine_, _recipe_, _program_, _script_, _scenario_, ... Has indeed many definitions.

In the flon context, a workflow is a program conducted by a flon (understood as a web of flon workers) from start to end.

A workflow generally has a goal, be it transformation and/or circulation of data by/to participants.

### workflow definition

TODO

### workitem

TODO

