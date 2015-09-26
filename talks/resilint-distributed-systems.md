# Architectural Patterns of Resilient Distributed Systems

By, Ines Sombra

## Literature

- Harvest & Yield Model
- Cook & Rasmussen Model
- Borrill's Model

## Fault Tolerance

- Netflix
  - (Web) APIs is inherently more vulnerable than any other system
    - Implemented client libraries with exp backoff, semaphores, harsh timeouts
    - Exceptions cause app to shed load until things are stable
- Google
  - [The Chubby Lock Service](papers/The Chubby lock service for loosely-coupled distributed systems.pdf)
    - Built a service rather than a library. Also restricted user behavior

## Patterns

- Redundancies are key
- Operations matter
- Not all complexity is bad
- Leverage best practices
  - re-examine the way we prototype systems

## Questions

- Designing
 - Are we favoring *harvest* or *yield*?
- Operability
 - Would I want to be on call for this?
- Unk-Unk
 - Have we done everything we can?

## Links

- [Her Notes](https://github.com/Randommood/Strangeloop2015)
