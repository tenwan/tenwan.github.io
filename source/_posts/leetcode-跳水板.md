---
title: leetcode题解--跳水板拼凑
excerpt: 题目：有两块板子，长度为x和y，假设有k块，输出所有可能的拼凑长度，例如x=1,y=2,k=3，输出[3,4,5,6] 
index_img: /img/leetcode.png
categories:
- java算法
tags:
- java
- 习题
---

# 跳水板拼凑

题目:有两块板子，长度为x和y，假设有k块，输出所有可能的拼凑长度，例如x=1,y=2,k=3，输出[3,4,5,6]

本题可看成首项为k*x，末项为k*y，公差为y-x的等差数列，每用长的替换短的，都是加一次公差，项数为k+1.

代码如下:

```java
Public int [] result(int shorter,int longer,int k){
    if(k==0){
        return new int[0];
    }
    if(shorter==longer){
        return new int[]{shorter*k};
    }
    int[] ans=new int[k+1];
    int sx = k*shorter;
    int delta = longer-shorter;
    for(int i =0;i<=k;i++){
        ans[i]=sx+i*delta;
    }
    return ans;
}
```

