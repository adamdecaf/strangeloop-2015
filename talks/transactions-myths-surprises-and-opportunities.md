# Transactions: myths, surprises and opportunities

By, Martin Kleppmann

## Read Committed

- Read Skew (multi-transaction reads) can mess up concurrent reads.
  - Often from other async processes going on (analytics, or backups)

## Write Skew

- Pattern:
 - read something
 - make choice
 - write choice to db
- Happens when the write is commited the premise of the choice isn't true

## 2 Phase Locking

- Shared lock on the entire table
  - HStore: In vaultDB (Literally execute everything in a serial order.)
    - Only works if **every** transaction is fast
  - SSI: Detect conflicts and abort
    - "Locks" in 2 Phase Locking, but records incoming writes and looks at the various conflicts with the predicate

## Distributed Systems

- How do we handle atomic broadcast?
  - (Atomic Broadcast == Consensus)?
- Cross application rollback protocols?
  - Cross constraint violation checking would also be needed
    - Or just apologize later (give a discount code, etc)
- Causal relationships are almost always lost between microservices
  - Active research on this.

## Papers

- [Attiya, Ellem, and Morrison 2015](papers/Limitations of Highly-Available Eventually-Consistent Data Stores.pdf)
