# VisionKit

VisionKit 是一个基于 Web 技术的**多功能前端集成工具箱**，旨在为开发者和内容创作者提供便捷的在线工具集合。

本项目采用无构建（No-Build）架构，直接通过 CDN 引入 Vue 3 与 Arco Design Web Vue，无需配置复杂的开发环境，开箱即用。

## 🛠 功能模块

VisionKit 包含以下核心工具：

### 📺 媒体与播放器
- **VePlayer 标准模式** (`ve_standard.html`): 全功能视频播放器，提供沉浸式暗色体验，支持 URL 参数快速播放。
- **VePlayer 极简模式** (`ve_no_controls.html`): 无控制栏的纯净播放器，适用于背景视频或特殊展示场景。
- **VePlayer 嵌入生成器** (`ve_generator.html`): 可视化生成 VePlayer 初始化代码，支持自定义配置。
- **YouTube 嵌入生成器** (`youtube_tool.html`): 生成带有高级参数配置的 YouTube iframe 代码。
- **综合媒体导航** (`media_navigation.html`): 整合多平台媒体资源，支持一键播放。

### 🔧 实用开发工具
- **DoH DNS 查询工具** (`dns_tool.html`): 支持 Cloudflare (1.1.1.1)、阿里云 (AliDNS)、腾讯云 (DNSPod) 的 DNS over HTTPS 查询工具，支持多种记录类型（A, AAAA, CNAME, MX 等）。
- **通用 Iframe 生成器** (`iframe_generator.html`): 生成高度可定制的 Iframe 嵌入代码，支持全屏、沙箱权限等高级属性设置。
- **JSON 配置编辑器** (`json_editor.html`): 可视化编辑和管理 JSON 配置数据。

### 📄 文档预览
- **Office 在线预览助手** (`office_viewer.html`): 快速预览 Word, Excel, PPT 等 Office 文档。

## 🚀 技术栈

- **核心框架**: [Vue 3](https://vuejs.org/) (Global Build via CDN)
- **UI 组件库**: [Arco Design](https://arco.design/) (Web Vue)
- **样式工具**: [Tailwind CSS](https://tailwindcss.com/)
- **播放器内核**: Volcengine VePlayer SDK

## 📦 安装与使用

由于本项目采用无构建架构，您无需安装 Node.js 或运行 `npm install`。

1. **下载或克隆项目**到本地。
2. 使用本地 HTTP 服务打开项目（推荐），再访问 `index.html` 进入工具箱主页。
3. 点击主页上的卡片即可跳转到相应的工具页面。

### 快速预览 (VS Code)

如果您使用 VS Code，推荐安装 "Live Server" 插件：
1. 右键点击 `index.html`。
2. 选择 "Open with Live Server"。

### 注意事项

- `media_navigation.html` 通过 `fetch('Veplayer_live_list_m3u8.json')` 读取播放列表数据，若直接以 `file://` 方式打开页面，浏览器通常会阻止读取本地 JSON 文件，请务必使用本地 HTTP 服务。

## 📝 目录结构

```text
VisionKit/
├── index.html                  # 项目入口/主页
├── dns_tool.html               # DNS 查询工具
├── iframe_generator.html       # Iframe 生成器
├── json_editor.html            # JSON 编辑器
├── media_navigation.html       # 媒体导航
├── office_viewer.html          # Office 文档预览
├── ve_generator.html           # VePlayer 代码生成器
├── ve_standard.html            # VePlayer 标准播放器
├── ve_no_controls.html         # VePlayer 极简播放器
├── youtube_tool.html           # YouTube 工具
├── Veplayer_live_list_m3u8.json # 媒体列表数据示例
└── ...
```

## 📄 许可证

本项目开源，欢迎学习与交流。
