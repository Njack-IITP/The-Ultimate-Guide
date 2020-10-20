# Binary Search

- [Tutorial 1](https://www.geeksforgeeks.org/binary-search/)
- [Tutorial 2](https://leetcode.com/explore/learn/card/binary-search/138/background/1038/discuss/423162/Binary-Search-101)
- [Video](https://www.youtube.com/watch?v=P3YID7liBug)


### Binary Search Templates:

- <b>Template 1:</b> 
  used to search for an element or condition which can be determined by accessing a single index in the array. Search Condition can be determined without comparing to the element's neighbors (or use specific elements around it).
  ```
      Initial Condition: left = 0, right = length-1
      Termination: left > right
      Searching Left: right = mid-1
      Searching Right: left = mid+1
      
      int binarySearch(vector<int>& nums, int target){
         if(nums.size() == 0)
          return -1;

        int left = 0, right = nums.size() - 1;  // Initial condition
        while(left <= right){
          int mid = left + (right - left) / 2;  // Prevent (left + right) overflow
          if(nums[mid] == target) 
            return mid; 
          else if(nums[mid] < target)  
            left = mid + 1;     //  Searching right
          else 
            right = mid - 1;    // Searching left
        }
        // End Condition: left > right
        return -1;
    }
  ```
  ##### Practice Questions:
  1. [Binary Search](https://leetcode.com/problems/binary-search/)
  2. [Search Insert Position](https://leetcode.com/problems/search-insert-position/)
  3. [Guess Number Higher or Lower](https://leetcode.com/problems/guess-number-higher-or-lower/)
  
  
  
- <b>Template 2:</b> 
  It is used to search for an element or condition which requires accessing the current index and its immediate right neighbor's index in the array.
  ```
      Initial Condition: left = 0, right = length
      Termination: left == right
      Searching Left: right = mid
      Searching Right: left = mid+1
      
      int binarySearch(vector<int>& nums, int target){
          if(nums.size() == 0)
            return -1;

          int left = 0, right = nums.size();
          while(left < right){
            int mid = left + (right - left) / 2; // Prevent (left + right) overflow
            if(nums[mid] == target){ return mid; }
            else if(nums[mid] < target) { left = mid + 1; }
            else { right = mid; }
          }

          // Post-processing:
          // End Condition: left == right
          if(left != nums.size() && nums[left] == target) return left;
          return -1;
        }
  ```
  
  ##### Practice Questions:
  1. [Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
  2. [First Bad version](https://leetcode.com/problems/first-bad-version/)
  3. [Peak Index in a Mountain Array](https://leetcode.com/problems/peak-index-in-a-mountain-array/)
  4. [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
  5. [Find Peak Element](https://leetcode.com/problems/find-peak-element/)
  
 
## Beyond Sorted Array Binary Search
  - Binary search obviously works on searching for elements in a sorted array. But it works is because the array itself is monotonic ( either increasing or decreasing ). So, if you are a particular position, you can make a definite call whether the answer lies in the left part of the position or the right part of it.
  <br> Similar thing can be done with monotonic functions ( monotonically increasing or decreasing ) as well.
  Lets say we have f(x) which increases when x increases.
  <br> So, given a problem of finding x so that f(x) = p, I can do a binary search for x.<br>
    At any instance,
    1. if f(current_position) > p, then I will search for values lower than current_position.
    2. if f(current_position) < p, then I will search for values higher than current_position
    3. if f(current_position) = p, then I have found my answer.

    #### Practice Questions:
    1. [Sqrtx](https://leetcode.com/problems/sqrtx/)
    2. [Capacity To Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/)
    3. [Painter's Partition Problem](https://www.interviewbit.com/problems/painters-partition-problem/)
    4. [Allocate books](https://www.interviewbit.com/problems/allocate-books/)


### More Practice Problems:
1. [Search a 2D Matrix II](https://leetcode.com/problems/search-a-2d-matrix-ii/)
2. [Heaters](https://leetcode.com/problems/heaters/)
3. [Kth Smallest Element in a Sorted Matrix](https://leetcode.com/problems/kth-smallest-element-in-a-sorted-matrix/)
4. [Find Minimum in Rotated Sorted Array II](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array-ii/)
5. [Split Array Sum](https://leetcode.com/problems/split-array-largest-sum/)
6. [Median of two sorted arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
7. [Matrix median](https://www.interviewbit.com/problems/matrix-median/)


## References:
1. [Binary Search-leetcode](https://leetcode.com/explore/learn/card/binary-search/136/template-analysis/)

 
