---
title: pyinstaller安装失败
date: 2022-12-23 17:33:27
tags: "技术"
---

### 正文

今天我在Windows11下的Python环境中用pip安装pyinstaller，结果报错：

> ERROR: Could not install packages due to an OSError: [Errno 22] Invalid argument:

搜遍全网，也没找到解决方案，大概是刚有的问题。

临时解决方案是从[Releases · pyinstaller/pyinstaller (github.com)](https://github.com/pyinstaller/pyinstaller/releases)下载最新版本的源码，之后在源码目录下执行：

```shell
python setup.py install
```

但我执行时提示该选项已废除，需要执行以下命令代替：

```shell
pip install .
```

### 后记

1. 这种情况按道理应该去提一个issues的，但我的英语水平实在太差，于是就不得不作罢了（又想起我在Linux Mint官方Twitter号上的反馈，完全是百度翻译……）

2. 细心的可能会问：你怎么用Windows11来了，唉，说来话长，且听下回分解……（about那篇文章还没改）

### 更新

突然发现：

![](https://pic.imgdb.cn/item/63a705c508b6830163b6d6f5.jpg)

不得不说，Windows安全中心比任何国产杀毒软件都强。
