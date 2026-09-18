# 第 1 次开发记录：首个 Godot Demo

- 日期：2026-09-18
- 阶段：Godot 新手入门
- 状态：已完成工程与场景基础搭建

## 本次目标

跟随 Godot 4 官方“你的第一个 2D 游戏”教程熟悉编辑器，创建第一个可以打开和运行的 Godot 工程，并为后续的俯视角 2D 游戏建立基础场景结构。

## 学习内容

本次主要接触了以下 Godot 概念：

- **项目**：保存游戏的场景、脚本、资源和全局设置。
- **节点**：Godot 中组成游戏对象的基本单元，每种节点承担一种职责。
- **场景**：由节点树组成的可保存、复用内容。
- **场景树**：描述节点之间的父子关系，以及游戏运行时的组织方式。
- **主场景**：启动游戏时首先加载的场景。

## 实现内容

创建了 `my-demo` Godot 工程，并完成以下配置：

- 项目名称设置为 `MyDemo`。
- 将 `main.tscn` 设置为主场景。
- 使用 Mobile 渲染方式，适合当前轻量 2D 项目。
- 画面拉伸模式设置为 `canvas_items`，宽高比设置为 `expand`。
- 添加 `Hello World` 标签，用于确认场景内容可以正确显示。

主场景中建立了玩家的基础节点树：

```text
Player (CharacterBody2D)
├── AnimatedSprite2D
├── CollisionShape2D
├── AudioStreamPlayer2D
└── Camera2D
```

各节点的预期职责：

| 节点 | 后续用途 |
| --- | --- |
| `CharacterBody2D` | 接收输入、移动玩家并处理碰撞 |
| `AnimatedSprite2D` | 显示角色并播放待机、移动、攻击等动画 |
| `CollisionShape2D` | 定义玩家身体的碰撞范围 |
| `AudioStreamPlayer2D` | 播放脚步、攻击或受伤等位置音效 |
| `Camera2D` | 跟随玩家移动并显示周围场景 |

## 文件变化

- `my-demo/project.godot`：新增工程设置。
- `my-demo/main.tscn`：新增主场景和玩家节点结构。
- `my-demo/icon.svg`：新增默认项目图标。
- `my-demo/icon.svg.import`：新增图标导入配置。
- `my-demo/.editorconfig`：统一文本文件编辑格式。
- `my-demo/.gitattributes`：统一 Git 文本换行符。
- `my-demo/.gitignore`：忽略 `.godot/` 和 Android 构建目录。

## 验证结果

- Godot 能识别并打开项目。
- `main.tscn` 已配置为项目启动场景。
- 主场景包含玩家基础节点和 `Hello World` 标签。
- `.godot/` 编辑器缓存不会被提交到 Git。

## 当前限制

本次完成的是工程和场景结构。仓库中还没有 GDScript，因此玩家暂时不能移动；`AnimatedSprite2D` 和 `CollisionShape2D` 也尚未配置实际资源。当前场景用于验证项目结构，而不是完整的可玩 Demo。

## 下一步

下一次从玩家控制开始：

1. 在项目设置中添加上、下、左、右输入动作。
2. 为 `Player` 创建 GDScript。
3. 在 `_physics_process()` 中读取输入并调用 `move_and_slide()`。
4. 配置临时角色图像和碰撞形状。
5. 验证八方向移动速度保持一致。
