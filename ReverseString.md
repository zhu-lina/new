## 问题分析：
编写一个函数，将字符串s作为输入参数，输出s逆序的字符串.
## 编程实现：
``` c++
class Solution {
public:
    string reverseString(string s) {
        string ret = s;
        
        for (int i = 0, j = ret.size() - 1; i < j; ++i, --j) 
        {
            char s = ret[i];
            ret[i] = ret[j];
            ret[j] = s;
        }
        
        return ret;
    }
    
};
```
## 总结体会：
从字符串首部、尾部分别向中心位置进行遍历，每次交换首尾的字符，直到首部下标大于等于尾部下标.