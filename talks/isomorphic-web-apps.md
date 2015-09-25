# Building Isomorphic Web Applications with React

By, Elyse Kolker Gordon

## Why?

- SEO Crawlers
- Performance
- "Write once. Run anywhere."
- Dev Benefits

## What

- Shared routes on client and server
  - Also shared js code, with identiical interface mushing
- Showing different pages and (markup) layout to bots vs humans
  - Is that a good idea?

## How

- Templates and abstractions allow the VirtualDOM to pre-compute the final form for the DOM
  - Because the actual paint is costly, and re-paints even more so.
  - Isomorphic (shared codebases) between client and server is mostly to reduce code

## Pros and Cons

- Pros
  - Serve better responses to bots and crawlers
  - Good initial load times
- Cons
  - Server render performance
  - Bootstrapping each environment has hidden costs

## Links

- [Demo application](https://github.com/elyseko/iso-react-demo)
