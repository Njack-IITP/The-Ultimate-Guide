# Trie:

- [Tutorial 1](https://www.hackerearth.com/practice/data-structures/advanced-data-structures/trie-keyword-tree/tutorial/)
- [Tutorial 2](https://www.hackerearth.com/practice/notes/lalitkundu95/tutorial-on-trie-and-example-problems/)

- [Video](https://www.youtube.com/watch?v=AXjmTQ8LEoI)

* Used to calculate length of common prefix of strings or related question.
* Used to calculate [maximum subarray XOR in a given array](https://www.geeksforgeeks.org/find-the-maximum-subarray-xor-in-a-given-array/) 
* Used to calculate [Maximum XOR Pair](https://www.youtube.com/watch?v=jCu-Pd0IjIA)

## Practice Problems

Note: SOme problems can be done using sets/map. Try to think solution using tries.

#### Easy

1. [Tries Insert and Search](https://practice.geeksforgeeks.org/problems/trie-insert-and-search/0)
2. [Tries](https://www.hackerearth.com/practice/data-structures/advanced-data-structures/trie-keyword-tree/practice-problems/algorithm/tries-78733022/)
3. [Unique rows in boolean matrix](https://practice.geeksforgeeks.org/problems/unique-rows-in-boolean-matrix/1)
[Count of distinct substrings](https://practice.geeksforgeeks.org/problems/count-of-distinct-substrings/1)
4. [Pair of strings having longest common prefix of maximum length in given array](https://www.geeksforgeeks.org/pair-of-strings-having-longest-common-prefix-of-maximum-length-in-given-array/)
5. [Longest Word in Dictionary](https://leetcode.com/problems/longest-word-in-dictionary/)

#### Medium

1. [Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/)
2. [Trie delete](https://practice.geeksforgeeks.org/problems/trie-delete/1)
3. [ Maximum XOR of Two Numbers in an Array](https://leetcode.com/problems/maximum-xor-of-two-numbers-in-an-array/)
4. [Replace words](https://leetcode.com/problems/replace-words/)
5. [Map sum](https://leetcode.com/problems/map-sum-pairs/)

#### Hard

1. [Hotel Reviews](https://www.interviewbit.com/problems/hotel-reviews/) 
2. [Shortest unique prefix](https://www.interviewbit.com/problems/shortest-unique-prefix/)
3. [Palindrome pairs](https://www.interviewbit.com/problems/palindrome-pairs/) : Can be done using Hashing. If using a struct, remember to clear the memory before the next call. because it might happen that GCC hasn't cleared previous memory before the next call or you might have memory leak issues like not deleting from the heap.
4. [Anagrams](https://www.interviewbit.com/problems/anagrams/) : Can be solved using tries, but hashing(using maps) does better as fewer chances for memory leaks and easy to implement.