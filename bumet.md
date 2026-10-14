# Profile: Bermet Umetalieva

- **NetID:** bumet
- **Major:** Computer Science
- **Question that I chose from the memoization exercise:** Climbing stairs to reach the top
- **Link to the question article:** https://www.geeksforgeeks.org/dsa/count-ways-reach-nth-stair/
- **My solution:**
```c
int countWaysRec(int n, int dp[]) {
    if (n == 0 || n == 1) {
        return 1;
    }

    if (dp[n] != -1) {
        return dp[n];
    }

    dp[n] = countWaysRec(n - 1, dp)
          + countWaysRec(n - 2, dp);

    return dp[n];
}

int countWays(int n) {
    if (n == 0 || n == 1) {
        return 1;
    }
    int dp[41];
    
    for (int i = 0; i <= n; i++) {
        dp[i] = -1;
    }
    return countWaysRec(n, dp);
}
