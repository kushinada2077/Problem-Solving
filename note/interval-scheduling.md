# Interval Scheduling (区間スケジューリング)

## Problem

Given $N$ intervals $[l_i, r_i]$, determine whether it is possible to select $K$ pairwise non-overlapping intervals.

## Algorithm

1. Let $A$ be an empty set of selected intervals.
2. Sort all intervals by increasing $r_i$.
3. Process the intervals in order:
    - Let $[l_j, r_j]$ be the last selected interval.
    - Select $[l_i, r_i]$ if $r_j < l_i$.
4. Check whether $|A| \ge K$.

## Complexity

$O(N \log N)$

## Example

- https://atcoder.jp/contests/abc463/tasks/abc463_d

## Tags

- Greedy
- Sorting
