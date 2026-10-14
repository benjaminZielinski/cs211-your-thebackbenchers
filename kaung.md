# Profile: [Kyaw Htut Aung]

- **NetID:** [kaung]
- **Major:** [Computer Science]
- **Question that I chose from the memoization exercise:** [Count Ways with 3 Moves]
- **Link to the question article:** [(https://www.geeksforgeeks.org/problems/count-number-of-hops-1587115620/1)]
- **My solution:**

\```

P
class Solution {
  public:
    int countWays(int n) {
        // ways to reach steps
        int a = 1;
        int b = 1;
        int c = 3;
        
        for (int i = 3; i <= n; i++) {
            int next = a + b + c;
            
            // keep the latest three counts
            a = b;
            b = c;
            c = next;
        }
        
        // c has number of total ways
        return c;
    }
};


\```
