# Dynamic Programming

## Basic introduction:

<b> Note: </b>
- If you have knowledge about definitions and what basic DP means then you can skip this part
- If you specifically need a youtube video to explain you can find it at the end of this part

A very simple way of imagining is that you want to optimise your recursive approach. ( A practical definition ).
A formal definition will be that you want to break your problem into subproblems and then use their answer to build your overall answer.

If you think you have never seen DP then you are wrong !!

Some basic problems that use dp and you probably have seen before:

```
Fibonacci sequence:

	Basic recursive definition a[n]=a[n-1]+a[n-2];

	fib[N];
	Int fibo(int n){
		if(n<0)return 0;
		if(fib[n]!=-1)return fib[n];
		fib[n]=fibo(n-1)+fibo(n-2);
		Return fib[n];
	}
	memset(fib,-1,sizeof(fib))
	fib[0]=fib[1]=1;

```
Here one can observe that even though it is a recursive solution it still covers only the size N . Since you can never revisit a state because you saved it for future use. <br>

Similar recursive definitions can be easily solved with dp. <br>

<b> Let us observe the time complexity here. </b>
All this code basically does is find you the fib[x] by filling up the array fib. One index is never revisited hence the worst case will be that you visit the whole array. Hence time and space complexity are both O(n).


Take some time to analyse this. If you are fine with this let's move on.



## Types of DP:

This basically refers to in what way you want to visit your states and fill your dp array.

There are 2 main approaches.

1. Bottom up approach:
2. Top down approach.

A very naive explanation will be that in the bottom up approach we fill the array using loops and start from the base case while in top down we start from the required state and move on to the base case using recursion.

Let us look back to our fibonacci example.

Try to observe that to get fib[n] we call the function fibo(n) and then find our answer moving down in recursion to hit base case zero or one.

Now let us see another approach.
```
	int fib[N];

	fib[0]=fib[1]=1;
	for(int i=2;i<N;i++){
		fib[i]=fib[i-1]+fib[i-2];
	}
```
Here we observe that now we actually start from our base case and then move upwards.

There is no difference or preference in any style. One can use whichever he/she is comfortable with. For interview purposes it is advised you try to grasp both techniques.



## Analysing the states of problem.

A very essential rule to solve any DP problem is to recognize what are the states that your answer depends on. Like in the fibonacci case the state only depends on only one parameter. That is an example of 1 dimensional DP or 1D DP.

Now we will take another example:

```
Binomial coefficient nCr which equates to (n!)/((r!)(n-r)!)
Has a recursive property 
C(n, k) = C(n-1, k-1) + C(n-1, k)
With base conditions as:   C(n, 0) = C(n, n) = 1
Now here one can observe that a particular state depends on two parameters n and k.
Hence it is an example of 2 dimensional DP or 2-D DP.

Code for bottom up approach :
(source: https://www.geeksforgeeks.org/binomial-coefficient-dp-9/) 
int binomialCoeff(int n, int k)
{
    int C[n + 1][k + 1];
    int i, j;
 
    // Caculate value of Binomial Coefficient
    // in bottom up manner
    for (i = 0; i <= n; i++)
    {
        for (j = 0; j <= min(i, k); j++)
        {
            // Base Cases
            if (j == 0 || j == i)
                C[i][j] = 1;
 
            // Calculate value using previously
            // stored values
            else
                C[i][j] = C[i - 1][j - 1] +
                          C[i - 1][j];
        }
    }
 
    return C[n][k];
}

```
You can also refer to the top down approach mentioned in the source.
Here we had to make a 2 dimensional array and fill up that space.
Time and space complexity O(n * k).

Now we end our discussion and move on to practice.

## Summary:

<b>Simple steps to solve a DP problem are:</b>
- First identify if it is a DP problem i.e can it be broken into subproblems and then use them to form answers.
- Try to understand the states involved and then on what parameters will that state be dependent on.
- Try to find the relation between different states and how to transit between them.
- Choose an approach bottom up or top down.



