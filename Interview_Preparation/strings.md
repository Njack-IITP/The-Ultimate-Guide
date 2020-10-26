# Strings

- Videos:
	* [Character Array and Pointers](https://www.youtube.com/watch?v=Bf8a6IC1dE8)
	* [Strings](https://www.youtube.com/watch?v=3rDp0yOACZQ)
- [Tutorial: Strings GFG](https://www.geeksforgeeks.org/stdstring-class-in-c/)

## Implementation
   ```
    C style char arrays work in C++ as well.  However, C++ provides string which is much more powerful than C arrays. 
	String declaration :
	    string A; // declares an empty string
	    string A = "Hello"; // declares string initialized to "Hello".

	Accessing ith element :
	    A[i] // O(1)

	Size ( number of elements ) of the string :
	    A.length()  // O(1)

	Appending to the string :
	    A += "Hello"; // Appends Hello to the string. O(n) operation
	    A.push_back('H'); // Append character H to the string. O(1) operation. 
   ```
	

   #### Practice Questions:
   (May skip if comfortable in using strings)
   1. [Consecutive Characters](https://leetcode.com/problems/consecutive-characters/)
   2. [First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
   3. [Ransom note](https://leetcode.com/problems/ransom-note/)
   4. [Amazing subarrays](https://www.interviewbit.com/problems/amazing-subarrays/)
   5. [Palindrome string](https://www.interviewbit.com/problems/palindrome-string/)
   6. [Count and Say](https://www.interviewbit.com/problems/count-and-say/)
   7. [Group Anagrams](https://leetcode.com/problems/group-anagrams/)


## KMP

- [Tutorial 1](https://www.hackerearth.com/practice/algorithms/string-algorithm/string-searching/tutorial/)
- [Tutorial 2](https://cp-algorithms.com/string/prefix-function.html)
- [Video1](https://www.youtube.com/watch?v=KG44VoDtsAA)
- [Video2](https://www.youtube.com/watch?v=cH-5KcgUcOE)


##### Practice Questions:
1. [Test Your Understanding](https://www.hackerearth.com/practice/algorithms/string-algorithm/string-searching/tutorial/)
2. [Implement strstr](https://leetcode.com/problems/implement-strstr/)
3. [Minimum characters required to make a string palindromic](https://www.interviewbit.com/problems/minimum-characters-required-to-make-a-string-palindromic)
4. [Repeated substring pattern](https://leetcode.com/problems/repeated-substring-pattern/)


## Manachar Algorithm

- [Tutorial](https://www.hackerearth.com/practice/algorithms/string-algorithm/manachars-algorithm/tutorial/)
- [Video](https://www.youtube.com/watch?v=nbTSfrEfo6M)

##### Practice Questions:
1. [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
2. [Palindromic substrings](https://leetcode.com/problems/palindromic-substrings/)


## Robin Karp Algorithm
- [Tutorial](https://www.geeksforgeeks.org/rabin-karp-algorithm-for-pattern-searching/)
- [Rolling Hash](https://www.youtube.com/watch?v=BQ9E-2umSWc)
- [Robin Karp Algorithm](https://www.youtube.com/watch?v=H4VrKHVG5qI)

##### Practice Questions:
Most of the KMP problems can be solved using Robin Karp Algorithm but it is used less because  hashing will not be 100% deterministically correct, because two complete different strings might have the same hash (the hashes collide). [Read more here](https://cp-algorithms.com/string/string-hashing.html)

1. [NHAY - A Needle in the Haystack](https://www.spoj.com/problems/NHAY/)
2. [SUB_PROB - Substring Problem](https://www.spoj.com/problems/SUB_PROB/)
3. [Distinct Echo Substrings](https://leetcode.com/problems/distinct-echo-substrings/)
4. [Longest Chunked Palindrome Decomposition](https://leetcode.com/problems/longest-chunked-palindrome-decomposition/)
