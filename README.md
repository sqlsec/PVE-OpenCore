# PVE-OpenCore

## 主要内容

基于原项目：https://github.com/thenickdude/KVM-Opencore/ 进行个人优化

主要就是升级一下最新的  OC 0.7.9 然后精简一下吧，下面是国光我精简优化的思路：

-  **ACPI  设置**
  - 只留几个实际加载的 SSDT：DTGP、EC、EHCI、PLUG
  - 删除「删除」和「补丁」中没有加载的选项
- **内核设置**
  - 修改仿冒 CPU 数据
    - 不清楚作者的这个数据哪来的，所以我换成自己比较熟悉的数据了
    - Cpuid1Data：55060A00 00000000 00000000 00000000
    - Cpuid1Mask：FFFFFF00 00000000 00000000 00000000
  - 只留下面 3 个必备的 Kexts 并保持最新：
    - Liu.kext
    - WhateverGreen.kext
    - USBPorts.kext

## 详细文章

关于 PVE 黑苹果生成环境的搭建详细可以参考我的这篇我文章：[PVE 虚拟化生产（黑苹果）环境配置优化记录](https://www.sqlsec.com/2022/04/pve.html)

## 支持一下

[打赏列表 | 国光](https://www.sqlsec.com/dashang.html)

用爱发电并不能持久，你们的打赏是我前进的动力，非常感激每一位打赏的朋友！金额大小无关情义，无论如何都非常感谢你们的支持，在这里会显示所有通过打赏方式支持我的人，打赏列表两天之内必会更新，谢谢各位的鼓励，大家一起努力进步。

