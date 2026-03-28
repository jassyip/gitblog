# 20260321 LingoSync AI 配方构思记录

Source URL: https://www.notion.so/329d75c13c6a81769a50f34a6d851941

## Properties

| Property | Value |
| --- | --- |
| title | 20260321 LingoSync AI 配方构思记录 |

## Content

本文档详细记录 LingoSync AI 配方的构思背景与完整实现逻辑，涵盖语境感知自适应、即时纠偏建议、每日山汇总复盘及 Notion 增量同步等核心模块。
## 一、配方名称
LingoSync AI
## 二、核心功能
### 2.1 语境感知自适应
系统持续分析用户的语言使用场景与表达模式，根据目标语言类型、语言掌握程度及对话语境自动调整交互难度与内容深度。语境检测模型在每次交互后持续更新用户的语言画像，确保内容始终处于用户可接受且有山进阶意义的层次。
### 2.2 即时纠偏建议
当用户在正常对话中出现语法错误、用词不当或表达方式不自然时，系统以自然嵌入的方式提出纠偏建议，避免中断对话流程。纠偏内容包含正确表达方式与简要解释，帮助用户在真实语境中建立正确语言直觉。纠偏记录将自动保存，供晚间山汇总使用。
### 2.3 每日 22:00 山汇总复盘
每天晙22:00，系统自动汇总当日全部纠偏条目与语法要点，以结构化学习报告的形式呈送给用户。复盘内容包括错误情塶分类、典型错误案例与建议的正确表达对照，帮助用户在轻松状态下巩固当日所学内容。
### 2.4 Notion 增量同步（含错误自动划线逻辑）
每次复盘完成后，系统将当日纠偏条目增量写入用户指定的 Notion 数据库，按日期进行标注归档。对于用户在后续对话中展现已掌握的错误词汇或语法点，系统自动在 Notion 归档条目中对其加以划线标记，直观表明掌握状态，避免重复复习已熟悉的内容。
## 三、多语言自适应
系统支持全球化语言自适应（Match the user's primary language）。界面语言、纠偏说明、山汇总报告及所有引导文本，均自动识别用户的母语偏好，以对应语言输出。对于正在学习目标语言的用户，系统将根据学习目标展示二语对照内容。
## 四、英文 Context（配方完整描述）
LingoSync AI is a context-aware language learning assistant that integrates seamlessly into daily conversations to deliver personalized, real-time language coaching. The recipe is built around four core pillars: adaptive context matching, non-intrusive error correction, daily structured review, and incremental Notion archiving.
Key capabilities include:
1. Context-aware adaptive matching: The system continuously analyzes the user's language usage patterns, target language type, and current proficiency level. Conversation difficulty and content depth are dynamically adjusted after each interaction to ensure the material remains appropriately challenging and pedagogically progressive.
2. Instant correction suggestions: When the user produces grammatical errors, incorrect word choices, or unnatural expressions during regular conversation, the system embeds correction suggestions naturally without interrupting the conversational flow. Each correction includes the recommended phrasing and a brief contextual explanation to reinforce correct language intuition.
3. Daily review summary at 22:00: A structured learning report is automatically compiled and delivered each evening at 10:00 PM, covering all corrections and grammar points from the day. The report categorizes errors by type, pairs each mistake with the corrected expression, and provides context-rich examples to facilitate retention.
4. Notion incremental sync with mastery strikethrough: After each daily review, all correction items are written to the user's designated Notion database with date-based labeling. As the user subsequently demonstrates mastery of previously flagged vocabulary or grammar points in live conversation, the system automatically applies strikethrough formatting to the corresponding Notion entries, providing a clear visual record of learning progress.
5. Multilingual adaptive output (Match the user's primary language): All interface text, correction explanations, and summaries are delivered in the user's native language. For learners targeting a specific language, bilingual comparison content is displayed where appropriate.
## 五、设计原则
1. 非入侵式纠偏：语言建议以自然嵌入为首要原则，不中断正常对话，确保学习体验轻松自然。
2. 山进阶内容：语境自适应机制确保内容始终在用户掌握边界上下，避免过于简单或过于困难。
3. 可视化成长轨迹：Notion 划线逻辑将掌握状态直观呀展示，帮助用户建立山学习成就感。
4. 尊重学习节奏：复盘时间默认设置为 22:00，可根据用户个人作息灵活调整，尊重个体差异。