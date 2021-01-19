---
title: leetcode题解--移除有序数组重复元素
excerpt: 移除有序数组重复元素，返回剩余元素个数。例如[1,1,2,2,3],返回3
index_img: /img/leetcode.png
categories:
- java算法
tags:
- java
- 习题
---

# 移除有序数组重复元素

> 题目:移除有序数组重复元素，返回剩余元素个数。例如[1,1,2,2,3],返回3
>
> 使用一个指针指向头部，进行赋值

代码如下:

```java
Public int result(int[] nums){
    int len = nums.length;
    if(len<=1) return len;
    int tail = 1;
    for(int i =1;i<len;++i){
        if(nums[i-1]!=nums[i]){
            nums[tail++]=nums[i];
        }
    }
    return tail;
}
 
```

