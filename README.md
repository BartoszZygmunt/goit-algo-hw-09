# Cash Register Change Algorithms

This project includes two algorithms to determine the best way to give change to a customer using a set of coin denominations [50, 25, 10, 5, 2, 1]:

1. **Greedy Algorithm**: `find_coins_greedy`
2. **Dynamic Programming Algorithm**: `find_min_coins`

## find_coins_greedy

The greedy algorithm takes an amount and returns a dictionary with the number of coins of each denomination used to make up the amount. It always chooses the largest available coin denominations first.

### Example

```python
find_coins_greedy(113)  # Output: {50: 2, 10: 1, 2: 1, 1: 1}

```

#Greedy Algorithm
Advantages: Fast and efficient for large sums, simple to implement.
Disadvantages: Does not always provide the minimum number of coins, especially if the coin denominations are non-standard.

#Dynamic Programming Algorithm
Advantages: Guarantees the minimum number of coins.
Disadvantages: Can be slow for very large amounts due to higher time complexity, requires more memory.

#Handling Large Amounts
#Greedy Algorithm
The greedy algorithm works quickly for large sums as it processes the amount linearly by choosing the largest available denominations. It is efficient in terms of time, but may not always be optimal in terms of the number of coins used.

#Dynamic Programming Algorithm
The dynamic programming algorithm ensures an optimal solution but its (n⋅amount) complexity means the execution time can be significant for very large amounts. Additionally, it requires more memory to store intermediate results.

#Conclusion
For a cash register system, the greedy algorithm is generally faster and simpler, making it suitable for real-time applications. However, the dynamic programming approach should be used when the absolute minimum number of coins is required.
