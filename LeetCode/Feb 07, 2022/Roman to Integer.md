# Feb 07, 2022
## Question - 9. Palindrome Number
https://leetcode.com/problems/roman-to-integer/

## Related Topics
    Hash Table
    Math
    String

## Solution - Using Python

```
class Solution(object):
    def romanToInt(self, s):
        romanToValue={'M':1000,'CM':900,'D':500,'CD':400,'C':100,'XC':90,'L':50,'XL':40,'X':10,'IX':9,'V':5,'IV':4,'I':1}

        value=0
        cursor=0

        while cursor<len(s):
            # Check current character and next character
            if (cursor+1)!=len(s) and s[cursor]+s[cursor+1] in romanToValue: 
                value+=romanToValue[s[cursor]+s[cursor+1]]
                cursor+=2
            else:
                value+=romanToValue[s[cursor]]
                cursor+=1
        return value
```

## Something I learned from this problem

1. If s = "III", because it is a String, len(s) = 3.