---
title: leetcode题解--寻找插入位置
excerpt: 题目：从一个无重复元素已排序数组找到插入位置索引。例如，[1,3,5,6],插入数字2，即返回1；[1，3，5，6] 插入数字5，即返回2；
index_img: /img/leetcode.png
categories:
- java算法
tags:
- java
- 习题
---

# 寻找插入位置

>题目:从一个无重复元素已排序数组找到插入位置索引。例如，[1,3,5,6],插入数字2，即返回1；[1，3，5，6] 插入数字5，即返回2；

可通过二分查找找到第一个大于等于target元素位置

代码如下:

```java
Public int result(int[] nums,int target){
    int left =0,right=nums.length-1,mid = (right+left)>>1;
    while(left<=right){
        if(target<=nums[mid]){
            right=mid-1;
        }
        else{
            left = mid+1;
        }
        mid = (right+left)>>1
    }
    return left;
}
```

