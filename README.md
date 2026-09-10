<div align="center">
  <img src="assets/luxi-lab-main.svg" width="64" height="64" alt="鹿溪联合创新实验室 LUXI LAB" />
</div>

<h1 align="center">鹿溪设计范式 · LUXI Design System</h1>

<p align="center">
  <strong>林深见鹿，源启清溪</strong><br/>
  <em>Deep Insights, Evolutionary Origin.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Product-鹿溪设计范式-0D5E42" alt="product" />
  <img src="https://img.shields.io/badge/Lab-鹿溪联合创新实验室-047538" alt="lab" />
  <img src="https://img.shields.io/badge/Scope-交互%20%C2%B7%20视觉%20%C2%B7%20组件-6366f1" alt="scope" />
  <img src="https://img.shields.io/badge/Consumers-OpenDesign%20%7C%20Agent%20%7C%20Frontend-blue" alt="consumers" />
  <img src="https://img.shields.io/badge/Version-v1.0-f1c40f" alt="version" />
</p>

<p align="center">
  <b>鹿溪联合创新实验室</b>（LUXI Joint Innovation Lab）出品<br/>
  仓库：<a href="https://github.com/itrilogy/LUCY-DESIGN">itrilogy/LUCY-DESIGN</a>
</p>

---

把实验室 12 个产品的既有视觉与交互实践，收敛为**一套可执行的统一设计范式**——供生成式设计工具（OpenDesign）、AI Agent 与前端工程共同消费，避免"每个产品一套色、一套圆角"的漂移。

## 🧱 三层交付

| 文件 | 角色 | 消费方式 |
| :--- | :--- | :--- |
| **[DESIGN.md](./DESIGN.md)** | 叙事规范：原则、禁令、组件与页面骨架 | 人读规范；工具侧可作 prompt 前缀 / RAG 语料 |
| **[tokens.css](./tokens.css)** | 可执行层：CSS 变量 + 三主题 + 产品 accent | 前端直接 `<link>`，`data-theme` / `data-product` / `data-density` 驱动 |
| **[tokens.json](./tokens.json)** | 结构化层：设计 tokens 全量数据 | 设计工具导入变量；代码生成读取 schema |

## 🚀 快速使用

```html
<!-- 1. 引入 tokens（亮主题为默认） -->
<link rel="stylesheet" href="tokens.css" />

<!-- 2. 通过属性驱动主题 / 产品 accent / 密度 -->
<html data-product="hengliu" data-theme="dark" data-density="compact">
```

```css
/* 3. 组件直接消费语义变量，不写游离色值 */
.card {
  background: var(--bg-card);
  border: 1px solid var(--border-line);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-sm);
  padding: var(--space-6);
}
.button--primary {
  background: var(--color-primary);
  color: var(--text-inverse);
  height: 36px;
  border-radius: var(--radius-sm);
}
.button--primary:hover { background: var(--color-primary-hover); }
:focus-visible { outline: 2px solid var(--color-accent); outline-offset: 2px; }
```

## 🎨 品牌基石

| Token | 色值 | 用途 |
| :--- | :--- | :--- |
| 鹿溪绿 | `#0D5E42` | 主底色、品牌识别、primary 按钮 |
| 源启白 | `#F5F7FA` | 画布背景、面板反白 |
| 进化蓝 | `#00D2FF` | 溪流、源启星、数据高亮、焦点环 |
| 标题金 | `#F1C40F` | 落点、显著信号、命中热区 |

**三主题**：`light`（工作台/报表/文档）· `dark`（数据/推理界面）· `ink`（播放/展示沉浸页）。
**产品 accent**：见 `tokens.json → color.product`（12 产品各自 accent 与意象，如衡流蓝 `#60A5FA`、审微青 `#2F7A73`、观澜红蓝 `#E74C3C`/`#3498DB`、聆涧暖米 `#E8D4B0`）。

## 📁 项目结构

```
LUCY-DESIGN/
├── README.md                     # 本文件（对外说明）
├── DESIGN.md                     # 设计范式正文（原则 · 组件 · 页面骨架 · 生成指引）
├── tokens.css                    # CSS 变量：core / semantic / theme / product accent / 基线
├── tokens.json                   # 结构化设计 tokens（W3C 风格）
└── assets/
    ├── luxi-lab-main.svg         # 官方 LUXI LAB 主标（单向拷贝自 Obsidian 权威源）
    └── luxi-lab-main-512.png     # 主标 512×512 交付版
```

## 📚 文档

| 文档 | 内容 |
| :--- | :--- |
| [DESIGN.md](./DESIGN.md) | **完整范式**：品牌基石 · L-U-X-I 设计法则 · 色彩/字体/空间 · 组件规范 · 交互五铁律 · 动效预算 · 12 产品差异化矩阵 · 四类页面骨架 · OpenDesign 生成指引与自检清单 |
| [tokens.css](./tokens.css) | 主题与变量实现 |
| [tokens.json](./tokens.json) | tokens 数据（含产品 accent 与意象） |

## 🏛 权威源约定

- **实验室主标**唯一权威源：`Obsidian departments/lab/鹿溪联合实验室/LUXI LAB.svg`；本仓库 `assets/luxi-lab-main.svg` 为单向拷贝，**不得在工程侧修改主标**
- **产品方标**规范：512 视口 · 鹿溪绿圆角砖（rx=112）+ 业务图形 + 进化蓝 S 形溪流 + 源启星
- 各产品自有品牌资产位于其仓库品牌目录（如 `static/brand/`、`public/brand/`）

## 📄 版本策略

`v1.x` 仅新增 token 与组件（向后兼容）；`v2.0` 才可变更 core 四色与设计原则。变更需同步更新三层文件及各产品引用。

---

<div align="center">
  <img src="assets/luxi-lab-main.svg" width="48" height="48" alt="LUXI LAB" />
  <p><strong>鹿溪设计范式 · LUXI Design System</strong> · 林深见鹿，源启清溪</p>
  <p>© 鹿溪联合创新实验室 · LUXI Joint Innovation Lab</p>
  <p><em>Deep Insights, Evolutionary Origin.</em></p>
</div>
