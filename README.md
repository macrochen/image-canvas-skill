# image-canvas-skill

打开一个用于粘贴、拖拽和排列图片/文字贴纸的灵感画布页面。支持“打开画布”、“启动灵感画布”等指令。

## Installation

This is a skill for [Gemini CLI](https://github.com/google/gemini-cli).

To install this skill:

1. Clone this repository.
2. Run the install command:

```bash
gemini skills install ./image-canvas-skill
```

## Documentation

# 灵感画布 (Image Canvas)

这个 Skill 提供了一个极其简单的单页面应用，用于快速收集和排列视觉灵感。

## 核心功能

- **粘贴支持**：支持从剪贴板直接粘贴 (Cmd/Ctrl + V) 图片和文字。
- **自由布局**：所有粘贴的内容都可以通过鼠标自由拖拽。
- **等比例缩放**：图片提供左上角和右下角的缩放手柄。
- **清空功能**：一键清空画布。

## 使用指南

当用户请求打开画布时，你需要定位到该 Skill 目录下的 `assets/image_canvas.html` 文件，并使用 `open` 命令在浏览器中打开它。

### 操作步骤

1. 获取当前 Skill 的绝对路径。
2. 找到 `assets/image_canvas.html`。
3. 执行 `run_shell_command` 调用 `open <path_to_html>`。

## 注意事项

- 这是一个静态页面，不保存数据，刷新后内容会清空（除非用户手动保存页面）。
- 仅在本地 Chrome 浏览器环境下测试通过。
