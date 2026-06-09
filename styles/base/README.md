# Base — AI Styles 官方风格 · v1.0

> **Base** 是一套以组件化为核心的通用文档风格，适合将任意 AI 输出渲染为结构清晰、排版精良的 HTML页面，及其他格式。

---
## 执行步骤（必须严格按照步骤执行，不能省略任何一步）
### 第一步
根据选择的模板读取所有需加载文件，完成后打印加载完毕以及已加载的文件列表；
### 第二步
解析 @as-protocol 内容规范 和 模板，完成后打印出@as-protocol内容规范，以表格的形式展示data-as-slot/data-as-component/data-as-lock标注的元素列表；
### 第三步
严格按照 @as-protocol 内容规范 和 模板执行渲染，完成后打印渲染完毕；
### 第四步
全部渲染完成后，最后再按照 @as-check 内容执行检查，如发现问题则立即修改，完成后打印自检完毕；

---

## 模板列表
| 模板名称    | 适合场景                     | 需加载文件                   | 渲染依赖            |
|---------|--------------------------|-------------------------|-----------------|
| html    | 可视化 / 可打印 PDF / 浏览器分享    | templates/as.html       | 浏览器             |
| html2   | 可视化 / 可打印 PDF / 浏览器分享    | templates/as-v2.html    | 浏览器             |
| html3   | 可视化 / 可打印 PDF / 浏览器分享    | templates/as-v3.html    | 浏览器             |
| html4   | 可视化 / 可打印 PDF / 浏览器分享    | templates/as-v4.html    | 浏览器             |
| aoshtml | 可视化 / 可打印 PDF / 浏览器分享    | templates/aos-template.html | 浏览器             |
| md      | 文档站 / 邮件 / 纯文本归档 / PR 描述 | templates/as.md         | 任意 Markdown 渲染器 |
| ppt     | 网页 PPT / 演示 / 翻页幻灯片 / 可打印 PDF | templates/ppt.html      | 浏览器             |

**默认模板：** html

AI注意：
1. 如存在多个模板，而用户未指定模板时，列出选项提醒用户选择。
2. 需加载文件先从本地目录找；
   找不到则用 https://raw.githubusercontent.com/nest85/ai-styles/main/styles/base/ + 需加载文件 查找；
   只要有任一需加载文件最终找不到，就停止生成，并告诉用户缺哪个文件； 不要自行编造样式或用其它风格替代。



## 人类使用方式（AI忽略）

把以下内容复制给 Claude、ChatGPT、Gemini、豆包、千问、Kimi，附上你要美化的内容：

```
读取这套模板 https://raw.githubusercontent.com/nest85/ai-styles/main/styles/base/README.md，如果不能读取或读取失败则停止任务。
 
读取成功后，根据模板提示把以下内容用这套风格渲染：
[你的 AI 输出内容]
```