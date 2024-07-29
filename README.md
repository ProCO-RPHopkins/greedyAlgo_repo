# Minimum Absolute Difference in an Array - Greedy Algorithm 1

## Problem Description

In an array of numbers find which two numbers are closest to each other. The "closeness" between two numbers is measured by how far apart they are, which is the "absolute difference." For example, given the numbers 3 and 7, their closeness is 4 because 7 is 4 units away from 3.

## Approach

1. Arranged numbers in order from smallest to largest.
2. Iterated through each pair of numbers that are next to each other to determine how far apart they are.
3. Kept track of smallest distance found while checking each pair.
4. After all pairs were checked, the smallest distance found was returned.

## Optimization

By first arranging the numbers in order, it is only necessary to check the pairs of numbers that are next to each other to find the closest pair. This makes it quicker because every number does not need to be compared with every other number.

## Marc's Cakewalk - Greedy Algorithm 2

## Problem Description (G-2)

Find the distance Marc will have to walk to burn off calories. The problem is to find the minimum distance Marc has to walk. Each cupcake has a calorie count, and Marc can eat them in any order he likes. However, the total distance is calculated by the formula: the sum of \(2^i \times \text{calories}[i]\), where \(i\) is the order in which he eats the cupcakes.

## Approach (G-2)

1. Arrange calorie counts in descending order.
2. Initialize total miles to zero.
3. Calculate miles for each cupcake using the formula \(2^i \times \text{calories}[i]\).
4. Add these miles to get the total distance Marc needs to walk.

## Optimization (G-2)

To minimize the total distance, Marc should eat the cupcakes with the highest calories first. Why? Because the power of two grows rapidly, so the largest calorie counts to be multiplied by the smallest powers of two. This is why sorting the calories in descending order is the optimal strategy.

## Example

Given calorie counts of [5, 10, 7]:

1. Sorted in descending order [10, 7, 5].
2. The total distance would be \(2^0 \times 10 + 2^1 \times 7 + 2^2 \times 5 = 10 + 14 + 20 = 44\).
