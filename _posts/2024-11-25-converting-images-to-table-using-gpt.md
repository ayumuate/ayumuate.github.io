---
title: 用大模型识别表格，保存成 Excel 工作簿
date: 2024-11-25 00:27:00 +0800
categories: [ Computer, Tutorials ]
tags: [ Excel, Table, LLM, ChatGPT, Tutorial, Idiot, Conversion, Recognition, chinese ]
---

Excel 自带的图片转表格有多难用，用过的都知道。一般的图片转表格工具，多数收费，效果也仅仅是勉强令人满意。所幸，我们苟活到了 ChatGPT 的时代。虽然目前的大模型还不能直接输出 `xlsx` 格式的文件，但是，我们仍然可以用它更快更好的将图片转化成表格。

1. 打开一个支持多模态的大模型，如
   - [Kimi](https://kimi.moonshot.cn)
   - [ChatGPT](https://chatgpt.com)
   - [Microsoft Copilot](https://copilot.microsoft.com)
2. 上传你的表格图片，要求大模型“识别表格中的内容，并以表格格式输出”。
   - 如果你的大模型输出表格到一半戛然而止了，你可以用“继续”命令让它继续输出。
   - 如果表格的格式不符合你的要求，你可以向大模型陈述你希望的格式，大模型还是比较通人话的。
3. 从表格的第一行第一列的第一个字符开始，选中到最后一行最后一列的最后一个字符，复制。
4. 打开一个空白的 Excel 工作簿（或者其它你希望粘贴表格的现成的工作簿），在 A1 单元格（或你希望粘贴表格的其它位置）粘贴。
5. 调整列宽、行高、换行、字体等细节格式，调整你的表格，保存文档。

易用性、准确率简直爆杀多数的图片转表格工具，不是吗？
