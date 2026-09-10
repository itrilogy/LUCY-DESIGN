<div align="center">
  <img src="assets/luxi-lab-main.svg" width="64" height="64" alt="鹿溪联合创新实验室 LUXI LAB" />
</div>

<h1 align="center">鹿溪设计范式 · LUXI Design System</h1>

<p align="center">
  <strong>林深见鹿，源启清溪</strong><br/>
  <em>Deep Insights, Evolutionary Origin.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Matrix-四大矩阵-0D5E42" alt="matrix" />
  <img src="https://img.shields.io/badge/Scope-交互%20%C2%B7%20视觉%20%C2%B7%20组件-0D5E42" alt="scope" />
  <img src="https://img.shields.io/badge/Lab-鹿溪联合创新实验室-047538" alt="lab" />
  <img src="https://img.shields.io/badge/Consumers-OpenDesign%20%7C%20Agent%20%7C%20Frontend-6366f1" alt="consumers" />
  <img src="https://img.shields.io/badge/Version-v1.0-f1c40f" alt="version" />
</p>

<p align="center">
  <b>鹿溪联合创新实验室</b>（LUXI Joint Innovation Lab）出品<br/>
  仓库：<a href="https://github.com/itrilogy/LUCY-DESIGN">itrilogy/LUCY-DESIGN</a>
</p>

---

# 0. 这份文档是什么

**用途**：把实验室 12 个产品的既有视觉/交互实践收敛为一套**可执行的统一范式**，供三类读者消费：

| 读者 | 用法 |
| :--- | :--- |
| **OpenDesign / 生成式设计工具** | 作为设计约束与词汇表，生成符合品牌的产品界面与营销物料 |
| **AI Agent（编码 / 设计）** | 作为硬约束清单，产出直接可用的页面与组件代码 |
| **人类设计师 / 前端工程师** | 作为决策依据，避免"每个产品一套色、一套圆角"的漂移 |

**三层交付**：

```
DESIGN.md     ← 叙事规范（为什么这样做、禁止什么）      ← 本文件
tokens.css    ← 可执行层（CSS 变量 + 主题 + 产品 accent）
tokens.json   ← 结构化层（供工具读取、代码生成、设计同步）
```

**硬约束优先级**：`core 品牌色/主标` > `本文件的原则与禁令` > `产品 accent` > `页面局部自由`。

---

# 1. 品牌基石

## 1.1 身份

| 项 | 内容 |
| :--- | :--- |
| 中文全称 | 鹿溪联合创新实验室 |
| 英文全称 | LUXI Joint Innovation Lab |
| 品牌代号 | **LUXI** = Lucy（始祖/进化）+ Lucky（幸运/价值）+ Xi/Stream（鹿溪/本土生态） |
| 主标语 | **林深见鹿，源启清溪**（Deep Insights, Evolutionary Origin.） |
| 使命 | 在复杂中看见价值，在流动中定义未来 |
| 愿景 | 构建空地一体、虚实共生的行业进化母体 |

## 1.2 产品矩阵（谁在用什么 accent）

```
知行·三动（感官交互）  见鹿 JianLu · 听默 Tingmo · 绘流 HuiLiu · 聆涧 LingJian
具身·二察（具身感知）  脉息 MaiXi · 审微 ShenWei
理数·三思（数理推演）  问津 WenJin · 衡流 HengLiu · 观澜 GuanLan
工坊·一法（专业工程）  澄矩 ChengJu · 溯知 SuZhi
```

| 产品 | 英文/代号 | Slogan | accent | 意象（方标语义） |
| :--- | :--- | :--- | :--- | :--- |
| 见鹿 | JianLu | 指间林深，心澄见鹿 | `#0D5E42` | 键帽 + 光标 + 溪流 |
| 听默 | Tingmo | 谛听万籁，默化成文 | `#0D5E42` | 声纹弧 + 溪流 |
| 绘流 | HuiLiu (VectorStream) | 引线定锚，聚迹成流 | `#0D5E42` / `#F1C40F` | 贝塞尔锚点 + 导出落点 |
| 聆涧 | LingJian (VoiceStream) | 耳畔清涧，一字生境 | `#E8D4B0` | 山涧 + 一字生境 |
| 脉息 | MaiXi (PulseStream) | 光映微澜，脉息自明 | `#00D2FF` | 同心环 + 脉搏波 |
| 审微 | ShenWei (SafeSpot) | 察于至微，防于未萌 | `#2F7A73` | 光学分划 + 隐患点 |
| 问津 | WenJin | 向道问津，顺溪成程 | `#0D5E42` | 双枝航道 + 落点 |
| 衡流 | HengLiu (QuantFlow) | 审度称衡，守正观流 | `#60A5FA` | 马尔可夫环 + K线 |
| 观澜 | GuanLan | 观水有术，由表及澜 | `#E74C3C` / `#3498DB` | 红蓝球 + 市场曲线 |
| 澄矩 | ChengJu (IQS) | 源清流澈，行止应矩 | `#0D5E42` | 控制限 + 正交走线 |
| 溯知 | SuZhi (STORM) | 溯流求源，知汇成章 | `#0D5E42` | 三信源汇流 + 成章 |
| 听默 Android | Tingmo Android | 听而有迹，默而成文 | `#0D5E42` | 声纹弧 |

