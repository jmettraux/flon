
# cycle

A cycle is a chain of communication between flon workers. It always follows the alphabetical order of the worker URIs.

It's used to circulate

- the list of flon workers (URIs)
- the list of trackers (time trackers and event trackers)
- pass messages whose intended executor is MIA

The ring is the list of flon worker URIs, it is ordered alphabetically, thus, there is a always a first worker and a last worker. Cycle messages are passed from the last worker to the first worker (else it wouldn't be a cycle).

## _thought dump_

* think about cycle speed and strategies to shorten cycle time
* would star delivery be better than cycle circulation? Cycle is nice to give worker the opportunity to consider cycled messages on their own, without other workers competing.

