---
layout: post
title:  Godot 物理齿轮
date:   2025-10-11 18:18:20 +0300
image:  Gear.jpg
tags:   study godot C++
---


# [Godot 齿轮系统 C++ 扩展](https://github.com/fantasywoc/godot_GearWheel_extension)

## 项目介绍

这是一个基于 Godot Engine 的 C++ 扩展，提供完整的 2D 齿轮物理系统，支持机械结构模拟与游戏应用。该扩展使用 GDExtension 技术，为 Godot 引擎添加了专业的齿轮相关功能。

## 核心功能

### 1. 齿轮碰撞多边形系统
- `GearCollisionPolygon` 类：继承自 `CollisionPolygon2D`，支持自定义齿轮参数
- 自动计算齿轮顶点，生成碰撞形状
- 支持调整齿数、齿宽、齿高、半径等参数
- 智能半径调整算法，确保齿轮参数符合几何约束

### 2. 齿轮计算核心
- `GearWheelCalculator` 类：实现齿轮几何计算
- 弦长与圆心角计算
- 360度可整除性验证
- 双向搜索算法寻找最优齿轮半径

### 3. 可旋转刚体系统
- `RotatableRigidBody` 类：实现自动旋转功能
- 支持自定义旋转速度和方向
- 物理过程中自动应用旋转力

### 4. 编辑器集成
- C++ 编辑器插件与 GDScript 插件协同工作
- 在 Godot 编辑器中提供直观的参数调整界面

## 技术特点

- **跨平台支持**：支持 Windows、Linux、macOS、Android 等平台
- **性能优化**：C++ 实现核心计算，确保运行效率
- **模块化设计**：清晰的类结构和职责分离
- **几何算法**：实现了精确的齿轮几何计算
- **编辑器集成**：提供友好的编辑器界面

## 编译

```bash
# 清理缓存
scons -c
# 编译（默认编译debug single）
scons
```

### Release 版本
```bash
scons target=template_release precision=single
scons target=template_release precision=double
```

### Debug 版本
```bash
scons target=template_debug precision=single
scons target=template_debug precision=double
```

## 安装与使用

1. 编译扩展后，将生成的动态库文件复制到项目的 `addons/rigid_body/bin/` 目录下
2. 在 Godot 项目中启用插件
3. 在场景中添加 `GearCollisionPolygon` 和 `RotatableRigidBody` 节点
4. 通过 Inspector 面板调整齿轮参数

## 示例项目

项目包含 `demo` 目录，提供了示例场景和使用方法：
- `example.tscn`：展示基本齿轮系统
- `test.tscn`：测试齿轮参数调整
- `wheel.tscn`：展示可旋转刚体的使用

## 项目结构

- `src/`：核心源代码
  - `GearWheelCalculator.h`：齿轮几何计算
  - `gear_collision_polygon.h/cpp`：齿轮碰撞多边形
  - `rotatable_rigid_body.h/cpp`：可旋转刚体
  - `editor_plugin.h/cpp`：编辑器插件
- `demo/`：示例项目
- `bin/`：编译输出目录
- `godot-cpp/`：Godot C++ 绑定库

## 技术实现细节

### 插件架构
C++ 编写的 `RotatableEditorPlugin`（继承 EditorPlugin）和 GDScript 编写的 `plugin.gd`（同样继承 EditorPlugin）是两个独立的插件入口，但 Godot 会将它们合并为同一个插件的一部分：
- `plugin.cfg` 是插件的核心配置文件，指定了插件的基本信息（名称、描述等）
- C++ 插件通过 EditorPlugin 注册底层功能（如自定义 Inspector、节点类型）
- GDScript 的 `plugin.gd` 会被 Godot 识别为插件的脚本入口，用于补充编辑器逻辑（如打印日志、添加菜单等）
- 两者会在插件启用时同时生效，C++ 部分负责高性能的底层扩展，GDScript 部分负责灵活的上层编辑器逻辑，形成互补



## 应用场景

- 2D 物理模拟中的齿轮系统
- 机械结构可视化
- 游戏中的齿轮机制
- 教育类应用中的机械原理展示

## 许可证

MIT License

## 贡献

欢迎提交 Issue 和 Pull Request 来改进这个项目！
