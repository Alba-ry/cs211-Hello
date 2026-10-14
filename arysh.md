- **NetID:** arysh
- **Major:** Computer Science
- **Question that I chose from the memoization exercise:** Ways to Reach the n'th Stair
- **Link to the question article:** https://www.geeksforgeeks.org/dsa/count-ways-reach-nth-stair/
- **My solution:**
```
int countWays(int n) {
   // Base cases
    if (n == 1 || n == 0) { 
        return n;
    }
    
    // Recursively check each step and the ways you can reach that step
    return counttWays(n-1) + countWays(n-2);
    
    // Memoization method
    
  int memo[n];
    for (int i = 0; i < n; i++) {
        memo[n] = -1
    }
    memo[0] = 0;
    memo[1] = 1;
    
   if(n == 1 || n == 0) {
        return memo[n];
    }
    else {
        if(memo[n] > -1) {
            return memo[n];
        }
        else {
            memo[n] = countWays(n-1) + countWays(n-2);
        }
    }
    
    // NOTE: Should've instead create a helper function to do memoization
}
```