## 1.3 标识双层结构（不可混用）

```
产品层（表达业务域）        实验室层（表达出品方）
favicon / mark / logo  →    luxi-lab-main.svg ← 官方 LUXI LAB.svg
鹿溪绿圆角砖 + 业务图形       唯一权威源：Obsidian departments/lab/鹿溪联合实验室/LUXI LAB.svg
+ 进化蓝 S 形溪流 + 源启星    工程内单向拷贝，命名 luxi-lab-main.svg
```

**禁令**：
- ❌ 不得修改实验室主标；不得用几何实验稿（听默 Y+L）充当主标
- ❌ 产品方标不得复用其他产品的业务图形
- ❌ README / 界面中产品标与主标**必须并排等大**（`64×64` 或 `48×48`），不得一大一小

---

# 2. 设计原则（L-U-X-I 法则 → 设计过滤器）

任何界面决策，先过这四问：

| 法则 | 设计含义 | 具体表现 |
| :--- | :--- | :--- |
| **L**ink 连接 | 界面连接"空与地、业务与技术" | 数据与操作同屏；不把用户丢到空白页；空状态给下一步 |
| **U**nveil 揭示 | 拨开迷雾，揭示数据真相 | 关键指标第一眼可见；图表可解释（标注口径/边界）；不美化随机性 |
| **X**-Factor 变量 | 拥抱不确定性 | 预测/推荐类必须标注置信度与边界；禁止把模型输出包装成事实 |
| **I**terate 迭代 | 小步快跑，自我革新 | 组件可组合、可替换；范式提供"可调档位"（密度/主题/accent）而非死板模板 |

**三条贯穿始终的表现原则**：

1. **克制（Restraint）**——界面密度服务于任务，不服务于炫技。工具类产品**不做 DAW 式密集控制台**；默认隐藏高级控件，Shift/展开再露出。
2. **诚实（Honesty）**——概率不是承诺，模型不是真相，示例数据必须标注。产品自查声明（如观澜"非中奖预言"）属于设计的一部分，不是法律附件。
3. **可退（Reversible）**——破坏性操作可撤销（`.bak`、撤销栈、二次确认）；首次运行风险门（素材授权/密钥/外发数据）**必须显式确认**。

---

# 3. 色彩系统

## 3.1 四色 Tokens（不可覆写）

| Token | 色值 | 用途 |
| :--- | :--- | :--- |
| **鹿溪绿** `--luxi-green` | `#0D5E42` | 主底色、品牌识别、稳重底座、primary 按钮 |
| **源启白** `--origin-white` | `#F5F7FA` | 画布背景、面板反白、纯净留白 |
| **进化蓝** `--luxi-cyan` | `#00D2FF` | 溪流曲线、源启星、数据高亮、focus ring |
| **标题金** `--luxi-gold` | `#F1C40F` | 落点、显著信号、命中热区、警示替代 |

## 3.2 语义层与状态色

| 组 | Token | 值 | 用途 |
| :--- | :--- | :--- | :--- |
| 文本 | `--text-primary` / `--text-muted` | `#1A2428` / `#64748B` | 正文 / 辅助 |
| 表面 | `--bg-page` / `--bg-card` / `--bg-raised` | `#FFFFFF` / `#F5F7FA` / `#FFFFFF` | 页面 / 卡片 / 浮层 |
| 描边 | `--border-subtle` / `--border-line` / `--border-strong` | 绿 10% / 18% / 32% | 分割 / 常规 / 选中 |
| 状态 | `--state-up` / `--state-down` / `--state-flat` | `#22C55E` / `#EF4444` / `#94A3B8` | 数据语境涨跌平 |
| 业务 | `--alert-red` / `--info-blue` | `#E74C3C` / `#3498DB` | 警示 / 次级信息 |

