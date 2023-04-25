
## Task 1 **Technical Skills**

Given an input string s, find the length of the first longest substring without repeating characters.
**Difficulty: Easy**

Answer:

* To solve this problem, we can use the sliding window technique. We start with an empty substring and keep adding characters to it one by one. If a repeating character is encountered, we remove the first character of the substring until there are no repeating characters left. We keep track of the length of the longest substring encountered so far and return it as the answer.


* Python code for the above question:

'''

def lengthOfLongestSubstring(s: str) -> int:
    n = len(s)
    seen = {}
    left = 0
    right = 0
    max_len = 0
    
    while right < n:
        if s[right] in seen and seen[s[right]] >= left:
            left = seen[s[right]] + 1
        seen[s[right]] = right
        max_len = max(max_len, right - left + 1)
        right += 1
    
    return max_len

'''
