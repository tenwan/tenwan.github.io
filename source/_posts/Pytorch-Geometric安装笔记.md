---
title: Pytorch-Geometric安装笔记
categories:
- 深度学习
tags:
- 图神经网络
---
# 基础环境

1.操作系统：win10

2.python版本：3.6.10

3.cuda版本：10.1

4.pytorch版本：1.6.0

# 相关依赖包

安装pytorch-geometric前，需要先安装四个前置依赖，选择离线安装，这样比较快。

>torch-scatter
>
>torch-sparse
>
>torch-cluster
>
>torch-spline-conv

在https://pytorch-geometric.com/whl/可选择对应版本下载，我选择的是torch-1.6.0+cu101

得到四个包,放入文件夹，然后本地离线加载。

>torch_cluster-1.5.7-cp36-cp36m-win_amd64.whl
>
>torch_scatter-2.0.5-cp36-cp36m-win_amd64.whl
>
>torch_sparse-0.6.7-cp36-cp36m-win_amd64.whl
>
>torch_spline_conv-1.2.0-cp36-cp36m-win_amd64.whl

然后在载入四个前置依赖后，输入

pip install torch-geometric

没有报错，即安装完成。

