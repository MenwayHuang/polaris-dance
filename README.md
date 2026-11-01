# Polaris Dance · 一句话做课件、一句话改课件的 PPT Agent

> 输入一个主题，Agent 自动产出一份可以直接放映的演示文稿；做完之后用一句话接着改，它听得懂你要改哪几页、改什么。

[![在线体验](https://img.shields.io/badge/在线体验-polarisdance.online-2f81f7)](https://polarisdance.online)
[![models](https://img.shields.io/badge/models-Qwen3.7--Plus%20%7C%20Qwen3.8--Flash%20%7C%20Wan2.7--Image-4f86f7)](#-使用模型)

本仓库只展示成果，不含源码。下面所有页面都由 Agent 自动生成，没有做任何人工润色与重排。

---

## 🎬 演示视频：一句话做出一份课件，再一句话改好


https://github.com/user-attachments/assets/b6f2a6b3-5b67-4841-a0b2-c14a612d7c92

视频里发生了什么（3 倍速；点上图播放）：

| 时间 | 用户做了什么 | Agent 做了什么 |
| --- | --- | --- |
| 0:00 | 输入「给初一学生讲力学第一课」，选 8 页、16:9 | 先交出 8 页大纲：每页讲什么、讲几分钟；用户点「就这样，开始做」 |
| 0:49 | 网络中途断开，点「接着做完」 | 从断点接着做，做好的页陆续出现 |
| 1:40 | —— | 完成：8 页，用时约 19 分钟；可以在线翻看，也可以下载 PDF / PPTX |
| 2:03 | 一句话提三件事：所有页加页码；第 3 页标题改成红色；第 7 页底图换成黄色的背景图 | 先复述它的理解，再分别动手：全篇加上页码，第 3 页标题改成红色；第 7 页要哪种黄没说清，就先问用户（明亮暖黄 / 柔和浅黄 / 金黄） |
| 2:33 | 回答：第 7 页要明亮暖黄的底图；同时第 3 页标题改浅绿色、换一种现有字体 | 听出这是两页各自的修改：第 7 页单独换上一张暖黄底图，其余页一点不动；第 3 页改了标题颜色和字体 |

这段视频想说明三件事：

1. **通过对话和点选，一步步得到自己要的 PPT**：输入主题、选页数和比例，先看大纲、确认后再开始做；做的过程中页面陆续出现，断了也能接着做完；做好后在线翻看或下载 PDF / PPTX。
2. **一个主题就能生成完整的课件，也能按你的详细要求定制**：只给一句主题，Agent 自己规划内容和版式；想要更贴合自己的课，也可以把年级、重点、讲法、页数写清楚，它会照着做。
3. **具备意图识别能力**：做完之后直接用大白话提修改，Agent 分得清「改哪几页、改什么、还是整份都改」，只动该动的地方；没说清楚的先问一句；改得不满意，一句「撤销」就能退回。

---

## 🌐 在线体验

### 👉 [点这里打开 polarisdance.online，自己做一份](https://polarisdance.online)

1. 打开网页，在左下角输入一句话主题，例如「给初一学生讲力学第一课」，选好页数；
2. Agent 先给出大纲，确认后开始制作（8 页大约 15–25 分钟，做好的页会陆续出现在右侧）；
3. 做完后直接在对话框里提修改，比如「第三页标题改成红色」「所有页加上页码」「整份换成暖色调」，不满意可以说「撤销」；
4. 右下角可以下载 PDF / PPTX。

> ⚠️ 演示站点暂未部署在国内云服务器上，国内访问可能较慢；想快速看效果，直接浏览下面的对比图即可。

---

## ✨ 我们的特点

我们用同样的四个主题，让 Polaris Dance、**豆包（线上 PPT 生成）** 和 **Claude Opus 5.5（直接生成，推理程度 high）** 各做一份 8 页课件，对比下来：

- **🚀 Polaris Dance：把模型的设计能力用起来，排版丰富。** 每一页的版式都由模型按这一页的内容现场设计，而不是往固定模板里填字：同一份课件里，封面、概念页、举例页、对比页、总结页的布局各不相同。配图按页面内容现画（推门的手、用三扇门讲力的三要素、缓存失效的请求流程图），底图和整份主题配套（物理课是水彩纸，Redis 分享是深色电路板）。
- **🎈 豆包：模板化、公式化。** 页面结构高度固定：顶部标题 + 色条 + 三张卡片配图片，换了科目也是同一个套路，翻两页就能看出是模板。
- **🤖 Claude Opus 5.5 直接生成：内容扎实，但页面朴素。** 多是浅色底上的小字和简单几何图形，几乎没有配图，视觉层次弱，不够精美，难以直接拿上课堂。

除了做得好看，还有两点：

- **改得准**：做完后可以接着提修改——改某几页的文字、颜色、字体、配图或底图，整份换配色，加页码，增删和调整页面，撤销上一次修改。它先听懂这句话要改哪几页、改什么，只动点到的页。
- **每一页都检查过**：每页做好后会自动检查文字溢出、互相遮挡、看不清、字太小、图片缺失这些问题，有问题当场修好再交给你。

---

## 🖼️ 封面一览（每份成果的第 1 页）

从左到右依次是：**① 语文 · 朱自清《春》 → ② 数学 · 正弦函数 y = sin x → ③ 物理 · 力学第一课 → ④ 后端 · Redis 缓存故障**。

<div align="center">

### 🚀 Polaris Dance（本 Agent）做的四份封面

<img src="preview/hero-ours.jpg" width="900" alt="Polaris Dance 四个主题的封面"/>

### 🎈 豆包做的四份封面

<img src="preview/hero-doubao.jpg" width="900" alt="豆包四个主题的封面"/>

### 🤖 Claude Opus 5.5 直接生成的四份封面

<img src="preview/hero-opus.jpg" width="900" alt="Claude Opus 5.5 四个主题的封面"/>

</div>

---

## 📊 逐章对比：三份课件，8 页全部展开

> 三份是各自独立生成的，页面结构和节奏并不一一对应；按页码对齐只是为了方便横向比较观感。

### 1️⃣ 语文 · 朱自清《春》

💬 **用户输入**：给初一学生讲朱自清的《春》

<table>
<tr>
<td align="center"><b>🚀 Polaris Dance</b></td>
<td align="center"><b>🎈 豆包</b></td>
<td align="center"><b>🤖 Claude Opus 5.5 直出</b></td>
</tr>
<tr>
<td>
<img src="preview/1-spring/ours-1.jpg" width="280" alt="Polaris Dance 春 第1页"/><br/>
<img src="preview/1-spring/ours-2.jpg" width="280" alt="Polaris Dance 春 第2页"/><br/>
<img src="preview/1-spring/ours-3.jpg" width="280" alt="Polaris Dance 春 第3页"/><br/>
<img src="preview/1-spring/ours-4.jpg" width="280" alt="Polaris Dance 春 第4页"/><br/>
<img src="preview/1-spring/ours-5.jpg" width="280" alt="Polaris Dance 春 第5页"/><br/>
<img src="preview/1-spring/ours-6.jpg" width="280" alt="Polaris Dance 春 第6页"/><br/>
<img src="preview/1-spring/ours-7.jpg" width="280" alt="Polaris Dance 春 第7页"/><br/>
<img src="preview/1-spring/ours-8.jpg" width="280" alt="Polaris Dance 春 第8页"/>
</td>
<td>
<img src="preview/1-spring/doubao-1.jpg" width="280" alt="豆包 春 第1页"/><br/>
<img src="preview/1-spring/doubao-2.jpg" width="280" alt="豆包 春 第2页"/><br/>
<img src="preview/1-spring/doubao-3.jpg" width="280" alt="豆包 春 第3页"/><br/>
<img src="preview/1-spring/doubao-4.jpg" width="280" alt="豆包 春 第4页"/><br/>
<img src="preview/1-spring/doubao-5.jpg" width="280" alt="豆包 春 第5页"/><br/>
<img src="preview/1-spring/doubao-6.jpg" width="280" alt="豆包 春 第6页"/><br/>
<img src="preview/1-spring/doubao-7.jpg" width="280" alt="豆包 春 第7页"/><br/>
<img src="preview/1-spring/doubao-8.jpg" width="280" alt="豆包 春 第8页"/>
</td>
<td>
<img src="preview/1-spring/opus-1.jpg" width="280" alt="Opus 5.5 春 第1页"/><br/>
<img src="preview/1-spring/opus-2.jpg" width="280" alt="Opus 5.5 春 第2页"/><br/>
<img src="preview/1-spring/opus-3.jpg" width="280" alt="Opus 5.5 春 第3页"/><br/>
<img src="preview/1-spring/opus-4.jpg" width="280" alt="Opus 5.5 春 第4页"/><br/>
<img src="preview/1-spring/opus-5.jpg" width="280" alt="Opus 5.5 春 第5页"/><br/>
<img src="preview/1-spring/opus-6.jpg" width="280" alt="Opus 5.5 春 第6页"/><br/>
<img src="preview/1-spring/opus-7.jpg" width="280" alt="Opus 5.5 春 第7页"/><br/>
<img src="preview/1-spring/opus-8.jpg" width="280" alt="Opus 5.5 春 第8页"/>
</td>
</tr>
</table>

原文件（GitHub 预览大 PDF 偶尔加载不出来，可以下载后查看）：[Polaris Dance 版 `1-春.pdf`](result/1-春.pdf)（16.3 MB）· [豆包版 `1-春-豆包.pdf`](compare/1-春-豆包.pdf)（3.0 MB）· [Claude Opus 5.5 版 `1-春-opus5.5.pdf`](compare/1-春-opus5.5.pdf)（0.9 MB）

---

### 2️⃣ 数学 · 正弦函数 y = sin x 的图像与性质

💬 **用户输入**：给高一学生讲一节课：正弦函数 y=sin x 的图像与性质。要讲清楚五点作图法、周期性、奇偶性、单调区间和最值，配合图像来讲

<table>
<tr>
<td align="center"><b>🚀 Polaris Dance</b></td>
<td align="center"><b>🎈 豆包</b></td>
<td align="center"><b>🤖 Claude Opus 5.5 直出</b></td>
</tr>
<tr>
<td>
<img src="preview/2-sine/ours-1.jpg" width="280" alt="Polaris Dance 正弦 第1页"/><br/>
<img src="preview/2-sine/ours-2.jpg" width="280" alt="Polaris Dance 正弦 第2页"/><br/>
<img src="preview/2-sine/ours-3.jpg" width="280" alt="Polaris Dance 正弦 第3页"/><br/>
<img src="preview/2-sine/ours-4.jpg" width="280" alt="Polaris Dance 正弦 第4页"/><br/>
<img src="preview/2-sine/ours-5.jpg" width="280" alt="Polaris Dance 正弦 第5页"/><br/>
<img src="preview/2-sine/ours-6.jpg" width="280" alt="Polaris Dance 正弦 第6页"/><br/>
<img src="preview/2-sine/ours-7.jpg" width="280" alt="Polaris Dance 正弦 第7页"/><br/>
<img src="preview/2-sine/ours-8.jpg" width="280" alt="Polaris Dance 正弦 第8页"/>
</td>
<td>
<img src="preview/2-sine/doubao-1.jpg" width="280" alt="豆包 正弦 第1页"/><br/>
<img src="preview/2-sine/doubao-2.jpg" width="280" alt="豆包 正弦 第2页"/><br/>
<img src="preview/2-sine/doubao-3.jpg" width="280" alt="豆包 正弦 第3页"/><br/>
<img src="preview/2-sine/doubao-4.jpg" width="280" alt="豆包 正弦 第4页"/><br/>
<img src="preview/2-sine/doubao-5.jpg" width="280" alt="豆包 正弦 第5页"/><br/>
<img src="preview/2-sine/doubao-6.jpg" width="280" alt="豆包 正弦 第6页"/><br/>
<img src="preview/2-sine/doubao-7.jpg" width="280" alt="豆包 正弦 第7页"/><br/>
<img src="preview/2-sine/doubao-8.jpg" width="280" alt="豆包 正弦 第8页"/>
</td>
<td>
<img src="preview/2-sine/opus-1.jpg" width="280" alt="Opus 5.5 正弦 第1页"/><br/>
<img src="preview/2-sine/opus-2.jpg" width="280" alt="Opus 5.5 正弦 第2页"/><br/>
<img src="preview/2-sine/opus-3.jpg" width="280" alt="Opus 5.5 正弦 第3页"/><br/>
<img src="preview/2-sine/opus-4.jpg" width="280" alt="Opus 5.5 正弦 第4页"/><br/>
<img src="preview/2-sine/opus-5.jpg" width="280" alt="Opus 5.5 正弦 第5页"/><br/>
<img src="preview/2-sine/opus-6.jpg" width="280" alt="Opus 5.5 正弦 第6页"/><br/>
<img src="preview/2-sine/opus-7.jpg" width="280" alt="Opus 5.5 正弦 第7页"/><br/>
<img src="preview/2-sine/opus-8.jpg" width="280" alt="Opus 5.5 正弦 第8页"/>
</td>
</tr>
</table>

原文件：[Polaris Dance 版 `2-数学.pdf`](result/2-数学.pdf)（10.0 MB）· [豆包版 `2-数学-豆包.pdf`](compare/2-数学-豆包.pdf)（1.8 MB）· [Claude Opus 5.5 版 `2-数学-opus5.5.pdf`](compare/2-数学-opus5.5.pdf)（1.1 MB）

---

### 3️⃣ 物理 · 力学第一课

💬 **用户输入**：给初一学生讲力学第一课

<table>
<tr>
<td align="center"><b>🚀 Polaris Dance</b></td>
<td align="center"><b>🎈 豆包</b></td>
<td align="center"><b>🤖 Claude Opus 5.5 直出</b></td>
</tr>
<tr>
<td>
<img src="preview/3-force/ours-1.jpg" width="280" alt="Polaris Dance 力 第1页"/><br/>
<img src="preview/3-force/ours-2.jpg" width="280" alt="Polaris Dance 力 第2页"/><br/>
<img src="preview/3-force/ours-3.jpg" width="280" alt="Polaris Dance 力 第3页"/><br/>
<img src="preview/3-force/ours-4.jpg" width="280" alt="Polaris Dance 力 第4页"/><br/>
<img src="preview/3-force/ours-5.jpg" width="280" alt="Polaris Dance 力 第5页"/><br/>
<img src="preview/3-force/ours-6.jpg" width="280" alt="Polaris Dance 力 第6页"/><br/>
<img src="preview/3-force/ours-7.jpg" width="280" alt="Polaris Dance 力 第7页"/><br/>
<img src="preview/3-force/ours-8.jpg" width="280" alt="Polaris Dance 力 第8页"/>
</td>
<td>
<img src="preview/3-force/doubao-1.jpg" width="280" alt="豆包 力 第1页"/><br/>
<img src="preview/3-force/doubao-2.jpg" width="280" alt="豆包 力 第2页"/><br/>
<img src="preview/3-force/doubao-3.jpg" width="280" alt="豆包 力 第3页"/><br/>
<img src="preview/3-force/doubao-4.jpg" width="280" alt="豆包 力 第4页"/><br/>
<img src="preview/3-force/doubao-5.jpg" width="280" alt="豆包 力 第5页"/><br/>
<img src="preview/3-force/doubao-6.jpg" width="280" alt="豆包 力 第6页"/><br/>
<img src="preview/3-force/doubao-7.jpg" width="280" alt="豆包 力 第7页"/><br/>
<img src="preview/3-force/doubao-8.jpg" width="280" alt="豆包 力 第8页"/>
</td>
<td>
<img src="preview/3-force/opus-1.jpg" width="280" alt="Opus 5.5 力 第1页"/><br/>
<img src="preview/3-force/opus-2.jpg" width="280" alt="Opus 5.5 力 第2页"/><br/>
<img src="preview/3-force/opus-3.jpg" width="280" alt="Opus 5.5 力 第3页"/><br/>
<img src="preview/3-force/opus-4.jpg" width="280" alt="Opus 5.5 力 第4页"/><br/>
<img src="preview/3-force/opus-5.jpg" width="280" alt="Opus 5.5 力 第5页"/><br/>
<img src="preview/3-force/opus-6.jpg" width="280" alt="Opus 5.5 力 第6页"/><br/>
<img src="preview/3-force/opus-7.jpg" width="280" alt="Opus 5.5 力 第7页"/><br/>
<img src="preview/3-force/opus-8.jpg" width="280" alt="Opus 5.5 力 第8页"/>
</td>
</tr>
</table>

原文件：[Polaris Dance 版 `3-物理.pdf`](result/3-物理.pdf)（15.5 MB）· [豆包版 `3-物理-豆包.pdf`](compare/3-物理-豆包.pdf)（2.1 MB）· [Claude Opus 5.5 版 `3-物理-opus5.5.pdf`](compare/3-物理-opus5.5.pdf)（0.9 MB）

---

### 4️⃣ 后端 · Redis 缓存故障（穿透 / 击穿 / 雪崩）

💬 **用户输入**：给后端工程师讲清楚 Redis 的缓存穿透、缓存击穿和缓存雪崩

<table>
<tr>
<td align="center"><b>🚀 Polaris Dance</b></td>
<td align="center"><b>🎈 豆包</b></td>
<td align="center"><b>🤖 Claude Opus 5.5 直出</b></td>
</tr>
<tr>
<td>
<img src="preview/4-redis/ours-1.jpg" width="280" alt="Polaris Dance Redis 第1页"/><br/>
<img src="preview/4-redis/ours-2.jpg" width="280" alt="Polaris Dance Redis 第2页"/><br/>
<img src="preview/4-redis/ours-3.jpg" width="280" alt="Polaris Dance Redis 第3页"/><br/>
<img src="preview/4-redis/ours-4.jpg" width="280" alt="Polaris Dance Redis 第4页"/><br/>
<img src="preview/4-redis/ours-5.jpg" width="280" alt="Polaris Dance Redis 第5页"/><br/>
<img src="preview/4-redis/ours-6.jpg" width="280" alt="Polaris Dance Redis 第6页"/><br/>
<img src="preview/4-redis/ours-7.jpg" width="280" alt="Polaris Dance Redis 第7页"/><br/>
<img src="preview/4-redis/ours-8.jpg" width="280" alt="Polaris Dance Redis 第8页"/>
</td>
<td>
<img src="preview/4-redis/doubao-1.jpg" width="280" alt="豆包 Redis 第1页"/><br/>
<img src="preview/4-redis/doubao-2.jpg" width="280" alt="豆包 Redis 第2页"/><br/>
<img src="preview/4-redis/doubao-3.jpg" width="280" alt="豆包 Redis 第3页"/><br/>
<img src="preview/4-redis/doubao-4.jpg" width="280" alt="豆包 Redis 第4页"/><br/>
<img src="preview/4-redis/doubao-5.jpg" width="280" alt="豆包 Redis 第5页"/><br/>
<img src="preview/4-redis/doubao-6.jpg" width="280" alt="豆包 Redis 第6页"/><br/>
<img src="preview/4-redis/doubao-7.jpg" width="280" alt="豆包 Redis 第7页"/><br/>
<img src="preview/4-redis/doubao-8.jpg" width="280" alt="豆包 Redis 第8页"/>
</td>
<td>
<img src="preview/4-redis/opus-1.jpg" width="280" alt="Opus 5.5 Redis 第1页"/><br/>
<img src="preview/4-redis/opus-2.jpg" width="280" alt="Opus 5.5 Redis 第2页"/><br/>
<img src="preview/4-redis/opus-3.jpg" width="280" alt="Opus 5.5 Redis 第3页"/><br/>
<img src="preview/4-redis/opus-4.jpg" width="280" alt="Opus 5.5 Redis 第4页"/><br/>
<img src="preview/4-redis/opus-5.jpg" width="280" alt="Opus 5.5 Redis 第5页"/><br/>
<img src="preview/4-redis/opus-6.jpg" width="280" alt="Opus 5.5 Redis 第6页"/><br/>
<img src="preview/4-redis/opus-7.jpg" width="280" alt="Opus 5.5 Redis 第7页"/><br/>
<img src="preview/4-redis/opus-8.jpg" width="280" alt="Opus 5.5 Redis 第8页"/>
</td>
</tr>
</table>

原文件：[Polaris Dance 版 `4-redis.pdf`](result/4-redis.pdf)（10.4 MB）· [豆包版 `4-redis-豆包.pdf`](compare/4-redis-豆包.pdf)（2.2 MB）· [Claude Opus 5.5 版 `4-redis-opus5.5.pdf`](compare/4-redis-opus5.5.pdf)（1.1 MB）

---

## 🧠 使用模型

| 环节 | 模型 |
| --- | --- |
| 理解需求、大纲、文稿、设计 | **Qwen3.7-Plus**（推理程度 low） |
| 配图、底图 | **Wan2.7-Image-Pro** / Wan2.7-Image |
| 意图识别 （听懂改哪几页、改什么） | **Qwen3.8-Flash** |

## 🗂️ 仓库结构

```
polaris-dance/
├── demo/          演示视频（demo.mp4，3 倍速）与视频封面图
├── result/        Polaris Dance 生成结果（每份 8 页）
│   ├── 1-春.pdf        语文 · 朱自清《春》
│   ├── 2-数学.pdf      数学 · y = sin x 图像与性质
│   ├── 3-物理.pdf      物理 · 力学第一课
│   └── 4-redis.pdf     后端 · Redis 缓存穿透 / 击穿 / 雪崩
├── compare/       对照组：豆包、Claude Opus 5.5 同主题生成结果（各 8 页 × 4 份）
├── preview/       README 内嵌的页面预览图（每份 8 页，含三张封面横图 hero-*.jpg）
└── README.md
```

---

<p align="center">
  🌐 在线体验：<a href="https://polarisdance.online">polarisdance.online</a> &nbsp;·&nbsp;
  由 Qwen3.7-Plus、Qwen3.8-Flash 与 Wan2.7-Image 驱动
</p>
