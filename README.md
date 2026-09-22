# LeetCode 247 - Strobogrammatic Number II

## Problem

Given an integer `n`, return all the strobogrammatic numbers that have exactly `n` digits.

A strobogrammatic number looks the same when rotated 180 degrees.

The valid digit pairs are:

```text
0 -> 0
1 -> 1
6 -> 9
8 -> 8
9 -> 6
```

## Example

### Input

```text
n = 2
```

### Output

```text
["11","69","88","96"]
```

## Approach

Build the number from the outside toward the center.

For each pair of positions, use one of these valid pairs:

```text
00
11
69
88
96
```

For the first position, `0` cannot be used because the result must contain exactly `n` digits.

For an odd length, the middle digit can only be:

```text
0, 1, 8
```

## Algorithm

1. Handle the base cases for lengths `0` and `1`.
2. Recursively build the inner part of the number.
3. Add each valid strobogrammatic pair around the inner part.
4. Do not place `0` at the outermost position.
5. Continue until the required length is reached.
6. Return all generated numbers.

## Complexity

* Time Complexity: `O(5^(n/2))`
* Space Complexity: `O(5^(n/2))`

The space complexity includes the generated output.

## Language

Python

## LeetCode

Problem: 247 - Strobogrammatic Number II

## Author

**T.Nandhini**
