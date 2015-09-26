# Distributed, Eventually Consistent Computations

By, Christopher Meiklejohn ([@cmeik](https://twitter.com/cmeik))

## Distributed Synchronization

- Internet of Things devices
  - Low power, limited memory, and connectivity
- Mobile Gaming
  - Limited connectivity, multiple concurrent games per user (shared accounts)

## Zero Synchronization

- Is it possible to write coordination free systems without concurrent anomalies?
- However, without it computer and systems can't do much.

## Physical Time

- Unavoidable, but difficult because of network latency, mutable state, or nondeterminism.

## Weak Synchronization

- Strong Eventual Consistency
  - Eventual replica-to-replica communication
  - Order insensitive (commutative)
  - Duplicate insensitive (idempotent)

## Programming Strong Eventual Consistency

- Need the ability to model non-monotonic operations monotoniacally.
  - How? (CRDT's)
- We need to maintain composition between values and models

## Links

- CRDT Implementations
- [Lattice Processing (Lasp)](http://lasp-lang.org)
- [Lasp: A Language for Distributed, Coordination-Free Programming](http://christophermeiklejohn.com/publications/ppdp-2015-preprint.pdf)
- Inflations vs Monotoniacity (blog post)
- Selective Hearing (Epidemic broadcast based runtime)
- [CRDT Paper](papers/Incremental Stream Processing using Computational Conflict-free Replicated Data Types.pdf)
- [CRDTs: Consistency without concurrency control](http://arxiv.org/pdf/0907.0929v1.pdf)
