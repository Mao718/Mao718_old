# Leetcode 49 Group Anagrams

```
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        dic = dict()
        for str_ in strs:
            sort_str = "".join(sorted(str_ , key = str.lower))
            if sort_str not in dic:
                dic[sort_str] = [str_]
            else :
                dic[sort_str].append(str_)
        return list(dic.values())
```
## Idea of solving
The idea of solving such a question is that the Anagrams have the same component, however, the difficulty is to compare the latter in a different order. Hence, if I sort the string before the comparison it will be much easier.  
First, a dictionary is created to save the data, the key of the dictionary is an ordered string and the value is all Anagram in strs. Then I used the for loop iterated into the strs list to check out if the string has the same ordered string as the previous. If true add the string to that key. If not then create a new one.
## Time complexity analyzation
Regarding the time complexity, since we using the sort inside the for loop, the time complexity will be O(N log(M)). N is length of the strs and M is length of each string.