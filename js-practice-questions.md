# Problem statement 1

### Objective: 
You are given an array of integers, where each element represents the price of a stock on a particular day. Your task is to find the maximum profit that can be achieved by buying and selling the stock multiple times.

You can only buy stock if its price is less than the price on the next day. You can sell the stock at any subsequent day to maximize your profit. Just make sure to make a profit with each transaction.

### Input
The input is a single array of integers where each element represents the price of the stock on each day.

### Output
Print a single integer representing the maximum profit that can be achieved.

### Constraints

- 1 ≤ n ≤ 10^5
- 1 ≤ prices[i] ≤ 10^4 for 1 ≤ i ≤ n


### Example 1

**Input:**

```javascript
[7, 1, 5, 3, 6, 4]
```

**Output:**

```javascript
7
```

**Explanation:**

- Buy on day 2 (price = 1) and sell on day 3 (price = 5), profit = 5-1 = 4.
- Buy on day 4 (price = 3) and sell on day 5 (price = 6), profit = 6-3 = 3.
- Total profit = 4 + 3 = 7.

### Example 2

**Input:**

```javascript
[1, 2, 3, 4, 5]
```

**Output:**

```javascript
4
```

**Explanation:**

- Buy on day 1 (price = 1) and sell on day 5 (price = 5), profit = 5-1 = 4.
- Total profit = 4.

### Example 3

**Input:**

```javascript
[7, 6, 4, 3, 1]
```

**Output:**

```javascript
0
```

**Explanation:**

- No transaction is done, i.e., max profit = 0.

### Where to code?

To write code please open file `src\assessments\01\solution.js` or click [here](src\assessments\01\solution.js)
