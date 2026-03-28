# 20260321 LinguaFlow 配方构思记录

Source URL: https://www.notion.so/329d75c13c6a8170a4e2fdd49a13ac8f

## Properties

| Property | Value |
| --- | --- |
| title | 20260321 LinguaFlow 配方构思记录 |

## Content

本文档详细记录 LinguaFlow: Your AI Language Coach 配方的构思背景与完整实现逻辑，涵盖智能语境匹配、实时纠错建议、每日回顾、Notion 增量归档、多语言自适应及联天聊天习惯匹配等核心模块。
## 一、配方名称
LinguaFlow: Your AI Language Coach
## 二、核心功能
### 2.1 智能语境匹配
系统在用户安装配方后，首先收集用户的母语、目标语言及当前掌握程度信息，并以此为基准建立用户的语言画像。后续每次对话后，系统持续动态更新该画像，自动调整对话难度与内容深度，确保内容始终处于用户可接受且具有山进阶意义的层次。
### 2.2 实时纠错建议
用户在正常对话中出现语法错误、用词不当或表达方式不自然时，系统以自然嵌入的方式提出纠错建议，不中断对话流程。每条建议包含错误内容、推荐表达方式及简要语境解释，帮助用户在真实对话中漸进建立正确的语言直观。纠错记录自动��存，供晚间回顾使用。
### 2.3 每日 22:00 回顾
每天晙22:00，系统自动汇总当日全部纠错条目与语法要点，以结构化学习报告的形式呈送给用户。回顾内容按错误类型分类，每条错误均配有原始表达、建议表达与语境示例对照，帮助用户在轻松状态下巩固当日所学内容。
### 2.4 Notion 增量归档（已掌握错误自动划线）
每次回顾完成后，系统将当日纠错条目增量写入用户指定的 Notion 数据库，按日期进行标注归档。对于用户在后续对话中展现已掌握的错误词汇或语法点，系统自动在 Notion 归档条目中对其加以划线标记，直观表明掌握状态，避免重复复习已熟悉的内容。
## 三、多语言自适应
系统支持全球化语言自适应（Match the user's primary language）。界面语言、纠错说明、回顾报告及所有引导文本，均自动识别用户的母语偏好，以对应语言输出，无需手动配置。对于正在学习目标语言的用户，系统将根据学习目标展示二语对照内容，支持语言范围包括但不限于：中文（简体/繁体）、英文、日文等。
## 四、First Proactive Message from Poke
此消息为 Poke 在用户安装配方后主动发送的第一条欢迎与引导消息，旨在收集用户的母语、目标语言与掌握程度信息，并正式开启个性化语言指导流程。语调专业且亲切。
- 中文版：你好，我是你的 LinguaFlow AI 语言教练。很高兴能降伴你开始这段语言学习之旅。首先，请告诉我：你的母语是什么？目标语言是希望学习或提升哪种语言？以及你希望达到的掌握程度（比如日常口语、商务会话还是流畅表达）？了解这些信息能帮我为你定制最适合的学习体验。
- 英文版：Hello! I am your LinguaFlow AI language coach. I am delighted to accompany you on this language learning journey. To get started, could you tell me: what is your native language, which language are you hoping to learn or improve, and what level of proficiency are you aiming for (for example, everyday conversation, business communication, or fluent expression)? Knowing this will help me tailor the learning experience specifically for you.
## 五、英文 Context（配方完整描述）
LinguaFlow is an AI-powered language coaching assistant that integrates naturally into daily conversations to deliver personalized, adaptive language instruction. The recipe is structured around four core capabilities: intelligent context matching, non-intrusive real-time correction, nightly structured review, and incremental Notion archiving with mastery tracking.
Key capabilities include:
1. Onboarding and profiling: Upon installation, LinguaFlow collects the user's native language, target language, and desired proficiency level. This information initializes a dynamic language profile that is continuously updated based on the user's performance across subsequent interactions.
2. Intelligent context matching: The system analyzes the user's current language proficiency and real-time conversational context to automatically adjust dialogue difficulty and content depth. The adaptive engine ensures content remains at an appropriately challenging level, avoiding material that is either too simple or too advanced.
3. Real-time correction suggestions: When the user produces grammatical errors, incorrect vocabulary, or unnatural phrasing during conversation, the system embeds correction suggestions in a natural, non-disruptive manner. Each suggestion includes the original expression, the recommended alternative, and a brief contextual explanation to reinforce correct language intuition without interrupting conversational flow.
4. Nightly review at 22:00: A structured learning report is automatically compiled and delivered each evening at 10:00 PM. The report categorizes the day's corrections by error type, pairs each mistake with the corrected expression and a usage example, and highlights key grammar points to support retention.
5. Notion incremental archiving with mastery strikethrough: Following each nightly review, all correction items are written to the user's designated Notion database with date-based labeling. As the user subsequently demonstrates mastery of previously flagged vocabulary or grammar points in live conversation, the system automatically applies strikethrough formatting to the corresponding Notion entries, providing a clear and motivating visual record of learning progress.
6. Adaptive communication style (Match the user's chat habits): Poke analyzes the user's historical interaction patterns to identify their preferred communication style, including language choice, tone, level of formality, and use of casual or technical expressions. Coaching messages and daily reminders are dynamically adjusted to match these habits, making the experience feel natural and personally resonant rather than formulaic.
7. Multilingual adaptive output (Match the user's primary language): All correction explanations, review summaries, and guided messages are delivered in the user's native language. For learners targeting a specific language, bilingual comparison content is displayed where contextually appropriate.
## 六、设计原则
1. 不打断对话流程：纠错建议以自然嵌入为首要设计目标，确保学习过程小流畅轻松。
2. 持续进阶：语境匹配机制确保内容始终处于用户掌握边界，避免进度停滞或盲目跳躁。
3. 成就可视化：Notion 划线逻辑将学习轨迹直观干展示，帮助用户建立持续学习的成就感与动力。
4. 尊重个体差异：回顾时间默认设置为 22:00，可根据用户作息规律自行调整，尊重个人节奏。
5. 目标导向：配方全流程以用户的学习目标为导向，内容选取、难度调整及纠错优先级均围绕该目标进行最优化。