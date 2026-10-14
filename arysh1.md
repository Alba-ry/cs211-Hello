- **NextID:** arysh1
- **Major:** Computer Science
- **Question that I chose from the memoization excerice:** Count ways to reach the n’th stair
- **Link to the question article:** https://www.geeksforgeeks.org/problems/count-ways-to-reach-the-nth-stair-1587115620/1
- **My solution:**

\```
// Using memoization to solve the stairs excerice
int countWays(int n, int* array) {
    // code here
    if (n == 0 || n == 1)
    {
        return 1;
    }
    
    if(n==2)
    {
        return 2;
    }
    
    if (array[n] != -1)
    {
        return array[n];
    }
    
    return array[n] = countWays(n-1, array) + countWays(n-2, array);
    
}

static int ways(int n)
{
    int array[n+1];
    for (int i = 0; i < n+1; i++)
    {
        array[i] = -1;
    }
    return countWays(n, array);
}
\```
