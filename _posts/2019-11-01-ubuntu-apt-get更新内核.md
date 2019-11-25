---
layout:     post
title:      ubuntu apt-get更新内核
subtitle:   ubuntu 更新内核
date:       2019-11-01
author:     Frog
header-img: img/my.jpg
catalog: true
tags:
    - ubuntu
---

## 首先

    sudo apt-get update

    sudo apt-get full-upgrade


## 查看已安装的内核

    sudo dpkg -l | grep linux-image

## 查看当前使用的内核

    sudo uname -r

## 查看可安装的内核

    sudo apt-cache search linux-image

## 安装新内核

    sudo apt-get install linux-image-$(uname -r)-generic

## 卸载不需要的内核 (一般无需卸载)

    sudo apt-get purge linux-image-xxx-generic

## 更新 grub

    sudo update-grub




### 参考资料


- [Ubuntu 18.04 手动升级内核](https://www.cnblogs.com/gaowengang/p/11272947.html)
