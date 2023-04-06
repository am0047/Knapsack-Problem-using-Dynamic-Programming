# Knapsack-Problem-using-Dynamic-Programming
This is a Python program to solve the 0-1 knapsack problem using dynamic programming with bottom-up approach.

Problem Description
In the 0-1 knapsack problem, we are given a set of n items. For each item i, it has a value v(i) and a weight w(i) where 1 <= i <= n. We are given a maximum weight W. The problem is to find a collection of items such that the total weight does not exceed W and the total value is maximized. A collection of items means a subset of the set of all items. Thus, an item can either be included just once or not included.

Problem Solution
1. The function knapsack is defined.
2. It takes three arguments: two lists value and weight; and a number capacity.
3. It returns the maximum value of items that doesn’t exceed capacity in weight.
4. The function creates a table m where m[i][w] will store the maximum value that can be attained with a maximum capacity of w and using only the first i items.
5. First m[0][w] is initialized to 0 for all 0 <= w <= capacity. 6. For item i, if weight[i] > w, then m[i][w] = m[i – 1][w].
7. If weight[i] <= w, then m[i][w] = (m[i - 1][w - weight[i]] + value[i]) or m[i][w] = m[i - 1][w], whichever is larger. 8. The table is filled from top to bottom row. 9. m[n][capacity] is returned.

Program Explanation
1. The user is prompted to enter the number of items n.
2. The user is then asked to enter n values and n weights.
3. A None value is added at the beginning of the lists so that value[i] and weight[i] correspond to the ith item where the items are numbered 1, 2, …, n.
4. The function knapsack is called to get the maximum value.
5. The result is then displayed.
