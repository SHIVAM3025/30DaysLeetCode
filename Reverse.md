# Reverse String
Write a function that reverses a string. The input string is given as an array of characters char[].

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

You may assume all the characters consist of printable ascii characters.
##  Example 1:
```
Input: ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
```
## Example 2:
```
Input: ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]
```

## Code
```
class Solution {
    public void reverseString(char[] s) {
        int l=s.length%2==0? (s.length-1)/2 : s.length/2;
        if(s.length!=0){
            for(int i=0;i<=l;i++){
                char f=s[i];
                s[i]=s[s.length-1-i];
                s[s.length-1-i]=f;
            }
        }
    }
}
```
## Time Complexity
```
Time complexity : O(N)
Space Complexity : O(1)
```