# PersonlGameProject

一款由个人开发的俯视角 2D 像素动作游戏。目前使用 Godot 4 和 GDScript，项目处于基础学习与原型搭建阶段。

## 当前进度

- 完成首个 Godot 4 工程的创建与基础配置。
- 创建主场景 `main.tscn`，并设置为启动场景。
- 建立玩家基础节点结构：`CharacterBody2D`、`AnimatedSprite2D`、`CollisionShape2D`、`AudioStreamPlayer2D` 和 `Camera2D`。
- 添加 `Hello World` 标签，用于确认场景可以正常显示。
- 配置适合 2D 项目的画面拉伸方式和 Mobile 渲染器。

当前版本尚未加入 GDScript、玩家移动、动画、碰撞形状和战斗逻辑。

## 运行项目

1. 安装 Godot 4.7 或兼容的 Godot 4.x 版本。
2. 在 Godot 项目管理器中导入 `my-demo/project.godot`。
3. 打开项目并运行主场景。

## 开发文档

- [项目开发总结](docs/DEVELOPMENT_SUMMARY.md)
- [开发记录索引](docs/development-log/README.md)
- [第 1 次记录：首个 Godot Demo](docs/development-log/2026-09-18-first-godot-demo.md)

## 下一步

- 为玩家创建脚本并实现八方向移动。
- 设置玩家碰撞形状。
- 添加临时角色图像和待机、移动动画。
- 创建一个可阻挡玩家的小型测试场景。