## Resources :
[A nice youtube video to explain this.](https://www.youtube.com/watch?v=vYquumk4nWw)




## Very basic questions:

<b>1D DP:</b>

1. [Tiling problem](https://www.geeksforgeeks.org/tiling-problem/)
2. [Subset sum](https://www.geeksforgeeks.org/subset-sum-divisible-m/)
3. [Painting fence](https://www.geeksforgeeks.org/painting-fence-algorithm/)
4. [Climbing stairs](https://leetcode.com/problems/climbing-stairs/)
5. [House robber](https://leetcode.com/problems/house-robber/)

<b>2D DP:</b>

1. [Binomial coefficient](https://www.geeksforgeeks.org/binomial-coefficient-dp-9/)
2. [Coin change problem](https://www.geeksforgeeks.org/coin-change-dp-7/) 
3. [Finding Minimum-Cost Path in a 2-D Matrix](https://www.geeksforgeeks.org/min-cost-path-dp-6/)
4. [Rod Cutting](https://www.geeksforgeeks.org/cutting-a-rod-dp-13/)

<b> Finding the number of ways to reach from a starting position to an ending position travelling in specified directions only and other interesting problems in</b> [hackerearth](https://www.hackerearth.com/practice/algorithms/dynamic-programming/2-dimensional/tutorial/)



<b>The above problems are classic and one should definitely solve them once.</b>


## Some more classic problems:

1. [Longest common subsequence (LCS)](https://www.geeksforgeeks.org/dynamic-programming-set-4-longest-common-subsequence/)
2. [Longest increasing subsequence (LIS)](https://www.geeksforgeeks.org/longest-increasing-subsequence-dp-3/)
3. [Edit Distance:](https://www.geeksforgeeks.org/edit-distance-dp-5/ )
4. [Knapsack](https://www.geeksforgeeks.org/0-1-knapsack-problem-dp-10/)
5. [Matrix Chain Multiplication](https://www.geeksforgeeks.org/matrix-chain-multiplication-dp-8/)
6. [Longest path in matrix](https://www.geeksforgeeks.org/find-the-longest-path-in-a-matrix-with-given-constraints/ )
7. [Series of stock problems](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-transaction-fee/discuss/108870/Most-consistent-ways-of-dealing-with-the-series-of-stock-problems)

## Practice for Dynamic Programming:

There is no end to DP !!
DP can be combined with trees, graphs, bitmasking, strings, etc.

For practice I would suggest try to increase your level by doing easy -> medium -> hard question.
Many questions are there to practice on leetcode, hackerearth ( my fav sites)
- [Leetcode](https://leetcode.com/tag/dynamic-programming/)
- [hackerearth 1D-DP](https://www.hackerearth.com/practice/algorithms/dynamic-programming/introduction-to-dynamic-programming-1/practice-problems/) 
- [hackerearth 2D-DP](https://www.hackerearth.com/practice/algorithms/dynamic-programming/2-dimensional/practice-problems/)
- [Atcoder DP](https://atcoder.jp/contests/dp/tasks)

Some of the important questions I will add here ( mostly hard category )

For easy questions just sit and read GFG question list. DO not waste too much time on easy questions.

<b>Best of luck for you preparation !! </b>

## Hard problems

Try these questions after you have a firm grasp of DP.


1. [Unique Paths](https://leetcode.com/problems/unique-paths/)
2. [Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
3. [Longest Valid Parenthesis](https://leetcode.com/problems/longest-valid-parentheses/ )
4. [Palindrome partitioning](https://leetcode.com/problems/palindrome-partitioning-ii/ )
5. [Maximum Sum BST](https://leetcode.com/problems/maximum-sum-bst-in-binary-tree/ )
7. [Distinct subsequences](https://leetcode.com/problems/distinct-subsequences/ )
8. [best time to buy and sell stock-iii](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-iii/ )
9. [cheapest flight within k stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/ )
10. [Another coin problem](https://www.interviewbit.com/problems/another-coin-problem/)
11. [Evaluate expression to true](https://www.interviewbit.com/problems/evaluate-expression-to-true/)
12. [Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
13. [Burst Balloons](https://leetcode.com/problems/burst-balloons/)
