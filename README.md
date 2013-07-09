
# flon

Flon is an evolution of [ruote](http://ruote.rubyforge.org).

It builds on the OpenWFE and then ruote projects.

Flon is a distributed interpreter for a language meant to describe "workflows".


## workflow

By "workflow", we do not mean:

* programming workflow
* digital photography workflow
* entity lifecycle

We mean:

* description and coordination of the work of one or more participants

We totally understand that stashing a few state machines on entities may suffice to describe the workflows around those entities and that flon and its ilk is about shooting oneself in the foot and growing long lasting monsters that are hard to revert.


## concepts

* flon is meant to work as a web of one or more flon workers
* there is no preferred language for the implementation of flon workers
* the focus is on protocol and interfaces

* flon builds heavily on HTTP and JSON

* a flon worker can assume two roles, execution worker or participant worker
* a flon execution worker interprets and executes messages
* a flon participant worker interprets and executes messages about participants, it hosts the participant code or interfaces with the real, remote participant


## documentation

* [glossary](doc/glossary.md)
* [flon worker](doc/worker.md)
* [messages](doc/messages.md) exchanged between flon execution nodes
* [testing](doc/testing.md) testing flon


## license

MIT (see LICENSE.txt)