## 3.3 主题（三套，均由 tokens.css 提供）

| 主题 | 触发 | 适用 | 依据 |
| :--- | :--- | :--- | :--- |
| **亮（默认）** | 无属性 | 工作台、报表、文档、营销页 | 澄矩 · 审微 · 问津 · 溯知 |
| **深色 `dark`** | `data-theme="dark"` | 长时间数据/推理界面 | 衡流 · 脉息 · 听默 · 绘流 |
| **沉浸 `ink`** | `data-theme="ink"` | 播放/展示型全屏页 | 聆涧（纯黑 `#0B0C0E` + 暖字 `#F3EEE6` + 衬线） |

**规则**：主题只切换 semantic 层，`core` 四色不变；深色界面必须把鹿溪绿提亮到 `#14805C`（`--color-primary`）以保证对比度 ≥ 4.5:1。

## 3.4 产品 accent 使用规范

- **允许**：强调元素、图表主序列、标签、进度、产品标识周边光晕
- **禁止**：替换 primary 按钮色（工具类产品 primary 恒为鹿溪绿）、替换四色品牌职能、在同屏并列多个产品 accent
- **回退**：`--product-accent` 缺省 = `--luxi-green`

---

# 4. 字体排印

## 4.1 字族

```css
--font-sans-zh:  "PingFang SC", "HarmonyOS Sans SC", "Microsoft YaHei", "Noto Sans SC", system-ui, sans-serif;
--font-serif-zh: "Songti SC", "Source Han Serif SC", "Noto Serif SC", Georgia, serif;
--font-mono:     "JetBrains Mono", "SF Mono", Menlo, Consolas, monospace;
```

**中文优先（Chinese-first）**：默认 `sans-zh`；`ink` 主题与文学性文案切 `serif-zh`；代码/DSL/数字列一律 `mono`（数字对齐）。

## 4.2 字号阶梯

| class | size / line-height | 用途 |
| :--- | :--- | :--- |
| `display` | 40 / 1.15 | 营销页主标 |
| `h1` | 28 / 1.25 | 页面标题 |
| `h2` | 22 / 1.3 | 区块标题 |
| `h3` | 17 / 1.4 | 卡片标题 |
| `body` | **14 / 1.6** | 正文（默认） |
| `small` | 13 / 1.5 | 次级信息 |
| `caption` | 12 / 1.45 | 说明 / 表注 |
| `micro` | 11 / 1.4 | 角标 / 时间戳 |

**字距**：大标题 `-0.02em`；品牌字距（Slogan / 章节眉）`0.18em` 且配大写或加空格。
**数字**：数据界面启用 `font-variant-numeric: tabular-nums`。

---

# 5. 空间 · 圆角 · 阴影

- **基准 4px**：所有间距取 4 的整数倍（`4/8/12/16/20/24/32/40/48/64/80`）
- **圆角**：`xs 4` 输入 / `sm 6` 按钮 / `md 10` 卡片（默认）/ `lg 16` 大面板 / `pill` 胶囊 / `tile 12` 产品砖
  - 兼容既有实现：Streamlit（衡流）沿用 `4–6px`；毛玻璃（绘流）用 `md/lg`
- **阴影**：仅 5 档（`xs/sm/md/lg/focus`）；浮层用 `md`，模态用 `lg`，键盘焦点用 `focus`（`0 0 0 3px rgba(0,210,255,.35)`，**全局必须可见**）
- **玻璃质感**（绘流范式）：`--gradient-glass` + `--shadow-glass` + `backdrop-filter: blur(16px) saturate(140%)`；**仅用于浮层/顶栏**，不用于正文卡片

---

# 6. 组件规范

## 6.1 控件尺寸

| 档 | 高度 | 场景 |
| :--- | :--- | :--- |
| `sm` | 28px | 表格内联操作、标签页 |
| `md` | 36px | 默认按钮 / 输入 |
| `lg` | 44px | 主行动（提交 / 开始） |

描边统一 `1px`；选中态用**颜色**而非加粗；禁用态 `opacity: .38` + `cursor: not-allowed`。

## 6.2 按钮层级（全产品统一）

