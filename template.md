---
id: artisan-portrait
title: 匠人环境人像
title_en: Environmental Artisan Portrait
description: 用官方摄影公式生成有故事感的环境人像
author: zkywalker
version: 1.0.0
profile: photo
tags: [人像, 摄影, 匠人, 工坊, portrait, artisan, workshop, editorial]
models:
  - name: gemini-3-pro-image-preview
    tested: true
    quality: best
  - name: gemini-3.1-flash-image-preview
    tested: false
    quality: good
  - name: gemini-2.5-flash-image
    tested: false
    quality: good
aspect: "3:4"
difficulty: beginner
category: art
samples:
  - file: samples/sample-3-pro-01.png
    model: gemini-3-pro-image-preview
    prompt: "A photorealistic environmental portrait of an elderly Japanese ceramicist carefully shaping a bowl on a potter's wheel, in a rustic workshop filled with clay tools and unfinished pottery. Lit by warm golden-hour window light and captured with an 85mm portrait lens with shallow depth of field. Quiet mastery, tactile craftsmanship, and grounded realism."
    aspect: "3:4"
created: 2026-03-30
updated: 2026-03-30
---

## 描述

生成有明确职业身份、环境叙事和摄影语言的匠人人像。适合陶艺师、木工、花艺师、面包师、制表师等“人物 + 手上动作 + 工作空间”场景。

## Prompt Template

```
A photorealistic environmental portrait of {{subject|an elderly Japanese ceramicist}} {{action|carefully shaping a bowl on a potter's wheel}}, in {{setting|a rustic workshop filled with clay tools and unfinished pottery}}. Lit by {{lighting|warm golden-hour window light}} and captured with {{lens|an 85mm portrait lens with shallow depth of field}}. {{mood|Quiet mastery, tactile craftsmanship, and grounded realism}}.
```

## Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `subject` | an elderly Japanese ceramicist | 主体身份。优先写清职业、年龄段或文化背景 |
| `action` | carefully shaping a bowl on a potter's wheel | 手上动作。写具体操作比写抽象姿态更稳 |
| `setting` | a rustic workshop filled with clay tools and unfinished pottery | 环境信息。放进工具、半成品和空间线索 |
| `lighting` | warm golden-hour window light | 灯光氛围。自然侧光、窗光、顶光都可以直接替换 |
| `lens` | an 85mm portrait lens with shallow depth of field | 摄影语言。用焦段和景深控制人物与背景关系 |
| `mood` | Quiet mastery, tactile craftsmanship, and grounded realism | 收尾气质。补充情绪和质感，不要堆质量标签 |

## Tips

- 这是官方摄影公式类模板，重点是主体、动作、环境、灯光和镜头语言一起出现，不要只丢职业名词
- 最稳的替换方式是只改 `subject` 和 `action`，先保留默认 `setting` / `lighting` / `lens`
- 如果想更像杂志 editorial，人和工具的互动要具体，比如 “measuring leather by hand” 或 “trimming bonsai branches”
- 想让环境更真实，就写出 2 到 4 个能证明职业身份的物件，不要写成空泛的 “in a studio”
- `85mm` 适合强调人物；如果想要更多环境信息，可以改成 `35mm documentary lens`
- 避免使用 “8K”, “masterpiece”, “ultra detailed” 这类堆砌词，Gemini 对叙事式描述更稳定
