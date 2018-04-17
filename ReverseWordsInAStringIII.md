## 问题分析：
给定一个字符串，需要颠倒一个句子中每个单词中的字符顺序，同时仍保留空格和初始单词顺序.
## 编程实现：
``` c++
class Solution {
public:
    string reverseWords(string s) {
           string res = s;
        int left = 0;
        int right = 0;
        for(int i=0; i<res.length()+1; i++){
            if(res[i]==' ' || res[i]=='\0'){
                left = right;
                right = i-1;
                int L = left;
                int R = right;
                for(; L<R; ++L,--R){
                    char temp = res[L];
                    res[L] = s[R];
                    res[R] = temp;
                }
                right = i+1;
            }
        }
        return res;
    }
    
};
```
## 总结体会：
将英文句子分割成单个单词，将每个单词反转以单词中间字母为中心，前后对称位置的字母交换位置.