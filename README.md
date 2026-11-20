<h1 align="center">Polaris Dance</h1>

<p align="center">
  <a href="https://giphy.com/gifs/kirby-nintendo-dance-l0HlIDueXmcWNTPO0">
    <img src="https://media.giphy.com/media/l0HlIDueXmcWNTPO0/200.gif" width="160" height="120" alt="星之卡比跳舞（动画作者 Kéké）">
  </a>
</p>

<p align="center"><strong>一句话做课件，再一句话改课件。</strong></p>

<p align="center">
  输入主题，确认大纲，生成整份演示文稿。做完可以用对话修改指定页面，再导出 PPTX 或 PDF。
</p>

<p align="center">
  <a href="https://polarisdance.online/"><strong>在线体验 ↗</strong></a>
  · <a href="#课件示例">看课件示例</a>
  · <a href="#完整演示">看完整演示</a>
</p>

<p align="center">
  <a href="#课件示例">
    <img src="preview/hero-ours.jpg" alt="Polaris Dance 生成的四份课件封面：《春》、正弦函数、力学第一课和 Redis 缓存故障">
  </a>
</p>

## 从主题生成 PPT

可以只给一句主题，也可以指定受众、讲解重点和呈现方式。

**一句主题**

> 给初一学生讲朱自清的《春》

[查看《春》课件（PDF）](result/1-春.pdf)

**完整要求**

> 给高一学生讲一节课：正弦函数 y=sin x 的图像与性质。要讲清楚五点作图法、周期性、奇偶性、单调区间和最值，配合图像来讲

[查看正弦函数课件（PDF）](result/2-数学.pdf)

## 一句话修改指定页

《力学第一课》生成后，在对话里提出修改。

> 把第 3 页标题改成浅绿色，标题和正文都换一种现有的字体。

| 修改前 | 修改后 |
| :---: | :---: |
| <img src="preview/edit-demo-before.jpg" width="400" alt="修改前的第 3 页使用橙红色标题和粗体字"> | <img src="preview/edit-demo-after.jpg" width="400" alt="修改后的第 3 页使用浅绿色标题和更新后的字体"> |

图片截自同一份课件的第 3 页。完整演示从 2:03 开始展示对话修改。

## 课件示例

四份课件由 Polaris Dance 生成。每份 8 页，点击图片可以放大查看。

<table>
  <tr>
    <td align="center" width="50%">
      <a href="preview/1-spring/ours-2.jpg"><img src="preview/1-spring/ours-2.jpg" width="380" alt="朱自清《春》课件内页"></a><br>
      <strong>语文 · 朱自清《春》</strong><br>
      <a href="result/1-春.pdf">PDF 原件</a> · <a href="compare/README.md#朱自清春">逐页对比</a>
    </td>
    <td align="center" width="50%">
      <a href="preview/2-sine/ours-3.jpg"><img src="preview/2-sine/ours-3.jpg" width="380" alt="正弦函数课件内页"></a><br>
      <strong>数学 · 正弦函数</strong><br>
      <a href="result/2-数学.pdf">PDF 原件</a> · <a href="compare/README.md#正弦函数">逐页对比</a>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <a href="preview/3-force/ours-3.jpg"><img src="preview/3-force/ours-3.jpg" width="380" alt="力学第一课课件内页"></a><br>
      <strong>物理 · 力学第一课</strong><br>
      <a href="result/3-物理.pdf">PDF 原件</a> · <a href="compare/README.md#力学第一课">逐页对比</a>
    </td>
    <td align="center" width="50%">
      <a href="preview/4-redis/ours-3.jpg"><img src="preview/4-redis/ours-3.jpg" width="380" alt="Redis 缓存故障课件内页"></a><br>
      <strong>后端 · Redis 缓存故障</strong><br>
      <a href="result/4-redis.pdf">PDF 原件</a> · <a href="compare/README.md#redis-缓存故障">逐页对比</a>
    </td>
  </tr>
</table>

[查看 Polaris Dance、豆包和 Claude Opus 5.5 的同题对比、完整提示词和模型设置 →](compare/README.md)

## 在线体验

1. 打开 [polarisdance.online](https://polarisdance.online/)，输入「给初一学生讲力学第一课」，选择页数和比例。
2. 确认大纲后开始生成。页面会陆续出现，8 页通常需要约 15–25 分钟。
3. 在对话框里修改页面，例如「所有页加上页码」。可以说「撤销」来撤回上一次修改。
4. 在页面右下角导出 PPTX 或 PDF。

中国大陆访问可能较慢，也可以先浏览上面的课件示例。

## 完整演示

《力学第一课》的生成、断点续做和对话修改过程。视频为 3 倍速，约 3 分钟。

https://github.com/user-attachments/assets/b6f2a6b3-5b67-4841-a0b2-c14a612d7c92

[查看仓库中的视频文件](demo/demo.mp4)

<details>
<summary>查看演示时间线</summary>

| 时间 | 操作 |
| --- | --- |
| 0:00 | 输入「给初一学生讲力学第一课」，选择 8 页、16:9，确认生成的大纲 |
| 0:49 | 网络中断后，点击「接着做完」 |
| 1:40 | 查看生成的 8 页课件，实际用时约 19 分钟 |
| 2:03 | 对话要求全篇加页码，修改第 3 页标题和第 7 页底图。Agent 询问第 7 页需要哪种黄色 |
| 2:33 | 明确第 7 页使用明亮暖黄色，并调整第 3 页标题颜色和字体 |

</details>

---

本仓库用于展示 Polaris Dance 的课件成果和同题对比。应用请通过[在线演示](https://polarisdance.online/)体验。
