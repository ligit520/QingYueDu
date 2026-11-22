<div align="center">

<img src="docs/logo.png" width="128" alt="轻阅读"/>

# 轻阅读 QingYueDu

**基于 WinUI 3 的现代化 Windows 桌面小说阅读器**

支持 TXT / EPUB · 四种翻页方式 · 划词批注 · 自动翻页 · TTS 听书 · 全文搜索 · Legado 书源 · 微信读书风阅读统计 · 一键备份恢复 · 本地优先

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011-lightgrey)]()
[![.NET](https://img.shields.io/badge/.NET-8.0-blueviolet)]()

**[🐙 GitHub](https://github.com/ligit520/QingYueDu)**

</div>

---

## ✨ 功能特性

### 📖 多格式阅读
- **TXT**：自动编码检测（UTF-8 / GBK / GB18030 / Big5…）、智能章节切分（第 X 章 / 卷 / 楔子 / 番外…）
- **EPUB**：完整解析 OPF / spine，保留原书样式与图片，WebView2 高保真渲染
- 2348 章 / 22MB 的超大文件实测流畅

### 🎨 沉浸式阅读体验
- **四种翻页方式**：上下滚动 / 左右翻动 / 仿真翻页（3D 卷页）/ 覆盖翻页
- **双栏排版**：可与左右 / 仿真 / 覆盖模式自由组合
- **微信读书风设置面板**：背景色块、字体胶囊（按字体渲染预览）、A∓ 字号步进、行距 / 段距 / 字距档位
- **阅读主题**：白纸 / 羊皮纸 / 护眼绿 / 夜间，实时切换不丢位置
- **跨章连续滚动**：滚动到底自动加载下一章，1795 章大部头无卡顿
- **分页跨章续接**：左右翻动 / 仿真 / 覆盖模式翻到章尾时自动加载并接入下一章，无需手动点「下一章」

### 🔖 书签与批注
- 章节级书签，一键添加 / 移除 / 跳转
- **划词批注**：选中文字弹出浮层——四色高亮、笔记、复制；批注按字符偏移锚定，重启精确还原
- 批注列表面板统一管理

### 🗂 书库管理
- 单文件 / 文件夹批量导入
- 网格 / 列表双视图，搜索、排序
- **书架分组**：拖动封面到分组框即可归类（网格 / 列表均支持），支持批量选择与「最近阅读」「已读完」视图
- 书籍详情页：元数据、完整目录跳转、继续阅读
- 进度实时持久化，重开自动定位

### 🔊 听书与搜索
- **TTS 听书**：调用 Windows 系统语音，按句朗读，支持音色选择、朗读高亮、上一句 / 下一句跳转
- **全文搜索**：跨全书章节搜索，关键词高亮定位，点击结果直达命中处

### 🌐 在线书源（Legado 规则引擎）
- **内置书源**：内置多条笔趣阁等常用书源，开箱即用
- **书源管理**：URL / 文件 / 剪贴板三种导入方式，列表化管理，一键启用 / 停用 / 删除，支持多选全开 / 全关
- **可用性检测**：启动时自动检测已启用书源，导入后即时检测，也可在书源管理页手动检测，结果一目了然
- **书城**：跨已启用书源搜索书籍，结果展示目录章节数，点击直接在线阅读；左侧数据源面板展示 Z-Library 支持详情
- **在线书本地化**：加入书架即缓存详情与目录，自动逐章抓取正文存本地（`chapters/`），阅读优先读缓存、支持断点续传；封面自动下载到 `covers/`
- **搜索优化**：多源搜索竞态隔离、失败源自动重试、目录分页完整抓取（数千章不漏）

### 📊 阅读统计（仿微信读书）
- **周 / 月 / 年 / 总 / 阅历** 五种口径，可左右翻看历史周期，自动计算日均与环比涨跌
- 阅读时长大数字卡 + 四宫格（读过 / 读完 / 阅读天数 / 笔记）
- **柱状图**：周 7 根（周一~周日）、月每自然日一根、年每月一根，柱顶显示时长，带纵轴刻度与虚线网格
- **阅读日历**：GitHub 风全年热力图，按阅读时长分五档着色
- 阅读时自动计时并落盘到 `stats.json`，统计页每分钟刷新

### 💾 数据备份与恢复
- **一键备份**：设置页选择目录，自动生成含全部数据的 zip（书籍 / 进度 / 书签批注 / 统计 / 书源 / 在线缓存 / 封面）
- **从备份恢复**：二次确认 + 备份校验，恢复前自动留一份安全网备份
- 也支持命令行：`--backup-to:目录`、`--validate-backup:zip`、`--restore-test:zip;目录`
- 数据全部本地 JSON，与程序目录分离，升级不丢失

## 📸 截图

| 书架 | 阅读器 |
| --- | --- |
| ![书架](docs/screenshots/bookshelf.png) | ![阅读器](docs/screenshots/reader.png) |

| 排版自定义 | 全文搜索 |
| --- | --- |
| ![排版](docs/screenshots/typography.png) | ![搜索](docs/screenshots/search.png) |

| 目录面板 | TTS 听书 |
| --- | --- |
| ![目录](docs/screenshots/toc.png) | ![TTS](docs/screenshots/tts.png) |

| 书城 | 书源管理 |
| --- | --- |
| ![书城](docs/screenshots/bookstore.png) | ![书源管理](docs/screenshots/sources.png) |

| 设置 |
| --- |
| ![设置](docs/screenshots/settings.png) |

## 📥 下载安装

前往 [**Releases**](https://github.com/ligit520/QingYueDu/releases) 页面下载 `QingYueDu-vX.X.X-win-x64.zip`，解压后运行 `QingYueDu.exe` 即可。

> 无需安装 .NET，压缩包已自包含全部运行时。
> 系统要求：Windows 10 (17763+) 或 Windows 11 x64；EPUB 渲染依赖 WebView2（Win11 自带）。

## 🧱 技术栈

| | |
| --- | --- |
| UI 框架 | WinUI 3 (Windows App SDK 1.8) · Fluent Design · Mica |
| 架构 | MVVM (CommunityToolkit.Mvvm) |
| TXT 解析 | Ude.NetStandard 编码探测 + 正则章节切分 |
| EPUB 解析 | 自研 ZipArchive + OPF 解析器（零第三方依赖） |
| 渲染 | WebView2 统一渲染管线（TXT / EPUB 共用） |
| 书源引擎 | 自研 Legado 规则引擎（CSS 选择器 / XPath 子集） |
| 数据 | 本地 JSON（书库 / 进度 / 书签 / 批注 / 统计 / 设置）+ 章节缓存，不上传任何服务器 |
| 部署 | Unpackaged + 自包含运行时，解压即用 |

## 🗺 路线图

- [ ] PDF 支持
- [ ] AI 助手（OpenAI / Claude / Gemini）

## 🤝 贡献

欢迎 Issue 与 PR！开发前请阅读构建说明；提交请附带复现步骤。

## 📄 许可证

[MIT](LICENSE) —— 数据完全存储在本地，不上传任何服务器。
