# Everything old is new again: Quoted Domain Specific Languages

By, Philip Wadler

## Implementing SQL in a host language

- Using quotation to represent code as data
  - Antiquotation is just used to substitute dynamically

## Quotations

- Closed: quotations of functions (`Exp<A -> B>`)
- Open: functions of quotations (`Exp<A> -> Exp<B>`)

## Subformula Property

- We are able to only list the hypothesis and conclusion of a proof.
  - The middle bits aren't stricly needed. Useful sure, but not required for usage of the proof.
- You're able to use any features of the host language as long as the free variables or result are simplified without it.

## Normalization

- Lots of systems get DSL translation wrong (or really just inefficient)
  - Normalization, even with it's minimal cost, is still highly valuable