| 层级 | 样式 | 用途 | 限制 |
| :--- | :--- | :--- | :--- |
| **Primary** | 鹿溪绿实底 + 白字 | 页面唯一主行动 | 每屏 ≤ 1 个 |
| **Secondary** | 描边 + 绿字 | 次行动 | 可多个 |
| **Ghost** | 无底无框，hover 出浅底 | 工具条 / 行内 | — |
| **Danger** | `--alert-red`，需二次确认 | 删除 / 覆盖 | 必须可撤销 |
| **Capsule** | `radius: pill`，用于标签/切换 | 场景切换 | 与 immersive 页搭配 |

## 6.3 必备组件清单（生成时必须覆盖）

`按钮` · `输入/选择/多选` · `卡片` · `表格（含空状态/加载/错误）` · `标签 Tag` · `提示 Toast` · `对话框（含破坏性确认）` · `抽屉/侧栏 240px` · `顶栏 56px` · `标签页` · `进度（线/环）` · `图表容器（含口径脚注）` · `首次运行法律/风险门` · `空状态（一句话 + 下一步）`

## 6.4 图表规范（澄矩 / 衡流 / 观澜 / 脉息 共用）

- **主序列**用产品 accent，次序列用 `--info-blue` / `--state-flat`
- **必须**渲染口径脚注（数据来源 / 时间范围 / 置信度或样本量）
- 颜色语义固定：涨 `--state-up`、跌 `--state-down`、持平 `--state-flat`
- 网格线 `--border-subtle`；**禁止**3D 效果、渐变阴影填充（除面积图 ≤ 0.45 alpha）
- 打印/导出走 `@media print` 白底黑字，字重降一档

---

# 7. 交互范式

## 7.1 五条铁律

1. **三态齐全**——每个数据区必须设计 `加载 / 空 / 错误` 三态；空状态给"下一步"动作
2. **键盘优先**——主流程全键盘可达；焦点环永不隐藏；`Esc` 退出当前层（模态 → 抽屉 → 页面）
3. **破坏可退**——删除/覆盖需二次确认 + 可撤销；写操作保 `.bak`
4. **风险显式**——首次运行门（素材授权、密钥、数据外发）不可默认同意（LegalGate 范式）
5. **乐观且诚实**——本地写操作可乐观更新，但失败必须回滚并明确告知

## 7.2 沉浸页范式（聆涧 / 听默 播放型页面）

| 元素 | 规范 |
| :--- | :--- |
| 层序 | 背景静帧 → 呼吸/晕影 → Canvas 粒子 → 控件（仅控件可点） |
| 主控件 | 播放/暂停 96px，`opacity: .12`，hover/focus `→ .5` |
| 进度 | 2px 会话计时（不是"曲长"）；`HH:MM:SS` 11px `opacity: .35` |
| 鼠标 | 2s 无移动隐藏；移至顶部 48px 或 `Esc` 返回 |
| 快捷键 | `Space` 播放/暂停 · `Esc` 返回 · `M` 静音 · `↑↓` 音量 ±5% · `F` 切换特效 |
| 降级 | `prefers-reduced-motion` → 静态颗粒 2%，取消闪烁/视差 |

## 7.3 工作台范式（工具/后台型）

- 左栏 `240px`（导航/过滤/库）+ 主区；顶栏 `56px`
- 表格行高按密度档：`compact 36` / `comfortable 44` / `sparse 52`
- 批量操作浮出于**选择后**出现的操作条，不做常驻工具栏
- 长任务（爬取/推理/导出）显示进度 + 可中断 + 完成后可回溯

---

# 8. 动效范式

| 类别 | 时长 | 缓动 | 示例 |
| :--- | :--- | :--- | :--- |
| 反馈 | 80ms | `standard` | hover / 按下 |
| 状态 | 160ms | `standard` | 开关、标签切换 |
| 区块 | 240ms | `enter` | 面板展开、列表入场 |
| 视图 | 400ms | `enter`/`exit` | 路由切换 |
| 沉浸 | 1200ms+ | `linear` | 呼吸、Ken Burns 单程 |

**预算与降级**：
- 粒子总预算 **800**；按音源/数据权重分配，两遍归一（最大→1，总和 ≤ 1.4）
- 页面隐藏（`document.hidden`）暂停一切 RAF
- `prefers-reduced-motion: reduce` → 取消位移/粒子/闪烁，仅保留 ≤160ms 透明度过渡
- 帧预算：1280×800 @60fps 下 **≤8ms/帧**；连续两次 >32ms 降档 30%

