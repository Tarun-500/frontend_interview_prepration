### 1. Given an array of integers nums and a positive integer k, find wheather it's possible to divide this array into k non-empty subsets whose sums are all equal.
input : nums = [4,3,2,3,5,2,1], k =4
output: true


### 2. Given an non-negative integer, you could swap two digits at most once to get the miximum valued number. return the maximum valued number you could get.
input : 2736
output: 7236


### 3. You hvae 4 cards each containing a number from 1 to 9. you need to judge whether they could operated through *,/,+,-,(, ) to get the value of 24.
input : [4, 1, 8, 7]
output: true


### 4. Given two sorted arrays of size m and n of distint elements. Given a value x. The problum is to count all pairs form both arrays whose sum is equal to x. Note: The pair has an element form each array.
input : 44
        1 3 5 7
        2 3 5 8
        10
output: 2

### 5. Given a string consisting of lowercase letters, arrange all its letters in ascending order.
input : 5
        edcab
output: abcde

### 6. Given a string consisting of lowercase letters, arrange all its letters in ascending order.
input : 5
        edcab
output: abcde


### 7. Given an array of n integers (duplicates allowed) print 'yes' if it is a set of contiguous integers else print 'no'.
input : 52364466
output: Yes  (the elements of array form a contiguos set of integers which is {2,3,4,5,6} so the out is yes.)


### 8. In given range, print all numbers having unique digits. e.g. in range 1 to 20 should print all numbers expect 11.
input : 1 10 20
output: 10 12 13 14 15 16 17 18 19 20


### 9. Given an integer n, you need to print all numbers less than n which are having digits only 3 or 7 both.
input : 10
output: 3, 7


### 10. Merge k sorted linked lists and return it as one sorted list .
input : 1 -> 10 -> 20
        4 -> 11 -> 13
        3 -> 8 -> 9
output: 1 -> 3 -> 4 -> 8 -> 9 -> 10 -> 11 -> 13 -> 20



### 11. Given an array with repeated elements, the task is to find the maximum distance between two occurrences of an element.
input : 6  [1, 1, 2, 2, 2, 1]
output: 5



### 12. Given an n-ary tree, retun the postorder traversal of its nodes values nary-Tree input serialization is represented in their level order traversal, each group of children is separated by the null value.
input : root = [1, null, 3, 2, 4, null, 5, 6]
output: [5, 6, 3, 2, 4, 1]



### 13. Given an integer array nums, find three numbers whose product is maximum and return the maximum product.
input : nums = [1,2,3]
output: 6



### 14. Given a positive integer n, find the number of non-negative integers less than or equal to n, whose binary representations do NOT contain consecutive ones.
input : 5
output: 5



### 15. Given a non-negative integer c, decide wheather there are two integers a and b such that a2 + b2 = c.
input : c = 5
output: true



### 16. Given an integer array nums, find threee numbers whose product is maximum and return the maximum product.
input : nums = [1, 2, 3]
output: 6



### 17. Given a non empty string s, you may delet at most one character. judge wheather you can make it a palindrome.
input : "aba"
output: true



### 18. Given a positive integer, check whaether it has alternative bits: namely, if two adjacent bits will always have different values.
input : n = 5
output: true



### 19. Merge k sorted llinked lists and return it as one sorted list.
input : 1 -> 10 -> 20
        4 -> 11 -> 13
        3 -> 8 -> 9
output: 1 -> 3 -> 4 -> 8 -> 9 -> 10 -> 11 -> 13 -> 20



### 20. Given a string S of lowercase alphabets, check if it is isogram or not. An isogram is a string in which no letter occurs more than once.
input : 2,  Coding , CodingClub 
output: 1, 0



### 21. Given a string str and another string patt. Find the character in patt that is present at the minimum index in str. if no character of patt is present in str then print 'No character present'.
input : codingMafia      mod
output: o



### 22. Given a number n, count minimum steps to minimize it to 1 according io the following criteria: if n is divisible by 2 then we may reduce n to n/2. if n is divisible by 3 then you may reduce n to n/3. Decrement n by 1.
input : n = 10
output: 3



### 23. Given a sorted aarray and a value X, the floor of x is the largest element in array smaller than or equal to x. write efficient functions to find floor of x.
input : arr[] = {10, 12, 19, 25, 30}, x = 20
output: 25


### 24. Given a string, your task is to count how many palindromic substrings in this string. the substring with diffrent start indexes or end indexes are counted as different substrings even they consist of same characters.
input : "abc"
output: 3



### 25. Given a positive 32-bit integer n, you need to find the smallest 32-bit integer which has exactly the same digits existing in the integer n and is greater in value than n. if no such positive 32-bit integer exists, you need to return -1.
input : 12
output: 21



### 26. Subarray sum Equals K given an array of integers nums and an integerr k, return the total number of continuous subarrays whose sum equals to k.
input : nums = [1, 1, 1], k = 2
output:  2



### 27. Complex Number multiplication given two strings representing two complex numbers. you need to return a string representing their multiplication. note i2 = -1 according to the definition. 
input: "1+1i", "1+1i"
output: "0+2i"





 

### 28. You are given two strings `x` and `y`. Return the **minimum number of times** you need to repeat string `x` so that string `y` becomes a **subsequence** (not necessarily contiguous, but order preserved) of the repeated string.

If it is **impossible**, return `-1`.

### Notes:
- Repeating `x` **0 times** gives `""` (empty string)
- Repeating `x` **1 time** gives `"abc"` (if `x = "abc"`)
- Repeating `x` **2 times** gives `"abcabc"`

---

## Examples

### Example 1
```js
Input: x = "abc", y = "acbac"
Output: 2

Explanation:
- Repeat "abc" 1 time → "abc" → "acbac" is NOT a subsequence
- Repeat "abc" 2 times → "abcabc" → "acbac" is a subsequence ✅
```





### 29. Given a non-empty list of words, return the k most frequent elements.

Your answer should be sorted by frequency from highest to lowest.
If two words have the same frequency, then the word with the lower alphabetical order comes first.

---

## Example

Input:
words = ["i", "love", "leetcode", "i", "love", "coding"], k = 2

Output:
["i", "love"]

---

## Explanation

* "i" appears 2 times
* "love" appears 2 times
* "leetcode" and "coding" appear 1 time

Since "i" and "love" have the same frequency, we sort them alphabetically → "i" comes before "love"

---

## Constraints

* 1 ≤ words.length ≤ 500
* 1 ≤ k ≤ number of unique words
* Words consist of lowercase English letters

---





#### Number of Longest Increasing Subsequences - Given an integer array `nums`, return the number of longest increasing subsequences.

Notice that the sequence has to be strictly increasing.

---

## Example

Input:
nums = [1,3,5,4,7]

Output:
2

---

## Explanation

The longest increasing subsequences are:

* [1, 3, 5, 7]
* [1, 3, 4, 7]

So, the total number of longest increasing subsequences is 2.

---

## Constraints

* 1 ≤ nums.length ≤ 2000
* -10⁶ ≤ nums[i] ≤ 10⁶

--- 
