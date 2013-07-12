
# flon execution nodes

(NTS: Is that a good designation? A "node" is often used to designate a host in a network, it could conflict with _flon worker_)

A node is a live piece of flon execution.

Abbreviated to FEN or fen.

In ruote an "execution node" was called a "flow expression". With flon, we want to move way from this designation. Ruote has an emphasis on executing messages on independent expressions, while flon deals with executions instead of excution nodes.


## flon execution node id (fenid)

TODO: explain exid vs id, and id { nodeid, subid }


## when stored

A node, when stored, is a JSON document.

```javascript
// (using javascript notation)
{
  exid: "",
  id: { nodeid: "x", subid: "y" },
  tree: [ ... ],
  applied_workitem: { ... },
  on: {
    reply: [],
    cancel: [],
    error: []
  }
}
```

## _thought dump_

* have primitives like reply_to_parent or remove_self, spec them, build upon them