---

# 9. 页面骨架模板（生成入口）

## 9.1 营销型（README / 落地页）

```
双标并排(64) → H1(中文·英文) → Slogan(中/英) → 徽章行 → 出品方+仓库
→ 简介(1 段) → 功能一览(表) → 快速开始(代码块) → 结构/架构 → 品牌标识(表+色板) → 页脚(主标48+版权)
```

## 9.2 工作台型

```
顶栏(56: 品牌+全局操作) → 左栏(240: 导航/过滤) → 主区(列表/详情, 含三态) → 右侧抽屉(可选)
```

## 9.3 仪表盘型

```
顶栏 → KPI 条(3–5 指标卡) → 图表区(2 列栅格, 含口径脚注) → 明细表(可分页/筛选)
```

## 9.4 沉浸型

见 §7.2。

---

# 10. 给 OpenDesign / 生成式工具的指引

## 10.1 系统提示（可直接粘贴）

```
你在为「鹿溪联合创新实验室（LUXI Joint Innovation Lab）」生成设计。

品牌：母题「林深见鹿，源启清溪」；四色 tokens：鹿溪绿 #0D5E42、源启白 #F5F7FA、
进化蓝 #00D2FF、标题金 #F1C40F。产品标识 = 鹿溪绿圆角砖 + 业务图形 + 进化蓝 S 形溪流 + 源启星。
实验室主标唯一权威源为官方 LUXI LAB.svg，不得重绘。

约束：
1) 中文优先，字体栈见 tokens.css；数据用 tabular-nums。
2) 间距 4px 基准；圆角 md=10px；阴影仅 xs/sm/md/lg/focus 五档。
3) 每屏仅一个 primary 按钮（鹿溪绿实底）；选中态用颜色不用加粗。
4) 必须设计 加载/空/错误 三态；空状态给下一步。
5) 键盘可达 + focus-visible 焦点环（#00D2FF）；实现 prefers-reduced-motion 降级。
6) 概率/预测/模型输出必须标注置信度与口径；禁止把模型输出呈现为事实。
7) 破坏性操作二次确认且可撤销。
8) 产品 accent 仅用于强调与图表主序列，不得替换品牌四色职能。
禁止：3D 图表、霓虹赛博配色、渐变阴影堆砌、无标注的红色警示滥用、重绘实验室主标。
```

## 10.2 产品 prompt 模板

```
产品：{中文名} · {英文名}（{工程代号}）
矩阵：{矩阵}     accent：{accent} / {accent2}
Slogan：{Slogan中} / {SloganEn}
意象：{方标语义}
任务：生成 {页面类型：营销页/工作台/仪表盘/沉浸页}
要求：遵循 LUXI Design System v1.0；主题 {light|dark|ink}；密度 {compact|comfortable|sparse}
```

## 10.3 自检清单（生成后逐条核对）

- [ ] 双标并排等大；主标来自官方源
- [ ] 仅一个 primary 按钮；选中态用色
- [ ] 三态齐全；空状态有下一步
- [ ] 焦点环可见；`Esc` 可退层
- [ ] 数据区有口径脚注；预测有置信度
- [ ] `prefers-reduced-motion` 降级生效
- [ ] 色值全部来自 tokens（无硬编码游离色）
- [ ] 深浅主题对比度 ≥ 4.5:1

---

# 11. 附录：三层文件的消费方式

| 文件 | 消费方式 |
| :--- | :--- |
| `tokens.json` | 设计工具导入变量；代码生成读取 schema；`color.product.*` 映射产品 accent |
| `tokens.css` | 前端直接 `<link>`；`data-theme` / `data-product` / `data-density` 三个属性驱动 |
| `DESIGN.md` | 人读规范；工具侧可作为 RAG 语料或 prompt 前缀 |

**版本策略**：`v1.x` 允许新增 token 与组件（向后兼容）；`v2.0` 才可变更 core 四色与原则。变更需同步更新三层文件与各产品引用。

---

<div align="center">
  <img src="assets/luxi-lab-main.svg" width="48" height="48" alt="LUXI LAB" />
  <p><strong>鹿溪设计范式 · LUXI Design System</strong> · 林深见鹿，源启清溪</p>
  <p>© 鹿溪联合创新实验室 · LUXI Joint Innovation Lab</p>
  <p><em>Deep Insights, Evolutionary Origin.</em></p>
</div>
