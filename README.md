<div align="center">

# 卡易 PPT 生成 Skill

<p>
  <img src="https://img.shields.io/badge/卡易-PPT_Skill-1770EA?style=flat-square" alt="Kayi PPT Skill">
  <img src="https://img.shields.io/badge/Claude_Code-支持-432391?style=flat-square&logo=anthropic" alt="Claude Code">
  <img src="https://img.shields.io/github/license/Chaunceycehn/Kayi-PPT-Skill?style=flat-square" alt="License">
</p>

**将文字、大纲、文档一键转换为卡易官方风格 `.pptx` 幻灯片**

完全复现浙江卡易智慧医疗科技有限公司 2026 版官方模板设计语言 · 支持 18 种版式 · 内嵌官方背景与 Logo · 零配置可用

</div>

---

## ✨ 核心能力

| 能力 | 说明 |
|------|------|
| 🎨 **官方设计还原** | 品牌色 `#1770EA` · 字体 · Logo · 背景图完全对齐 2026 版官方模板 |
| 🧠 **思维模型识别** | 自动识别内容结构，匹配金字塔、SWOT、PDCA、黄金圈、5W1H、SCQA 等 6 种思维框架 |
| 📐 **18 种智能版式** | 封面、目录、章节页、要点列表、数据卡片、Bento Grid、架构图、时间轴…… |
| 📄 **多格式输入** | Markdown · 文本大纲 · Word 文档 · 直接粘贴内容均可 |
| 🖼️ **图片占位符** | 自动生成占位框，方便后续插入截图、图表 |
| 🔐 **保密标识** | 自动添加「④ 内部公开 请勿外传」水印标识 |
| ✅ **视觉 QA** | 生成后自动转图检查，对齐问题自动修复再交付 |

---

## 🚀 快速开始

### 安装方法

```bash
# 进入 Claude Code 的 skills 目录
cd ~/.claude/skills/

# 克隆仓库
git clone https://github.com/Chaunceycehn/Kayi-PPT-Skill.git kayi-ppt

# 重启 Claude Code 即可生效
```

### 验证安装

打开 Claude Code，输入：

```
帮我做个卡易 PPT
```

若 Claude 开始询问场景和页数，说明 Skill 已成功加载 ✅

---

## 💬 使用示例

### 基础用法

```
帮我把以下内容做成卡易风格的汇报材料：

## 2026 年医疗影像云平台建设进展
- 已上线医院数量：156 家
- 活跃合作伙伴：48 家
- 平台调用量：月均 32 万次

## 下一步计划
- Q2 启动区域扩展计划
- 引入 AI 辅助诊断模块
```

### 进阶用法

```
将以下内容转换为卡易风格 PPT，要求：
- 场景：伙伴赋能
- 页数：中等（10-15 页）
- 图片：保留占位符

[粘贴你的文档内容]
```

### 触发词

> `做PPT` · `做个PPT` · `卡易PPT` · `卡易模板` · `生成幻灯片` · `汇报材料` · `演示文稿` · `生成deck` · `输出PPT`

---

## 🎬 工作流

```
┌─────────────────────────────────────────────────────────┐
│  第零阶段  思维模型识别                                    │
│    扫描内容结构信号，自动匹配最合适的版式框架                 │
├─────────────────────────────────────────────────────────┤
│  第一阶段  内容发现                                        │
│    询问场景 / 页数 / 图片处理方式 → 生成大纲 → 用户确认       │
├─────────────────────────────────────────────────────────┤
│  第二阶段  内容脚本                                        │
│    输出逐页内容脚本（含版式排布指令）→ 用户审阅定稿            │
├─────────────────────────────────────────────────────────┤
│  第三阶段  生成交付                                        │
│    生成 Node.js 脚本 → 执行 → 转图 QA → 修复 → 交付 .pptx  │
└─────────────────────────────────────────────────────────┘
```

---

## 🗂️ 支持场景

| 场景 | 典型用途 | 建议页数 |
|------|---------|---------|
| **内部汇报** | 向上级汇报工作进展、述职 | 短（5-10 页） |
| **伙伴赋能** | ISV / OEM / 开发者培训材料 | 中（10-20 页） |
| **客户大会** | 对外客户演示、合作发布 | 中（10-20 页） |
| **方案提案** | 项目立项、解决方案建议书 | 长（20 页+） |

---

## 🎨 支持版式

### 标准版式（12 种）
封面页 · 目录页 · 章节分隔页 · 要点列表 · 数据卡片 · 左右对比 · 横向流程 · 纵向流程 · 图文并排 · 时间轴 · 引用语录 · 结尾致谢

### 思维模型版式（6 种）
金字塔 / MECE · PDCA · SWOT · 黄金圈 · 5W1H · SCQA

### 高级版式（6 种）
数据看板 · Bento Grid · 架构生态 · 核心特性卡片 · 分层矩阵 · 金句页 · 图文沉浸 · 超大焦点页

---

## 📁 仓库结构

```
kayi-ppt/
├── SKILL.md               # Skill 主配置（触发规则 + 完整工作流）
├── style-guide.md         # 卡易品牌视觉规范（颜色、字体、坐标、Logo）
├── layout-presets.md      # 18 种版式 PptxGenJS 代码模板
├── pptx-builder.md        # 技术构建文档（QA 规范、常见陷阱）
├── README.md              # 本文件
├── LICENSE                # MIT 许可证
├── Changelog              # 更新日志
└── assets/                # 内嵌资源文件
    ├── bg_cover.png           # 封面背景
    ├── bg_toc.png             # 目录页背景
    ├── bg_section_a.png       # 章节页背景 A
    ├── bg_section_b.png       # 章节页背景 B
    ├── bg_section_c.png       # 章节页背景 C
    ├── bg_closing.png         # 结尾页背景
    ├── closing_thanks.png     # 多语言致谢图
    ├── logo_color.png         # 卡易彩色 Logo
    └── logo_white.png         # 卡易反白 Logo
```

---

## ❓ 常见问题

<details>
<summary><b>Q1：生成的 PPT 可以在 PowerPoint / WPS 中编辑吗？</b></summary>

可以。输出的 `.pptx` 完全兼容 Microsoft PowerPoint、WPS Office、Apple Keynote 等主流软件，所有文本、形状均可二次编辑。
</details>

<details>
<summary><b>Q2：图片占位符怎么替换？</b></summary>

打开 PPT 后，点击占位框，使用软件的「插入图片」功能替换即可。占位框已标注建议尺寸和内容描述。
</details>

<details>
<summary><b>Q3：如何更新 Skill 到最新版本？</b></summary>

```bash
cd ~/.claude/skills/kayi-ppt
git pull origin main
# 重启 Claude Code 生效
```
</details>

---

## 📄 许可证

[MIT License](LICENSE) © 2026 浙江卡易智慧医疗科技有限公司
