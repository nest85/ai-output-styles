---
name: as-blue
version: 1.0
description: AI Styles - 企业科技深蓝风格
as-protocol: as-protocol-html-v1.1
---

# AI Styles - 企业科技深蓝风格 · v1.0

## 模板介绍

本套风格简称 `blue`，是一套企业内部的文档风格，以深蓝科技为视觉基调，把 AI
输出渲染成企业级风格的正式文档，覆盖方案、汇报、纪要、研究分析到内部演示等场景。具体模板与适用场景见下表。

---

## 模板列表

| 模板名称 | 模板演示                             | 适用场景                       | 模板文件                                                                                                         |
|------|----------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------|
| doc  | [演示](examples/complex-ppt@doc-1.html) | 通用文档 / 方案 / 汇报 / 纪要 / 研究分析 | [templates/doc.html](https://raw.githubusercontent.com/nest85/ai-styles/dev/styles/blue/templates/doc.html)  |
| ppt  | [演示](examples/blue-ppt-demo.html) | 演示 / 汇报 PPT / 方案宣讲（单页可翻页）  | [templates/doc.html](https://raw.githubusercontent.com/nest85/ai-styles/dev/styles/blue/templates/ppt.html) |

---

## 使用说明

1. **网页 AI 提示词使用**：把以下提示词复制给 Claude、ChatGPT、Gemini、豆包、千问、Kimi。
   ```
   读取 AI Styles 风格说明：https://raw.githubusercontent.com/nest85/ai-styles/main/styles/blue/README.md。
   如果不能读取或读取失败则停止任务。
   读取成功后，根据该风格说明中的「渲染步骤」，把以下内容进行渲染：
   [你的 AI 输出内容]
   ```
2. **网页 AI 上传模板文件使用**：在模板列表下载具体模板文件，上传给网页 AI，把以下提示词复制给 AI。
   ```
   读懂所有 <模板文件名称> 内联的 AS 协议（通配符 @as-protocol-*）与元素声明，按其规范把以下内容进行渲染：
   [你的 AI 输出内容]
   ```
3. **安装 AS Skill 使用**：`/as blue <模板名称>`，示例如下：
   ```
   /as blue doc 以上对话内容
   ```
   ```
   /as blue ppt @待渲染文件
   ```

---

## 渲染步骤

> 注意：AI 必须按步骤严格执行，严禁省略；人类可略过。

1. **选择模板**：如用户指定则用指定模板；未指定则展示模板列表给用户选择。
2. **加载模板**：加载所选模板的「模板文件」（见模板列表），先按模板文件名从本地加载，若本地无文件则通过链接到远程加载。
3. **解析模板**：读懂模板所有内容，并打印输出以下内容：
    1. 所有采用通配符 `@as-protocol-*` 注释的 AS 协议；
    2. 表格展示所有标注 `data-as-element="name"` 属性的 AS Element，及其渲染说明（采用 `@as-element name`
       标注的注释），表格包含列：元素名称、允许、适用、禁止；
4. **渲染输出**：严格按照所有 AS 协议描述的规范和渲染步骤执行，严禁忽略任何规范，严禁跳过渲染步骤。

---