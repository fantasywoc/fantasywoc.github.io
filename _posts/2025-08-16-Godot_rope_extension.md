---
layout: post
title:  Godot 物理软绳模拟
date:   2025-08-16 18:18:20 +0300
image:  rope_cover.png
tags:   study  godot C++
---

## 📊 动态统计
[![Stars](https://img.shields.io/github/stars/fantasywoc/Godot-Rope-Extension?label=Stars&color=yellow&logo=github)](https://github.com/fantasywoc/Vimag/stargazers)
[![Forks](https://img.shields.io/github/forks/fantasywoc/Godot-Rope-Extension?label=Forks&color=blue&logo=github)](https://github.com/fantasywoc/Vimag/network/members)
[![Downloads](https://img.shields.io/github/downloads/fantasywoc/Godot-Rope-Extension/total?label=Downloads)](https://github.com/fantasywoc/Godot-Rope-Extension/releases)
## ⭐ 星标历史 Star History
<a href="https://star-history.com/#fantasywoc/Godot-Rope-Extension&Date"> 
<picture>   
<source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=fantasywoc/Godot-Rope-Extension&type=Date&theme=dark" />   
<source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=fantasywoc/Godot-Rope-Extension&type=Date" />   
<img alt="Star History Chart" src="https://api.star-history.com/svg?repos=fantasywoc/Godot-Rope-Extension&type=Date" /> 
</picture>
</a>


<div align=center>
<h1>Godot C++ 绳索模拟demo</h1>
<a href="https://github.com/fantasywoc/Godot-Rope-Extension?tab=readme-ov-file"><img src="https://img.shields.io/badge/Author-Fantasy-orange" alt="Author" /></a>
<img src="https://img.shields.io/github/languages/count/fantasywoc/Godot-Rope-Extension" alt="languages-count" />

<img src="https://img.shields.io/github/last-commit/fantasywoc/Godot-Rope-Extension" alt="last-commit" />

</div>


##  项目概述

这是一个基于 Godot 4 和 C++ 的绳索项目，使用 C++ GDExtension  和 gdscript

![afa20e](https://github.com/fantasywoc/Godot-Rope-Extension/blob/main/rope_cover.png)

## RopeDemo快捷键

- 左键双击：剪短该节点到末尾的绳索
- 右键单击：锁定/解锁节点
- 左键拖拽：移动锁定节点/移动解锁节点
- 滚轮：增减绳索节点
- ctrl+滚轮：增加/减少绳索节点长度
- up/down：增加/减少重力影响

# C++扩展编译
详细C++扩展和说明可以参考       **[Godot C++ 扩展编译demo](https://github.com/fantasywoc/godot_cpp_extension)**

```bash
#清理缓存
scons -c
#编译（默认编译debug single）
scons
```
### release版本
```bash
scons target=template_release precision=single
scons target=template_release precision=double

```


### debug版本
```bash
scons target=template_debug precision=single
scons target=template_debug precision=double
```

  
### 🎯 物理模拟
- **Verlet 积分算法** 

## 项目结构

```
Godot_c++/
├── src/                    # C++ 源代码
│   ├── example_class.h     # 绳索类头文件
│   ├── example_class.cpp   # 绳索类实现
│   └── register_types.cpp  # Godot 类型注册
├── demo/                   # Godot 项目： 绳索demo
│   ├── rope_demo.gd        # GDScript 演示脚本
│   └── example.tscn        # 演示场景
├── doc_classes/            # Godot 文档
│   └── ExampleClass.xml    
└── bin/                    # 编译输出库文件
    └── windows/            # 平台特定库文件
```

- **Godot 4.x** - 游戏引擎
- **C++17** - 核心语言
- **GDExtension** - Godot 扩展接口
- **CMake/SCons** - 构建系统
- **Verlet 积分** - 物理算法

## 主要类和方法

### ExampleClass (绳索模拟器)

**核心方法：**
- `setElasticity()` - 设置弹性参数
- `setElasticityPreset()` - 使用预设模式
- `update_physics()` - 物理更新
- `apply_force()` - 施加外力

**节点操作：**
- `set_node_position()` - 设置节点位置
- `setNodeLocked()` - 锁定/解锁节点
- `remove_node()` - 移除节点
- `cut_rope_at()` - 剪断绳索

**属性控制：**
- `node_count` - 节点数量 
- `rope_length` - 绳索长度
- `gravity` - 重力向量
- `debug_draw` - 调试绘制











        
