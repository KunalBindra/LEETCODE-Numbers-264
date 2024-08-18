# LEETCODE-Numbers-264
Let's dry run the `nthUglyNumber` method for `n = 10`.

1. Initialize: `dp = [1, 0, 0, 0, 0, 0, 0, 0, 0, 0]`, `p2 = 0`, `p3 = 0`, `p5 = 0`.

2. Iteration 1 (`i = 1`):
   - `next2 = dp[0] * 2 = 2`
   - `next3 = dp[0] * 3 = 3`
   - `next5 = dp[0] * 5 = 5`
   - `dp[1] = min(2, 3, 5) = 2`
   - `dp = [1, 2, 0, 0, 0, 0, 0, 0, 0, 0]`
   - `p2` is incremented: `p2 = 1`

3. Iteration 2 (`i = 2`):
   - `next2 = dp[1] * 2 = 4`
   - `next3 = dp[0] * 3 = 3`
   - `next5 = dp[0] * 5 = 5`
   - `dp[2] = min(4, 3, 5) = 3`
   - `dp = [1, 2, 3, 0, 0, 0, 0, 0, 0, 0]`
   - `p3` is incremented: `p3 = 1`

4. Iteration 3 (`i = 3`):
   - `next2 = dp[1] * 2 = 4`
   - `next3 = dp[1] * 3 = 6`
   - `next5 = dp[0] * 5 = 5`
   - `dp[3] = min(4, 6, 5) = 4`
   - `dp = [1, 2, 3, 4, 0, 0, 0, 0, 0, 0]`
   - `p2` is incremented: `p2 = 2`

5. Iteration 4 (`i = 4`):
   - `next2 = dp[2] * 2 = 6`
   - `next3 = dp[1] * 3 = 6`
   - `next5 = dp[0] * 5 = 5`
   - `dp[4] = min(6, 6, 5) = 5`
   - `dp = [1, 2, 3, 4, 5, 0, 0, 0, 0, 0]`
   - `p5` is incremented: `p5 = 1`

6. Iteration 5 (`i = 5`):
   - `next2 = dp[2] * 2 = 6`
   - `next3 = dp[1] * 3 = 6`
   - `next5 = dp[1] * 5 = 10`
   - `dp[5] = min(6, 6, 10) = 6`
   - `dp = [1, 2, 3, 4, 5, 6, 0, 0, 0, 0]`
   - `p2` and `p3` are incremented: `p2 = 3`, `p3 = 2`

7. Iteration 6 (`i = 6`):
   - `next2 = dp[3] * 2 = 8`
   - `next3 = dp[2] * 3 = 9`
   - `next5 = dp[1] * 5 = 10`
   - `dp[6] = min(8, 9, 10) = 8`
   - `dp = [1, 2, 3, 4, 5, 6, 8, 0, 0, 0]`
   - `p2` is incremented: `p2 = 4`

8. Iteration 7 (`i = 7`):
   - `next2 = dp[4] * 2 = 10`
   - `next3 = dp[2] * 3 = 9`
   - `next5 = dp[2] * 5 = 15`
   - `dp[7] = min(10, 9, 15) = 9`
   - `dp = [1, 2, 3, 4, 5, 6, 8, 9, 0, 0]`
   - `p3` is incremented: `p3 = 3`

9. Iteration 8 (`i = 8`):
   - `next2 = dp[4] * 2 = 10`
   - `next3 = dp[3] * 3 = 12`
   - `next5 = dp[2] * 5 = 15`
   - `dp[8] = min(10, 12, 15) = 10`
   - `dp = [1, 2, 3, 4, 5, 6, 8, 9, 10, 0]`
   - `p2` and `p5` are incremented: `p2 = 5`, `p5 = 2`

10. Iteration 9 (`i = 9`):
    - `next2 = dp[5] * 2 = 12`
    - `next3 = dp[3] * 3 = 12`
    - `next5 = dp[2] * 5 = 15`
    - `dp[9] = min(12, 12, 15) = 12`
    - `dp = [1, 2, 3, 4, 5, 6, 8, 9, 10, 12]`
    - `p2` and `p3` are incremented: `p2 = 6`, `p3 = 4`

The final result for `n = 10` is `dp[9] = 12`.
