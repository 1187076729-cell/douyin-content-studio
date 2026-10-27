# 灵感引力：抖音视频内容生成器

本项目是一个无需后端、无需 API Key 的单页面创作工具，用原生 HTML + Tailwind CSS CDN + JavaScript 实现，适合直接用 PyCharm 打开测试，或部署在 GitHub Pages。

## 快速启动

1. 用 Chrome / Edge 双击打开 `index.html`。
2. 如想使用 PyCharm：`File > Open` 选择此文件夹，在项目树右键 `index.html` 选择 `Open in Browser`。
3. 需要联网才能加载 Tailwind CDN；页面附带关键样式 CSS，离线时基本界面仍可使用。

## 功能

- 身份、赛道标签、创作方向：多选 / 自定义添加
- 自由输入生活素材，自动暂存在浏览器 `localStorage`
- 四个可调的增长优化权重
- 模拟生成标题、前三秒钩子、5 镜头拍摄清单、拍摄标准、BGM、剪辑字幕、封面与互动引导
- 多次生成不同版本、全量复制、下载 Markdown、打印 / PDF、清空草稿
- 响应式布局，支持电脑、手机

## 重要说明

“生成”使用本地模板与规则引擎，不调用真正的 AI；不会自行联网传输用户素材，也不保证获得流量。若要升级真实大模型，建议新增 Python/FastAPI 后端，由后端保管 API Key，切勿把密钥写在前端 HTML 中。

## GitHub Pages

新建 GitHub 仓库后上传 `index.html` 与 `README.md`，在仓库 `Settings > Pages > Build and deployment` 选 `Deploy from a branch`，选择 `main` 和 `/(root)`，保存。仓库需要允许 GitHub Pages 发布，并根据 Pages 页面给出的 URL 访问。

## 给 Codex 的下一阶段任务

请在保留当前全部交互与视觉设计的前提下，把项目改造成前后端分离的真实生成版本：前端继续使用 HTML/Tailwind CSS，后端用 Python FastAPI 代理大模型请求；API Key 仅从后端环境变量读取。新增生成状态、超时重试、错误提示、模板保存、JSON/Markdown 导出与测试；给出本地运行步骤与 `.env.example`，确保密钥不会提交到 Git。
