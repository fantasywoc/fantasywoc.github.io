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

## 添加命令行参数处理
在命令行后面添加参数，可以使用 **sys.argv**来获取这些参数。**sys.argv**是一个 Python 列表，包含了在命令行中传递的所有参数。列表的第一个元素是脚本本身的名称，从第二个元素开始，依次是命令行中传递的每个参数。

以下是一个简单的示例程序，演示如何在命令行中添加参数：

```python
import sys

def main():
    # 获取命令行参数
    args = sys.argv[1:]
    # 打印参数列表
    print(args)

if __name__ == '__main__':
    main()
```
在上面的示例中，我们定义了一个 **main()** 函数来获取命令行参数，并打印这些参数。我们使用 **sys.argv[1:]** 来获取除了脚本名称以外的所有参数，并将它们保存在 **args** 变量中。然后，我们直接打印 **args**，以显示所有的参数。

假设我们将上面的代码保存为 test.py 文件，并将其添加到 Linux 命令行工具中。如果要在命令行中传递参数，可以使用以下命令：
```shell
python test.py arg1 arg2 arg3
```
在上面的命令中，我们将 test.py 作为 Python 脚本文件执行，并在命令后面添加了三个参数：arg1、arg2 和 arg3。当执行此命令时，Python 解释器将读取 sys.argv 列表，并将其设置为 **['test.py', 'arg1', 'arg2', 'arg3']**。
在 main() 函数中，我们使用 sys.argv[1:] 获取除了第一个元素以外的所有元素，即 **['arg1', 'arg2', 'arg3']**，并将其打印输出。

