---
title: leetcode题解--寻找子串
excerpt: 题目：在一字符串中寻找子串，返回子串首字母索引，若未找到返回-1。
index_img: /img/leetcode.png
categories:
- java算法
tags:
- java
- 习题
---

# 寻找子串

> 题目:在一字符串中寻找子串，返回子串首字母索引，若未找到返回-1。
>
> 即找到在s1中遍历完s2的位置可求解
>
> 例如，s1=hello，s2=ll，则返回2

代码如下:

```java
Public int strstr(String s1,String s2){
    int l1= s1.length(),l2=s2.length();
    if(l1<l2) return -1;
    for(i=0;;i++){
        if(i+l2>l1) return -1;     //剩余长度不足以遍历完
        for(j=0;;j++){
            if(j=l2) return i;   //遍历完s2情况
            if(s1.charAt(i+j)!=s2.charAt(j))
                break;
        }
    }
    
}
```

