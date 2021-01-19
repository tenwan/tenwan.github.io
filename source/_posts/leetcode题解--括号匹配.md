---
title: leetcode题解--括号匹配
excerpt: 题目：判断括号匹配的情况
index_img: /img/leetcode.png
categories:
- java算法
tags:
- java
- 习题
---

# 括号匹配

> 可以考虑使用数组来模拟栈操作，另外让top=1，省去判断栈空，和数组越界的问题
>
> 在遇到）时，判断栈顶是否是（，以此类推

代码如下:

```java
Public boolean isvalid(String s){
    char[] stack = new char[s.length()+1];
    int top=1;
    for(char c:s.toCharArray()){
        if(c=='('||c=='['||c=='{'){
            stack[top++]=c;
        }
        else if(c=='）'&&stack[--top]!='('){
            return false;
        }
        else if(c==']'&&stack[--top]!='['){
            return false;
        }
        else if(c=='{'&&stack[--top]!='}'){
            return false;
        }
    }
    return top==1;
}
```

