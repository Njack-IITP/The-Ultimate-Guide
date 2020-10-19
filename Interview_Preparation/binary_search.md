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
  1. [First Bad version](https://leetcode.com/problems/first-bad-version/)
  2. [Peak Index in a Mountain Array](https://leetcode.com/problems/peak-index-in-a-mountain-array/)
  3. [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
  
 
 ## References:
 1. [Binary Search-leetcode](https://leetcode.com/explore/learn/card/binary-search/136/template-analysis/)
 
