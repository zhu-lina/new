## 问题分析：
在一个字符串中，找出第一个不重复字母的索引，如果不存在，则返回-1.
## 编程实现：
``` c++
class Solution {
public:
    int firstUniqChar(string s) {
         vector<int>count(26);
        for (int i = 0; i < (int)s.size(); i++)
        {
            count[s[i] - 'a'] ++;
        }
        for (int i = 0; i < (int)s.size(); i++)
        {
            if (count[s[i] - 'a'] == 1)
                return i;
        }
        return -1;
    }
};
```
## 总结体会：
  先进行字频统计，然后找出第一个出现次数为1的字符.