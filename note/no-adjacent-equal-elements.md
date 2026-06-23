# No Adjacent Equal Elements

## Problem

Given a multiset of elements, determine whether it is possible to rearrange them so that no two adjacent elements are equal.

## Condition

Let

$$
n = \sum_i c_i
$$

and

$$
mx = \max_i c_i.
$$

A valid rearrangement exists iff

$$
mx \le \left\lceil \frac{n}{2} \right\rceil.
$$

Equivalently,

$$
2mx \le n + 1.
$$

## Proof

Place all occurrences of the most frequent element first:

```text
X _ X _ X _ ... _ X
```

There are

$$
mx - 1
$$

gaps.

The number of remaining elements is

$$
n - mx.
$$

All gaps must contain at least one element, so

$$
n - mx \ge mx - 1.
$$

Rearranging,

$$
2mx \le n + 1.
$$

Conversely, if this condition holds, every gap can be filled, so a valid arrangement exists.

## Complexity

$$
O(n)
$$

(after counting frequencies)

## Typical Signals

- Rearranging characters
- Rearranging colors
- Rearranging values
- No adjacent equal elements
- Constructive greedy problems involving frequencies

## Key Idea

```text
X _ X _ X _ X
```

If the number of gaps exceeds the number of remaining elements, some gap remains empty and two `X`s become adjacent.

## Tags

- Greedy
- Pigeonhole Principle
- Frequency Counting
- Constructive
