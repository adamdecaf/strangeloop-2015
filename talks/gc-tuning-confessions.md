# GC Tuning Confessions Of A Performance Engineer

By, Monica Beckwith

## Performance Engineering

- SLA agreements, throughput, latency, RTT & worst-case
  - Only possible if you capture the metrics
    - min, max, median, 95%
  - [GC Histo](https://java.net/projects/gchisto) and JfreeCharts

## Types of GC's

- Always a tradeoff between throughput and latency
- G1 can avoid full gc's, CMS cannot

## Promotion failures

- Promotion failures in CMS: Unable to fit promoted objects into OldGen
  - Causes: High marking threshold, heap is too small, high app mutation rate

## G1

- Regionalized Heap
  - Generations are not continuous
  - Young collections are moved to a central spot, survivors are also moved around
- Regions which are entirely garbage can be freed without a pause
- Promotion failures
  - G1 couldn't find regions to use
- Evacuation failures
  - full gc is required
- Tips
  - Set a pause time and heap limits
    - Try increasing your heap next
    - Then adjust marking threshold

## G1 GC logs

- Any libraries to parse them? Or report directly to graphite/etc
- GC overhead: throughput
- GC elapsed time: latency

## Summary

- All GC's (ParallelOld, CMS, G1) sweep the entire Young gen
- Promotion is expensive
- CMS sweeps all objects for things to free, G1 prioritizes garbage regions first.
  - Garbage regions can be freeded without pauses
