---
layout: post
title:  python文件作为Linux命令行工具
date:   2023-12-25 18:18:20 +0300
image:  wallhaven-47l7p3.jpg
tags:   study  python  linux
---


## Python文件作为Linux命令行工具



### 1.修改文件权限

将Python文件保存在Linux系统中，并添加可执行权限。可以使用 **chmod** 命令来修改文件的权限，例如：**chmod +x /path/to/your/file.py**。

### 2.文件开头添加声明

在文件的开头添加 **#!/usr/bin/env python** 或 **#!/usr/bin/python** 声明文件使用 Python 解释器来解释执行。前者会自动寻找系统中安装的 Python 解释器，后者则指定了 Python 解释器的路径。

### 3.在Linux系统中添加一个符号链接

使得用户可以在任意目录下使用该命令行工具。可以使用 **ln -s** 命令来创建符号链接，例如：

```shell
sudo ln -s /path/to/your/file.py /usr/local/bin/command-name
# 其中 `command-name` 是您希望用户在命令行中输入的命令名称。
```

完成上述步骤后，用户就可以在命令行中输入 **command-name** 命令来执行 Python 文件了。如果需要传入参数，可以在命令后面添加参数，例如：**command-name arg1 arg2** 。
