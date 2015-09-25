# Building Scalable Stateful Services

By, Caitie McCaffrey

## History

- We've pushed state to single sources of truth.
  - Out apps still have actual state that matters
  - Or we shard out the data across many machines to lessen total failure

## Benefits

- You have data locality with request handling. (Low latency)
- Gives you stronger than non `C` for your `AP` systems, given your DB can handle node failures
  - You can also lose uncommitted local writes to a sicky node that didn't reach / commit to the underlying DB.

## Routing Logic / Load Balancing

- Without back pressure per machine machines can be overrun.
  - Or introduce a load balancer in front of of the nodes for initial discovery.
- If any node can at least proxy or redirect to other nodes:
  - Then you have cluster membership problems
  - Really needs to be dynamic, so you don't have to bring down the entire cluster.

## Dynamic membership

- Gossip protocols vs consensus systems
  - Available vs Consistent

## In the real world

- [Scuba](papers/Scuba.pdf): In memory database. distributed.
  - random fan out writes to signle node, read from all nodes.
- [Ringpop](https://github.com/uber/ringpop-node): Application layer sharding
  - Swim gossip protocol + Consistent hashing
- [Orleans](https://github.com/dotnet/orleans): Runtime and programming model that extends the actor model
  - Gossip protocol + consistent hashing + distributed hash table
  - Consistent hashing to find which node contains that part of the distributed hash table

## Caution

- Unbound data structures are killers
- Memory management: long gc pauses will show nodes as dead
  - Lots of long lived objects
- Reloading state
  - first connection (what do you need at a minimum)
  - recover from crashes (pre-warm?)
  - deployments
