# PersonlGameProject

一款由个人开发的俯视角 2D 像素动作游戏。目前使用 Godot 4 和 GDScript，项目处于基础学习与原型搭建阶段。

## 当前进度

- 完成首个 Godot 4 工程的创建与基础配置。
- 创建主场景 `main.tscn`，并设置为启动场景。
- 建立玩家基础节点结构：`CharacterBody2D`、`AnimatedSprite2D`、`CollisionShape2D`、`AudioStreamPlayer2D` 和 `Camera2D`。
- 添加 `Hello World` 标签，用于确认场景可以正常显示。
- 配置适合 2D 项目的画面拉伸方式和 Mobile 渲染器。
- 新建官方教程“你的第一个 2D 游戏”工程 `first-2d-game-demo`。
- 导入玩家、三类敌人、背景音乐、结束音效和 Xolonium 字体素材。

当前版本已完成新教程工程和素材准备，尚未加入 GDScript、玩家移动、敌人生成和游戏循环。

## 运行项目

1. 安装 Godot 4.7 或兼容的 Godot 4.x 版本。
2. 在 Godot 项目管理器中导入 `first-2d-game-demo/project.godot`。
3. 打开项目，继续官方“你的第一个 2D 游戏”教程。

早期节点练习工程保留在 `my-demo/`。

## 开发文档

- [项目开发总结](docs/DEVELOPMENT_SUMMARY.md)
- [开发记录索引](docs/development-log/README.md)
- [第 2 次记录：创建第一个 2D 游戏工程并导入素材](docs/development-log/2026-09-18-first-2d-game-project-setup.md)

## 下一步

- 创建玩家场景并配置精灵动画。
- 为玩家添加碰撞形状和输入动作。
- 编写玩家移动脚本。
- 创建敌人场景和随机生成逻辑。
