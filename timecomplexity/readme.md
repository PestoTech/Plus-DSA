# Time Complexity 


# Benchmarks for assignment
 - All the solution should have the optimized solutions
 - If possible an explanation for the provided optimized solutions should also be given

##### Questions

1) Guess the time complexity for the following 
    ```
        int a = 0, b = 0;    
        for (i = 0; i < N; i++) {
            a = a + rand();  
        }
        for (j = 0; j < M; j++) {
            b = b + rand();
        }
     Assume that rand() is O(1) time, O(1) space function.
     ```
     
2) What is the time, space complexity of following 
    ```
    int a = 0, b = 0;    
    for (i = 0; i < N; i++) {
        for (j = 0; j < N; j++) {
            a = a + j;
        }
    }
    for (k = 0; k < N; k++) {
        b = b + k;
    }
    ```
3) What is the time complexity of the following code :
   ```
    int a = 0;
    for (i = 0; i < N; i++) {
        for (j = N; j > i; j--) {
            a = a + i + j;
        }
    }
    ```
    
4) What is the time complexity of the following code :
    ```
        int a = 0, i = N;
        while (i > 0) {
            a += i;
            i /= 2;
        }
    ```
5) What is time complexity of following code :
    ```
        int count = 0;
        for (int i = N; i > 0; i /= 2) {
            for (int j = 0; j < i; j++) {
                count += 1;
            }
        }
    ```

6) What is the time complexity of the following code :
    ```
    int i, j, k = 0;
    for (i  = n/2; i <= n; i++) {
        for (j = 2; j <= n; j = j * 2) {
            k = k + n/2;
        }
    }
    ```
7) In the following C++ function, let n >= m.
   ```    
            int gcd(int n, int m) {
            if (n%m ==0) return m;
            if (n < m) swap(n, m);
            while (m > 0) {
                n = n%m;
                swap(n, m);
            }
            return n;
    }
    What is the time complexity of the above function assuming n > m?
  
8) What is the worst case time complexity of the following code :
    ```
    /* 
     * V is sorted 
     * V.size() = N
     * The function is initially called as searchNumOccurrence(V, k, 0, N-1)
     */
    int searchNumOccurrence(vector<int> &V, int k, int start, int end) {
        if (start > end) return 0;
        int mid = (start + end) / 2;
        if (V[mid] < k) return searchNumOccurrence(V, k, mid + 1, end);
        if (V[mid] > k) return searchNumOccurrence(V, k, start, mid - 1);
        return searchNumOccurrence(V, k, start, mid - 1) + 1 + searchNumOccurrence(V, k, mid + 1, end);
    }
    ```
9) What is the worst case time complexity of the following code:
    ```
    int findMinPath(vector<vector<int> > &V, int r, int c) {
      int R = V.size();
      int C = V[0].size();
      if (r >= R || c >= C) return 100000000; // Infinity
      if (r == R - 1 && c == C - 1) return 0;
      return V[r][c] + min(findMinPath(V, r + 1, c), findMinPath(V, r, c + 1));
    }
    Assume R = V.size() and C = V[0].size()
    ```
    
10) What is the worst case time complexity of the following code:
   ```
     int memo[101][101];
     int findMinPath(vector<vector<int> >& V, int r, int c) {
      int R = V.size();
      int C = V[0].size();
      if (r >= R || c >= C) return 100000000; // Infinity
      if (r == R - 1 && c == C - 1) return 0;
      if (memo[r][c] != -1) return memo[r][c];
      memo[r][c] =  V[r][c] + min(findMinPath(V, r + 1, c), findMinPath(V, r, c + 1));
      return memo[r][c];
    }
    
    Callsite : 
    memset(memo, -1, sizeof(memo));
    findMinPath(V, 0, 0);
    Assume R = V.size() and C = V[0].size() and V has positive elements
  ```
 
11) What is the time complexity of the following code :
    ```
        int a = 0, i = N;
        while (i > 0) {
            a += i;
            i /= 2;
        }
    ```
12) What is time complexity of following code :
    ```
        int count = 0;
        for (int i = N; i > 0; i /= 2) {
            for (int j = 0; j < i; j++) {
                count += 1;
            }
        }
    ```
    
13) What is the time complexity of the following code :
    ```
    int i, j, k = 0;
    for (i  = n/2; i <= n; i++) {
        for (j = 2; j <= n; j = j * 2) {
            k = k + n/2;
        }
    }
    ```
    
14) In the following C++ function, let n >= m.
    ```
    int gcd(int n, int m) {
            if (n%m ==0) return m;
            if (n < m) swap(n, m);
            while (m > 0) {
                n = n%m;
                swap(n, m);
            }
            return n;
    }
   
   What is the time complexity of the above function assuming n > m?
  ```
