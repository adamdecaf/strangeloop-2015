# Strange loops: reasoning about knots with computers and powerful notation

By, Kay Ye

## Knots 101

- Connected single thread wrapped and folded onto itself

## Alexander Briggs notation

- Stevedore
  - First: Count the number of crossings, but that's not a unique representation.
    - Too much compression
  - `W` notation
    - Talk about specific crossings with a direction
      - `1 8`, `2 7`, etc
        - Each crossing has an under and over string. So we've duplicated
      - Simplify to `8 6 10 2 12 4` (for an alternating knots)

## Enumerating with Dowker

- Any pairing of `(n, n+1)` can be untwisted and ignored as a knot.
- However, this is harder than it looks.
  - Two strategies: tear down, and build up

## How did he do it?

- Being able to represent knots as continued fractions -> rational numbers makes it easier by hand
- Dowker notation never has this advantage

## Takeaways

- Axes of notation
  - Easy for humans to read? Machines?
  - Minimal?
  - Is the notation bijective? Or are there repsentations or objects which don't have a mapping.
- Program equivalence <-> Knot equivalence
