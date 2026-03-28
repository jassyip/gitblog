# 20260321 VoiceJournal AI 配方构思记录

Source URL: https://www.notion.so/329d75c13c6a810fbda3f43dfcadccb7

## Properties

| Property | Value |
| --- | --- |
| title | 20260321 VoiceJournal AI 配方构思记录 |

## Content

本文档详细记录 VoiceJournal AI 配方的构思背景与完整实现逻辑，涵盖定时提醒、语音转写与润色增强、Notion 自动按日期归档等核心模块。
## 一、配方名称
VoiceJournal AI
## 二、核心功能
### 2.1 定时提醒（建议 21:00）
系统默认在每日晙21:00 向用户发送日记提醒，引导其开始当日记录。提醒时间可由用户根据个人作息规律自行调整。对于当天尚未记录的日期，系统将在设定时间居中发出温和提示，确保记录习惯得以持续建立。
### 2.2 语音直录与转写润色
用户可直接发送语音消息录入当日想法与感受，无需打字。系统将语音内容自动转写为文字，并在保留原意的前提下进行适度润色与结构整理，使日记文本更具可读性与完整性。最终转写结果将展示给用户确认，确认后自动归档。
### 2.3 智能标题生成
语音转写与润色完成后，系统将自动分析日记正文，提取当天的核心事件、主要情绪或关键词，并将其与 yyyymmdd 格式的日期组合，生成更具辨识度的页面标题。例如："20260321 身体好转但想跑步的一天"。标题生成结果将与转写内容一并呈现给用户确认，用户可接受系统建议或自行修改后再行归档。
### 2.4 Notion 自动按日期归档
每篇日记完成后，系统将以智能生成的标题为页面名称，自动将日记文本写入用户指定的 Notion 数据库或页面。归档条目包含日期、智能生成标题、选题标签（如果用户指定）以及完整转写正文，形成结构化、可检索的个人日记档案库。
## 三、多语言自适应
系统支持全球化语言自适应（Match the user's primary language）。提醒消息、转写润色输出及所有引导文本，均自动识别用户的母语偏好，以对应语言输出，无需手动配置。支持语言范围包括但不限于：中文（简体/繁体）、英文、日文等。
## 四、First Proactive Message from Poke
此消息为 Poke 在用户安装配方后主动发送的第一条欢迎与引导消息，旨在帮助用户建立对 VoiceJournal AI 功能范围的初始认知，并引导其完成第一次语音记录。语调温和而不失专业感。
Poke 会根据用户平时的聊天习惯自动调整问候的语气与形式，包括但不限于：是否惯用中文或英文、表达风格是否简洁、是否偏好口语化措辞等。系统通过分析用户的历史交互记录识别其沟通风格，并据此生成更具亲和力的个性化提醒，而非采用统一的固定话术。
- 中文版：你好，我是你的 VoiceJournal AI 语音日记助手。很高兴能降伴你记录每一天的思考与感受。我会在每晙21:00 提醒你开始当日日记，将你的语音转写整理后自动归档到你的 Notion 笔记中。现在就发一段语音给我，告诉我你今天的第一个念头吧。
- 英文版：Hello! I am your VoiceJournal AI voice diary assistant. I am here to accompany you in capturing your thoughts and reflections every day. I will remind you each evening at 9:00 PM to start your daily entry, transcribe and refine your voice recordings, and automatically archive everything in your Notion workspace. Go ahead and send me a voice message now — tell me what is on your mind today.
## 五、英文 Context（配方完整描述）
VoiceJournal AI is a voice-driven daily journaling assistant designed to lower the barrier to consistent self-reflection. The recipe integrates scheduled reminders, voice transcription and enhancement, and automatic Notion archiving into a seamless daily routine.
Key capabilities include:
1. Scheduled daily reminder at 21:00: The system sends a gentle journaling prompt to the user each evening at 9:00 PM by default. The reminder time is configurable based on the user's personal schedule. For any day without a completed entry, the reminder fires at the designated time to encourage consistent habit formation.
2. Voice input with transcription and enhancement: Users send voice messages directly without typing. The system transcribes the audio content, then applies light editorial refinement to improve readability and structure while preserving the original intent and tone. The refined transcript is presented to the user for confirmation before archiving.
3. Intelligent title generation: After transcription and refinement are complete, the system automatically analyzes the journal content to extract the core events, dominant emotions, or key themes of the day. It then combines these elements with the date in yyyymmdd format to generate a descriptive and recognizable page title — for example, "20260321 Feeling better but craving a run". The generated title is presented to the user alongside the refined transcript for confirmation. The user may accept the suggestion or modify it before archiving.
4. Notion automatic archiving by date: Upon confirmation, each completed journal entry is written to the user's designated Notion database or page, using the intelligently generated title as the page name. Each archived entry includes the date, the generated title, optional topic tags if specified by the user, and the full refined transcript, forming a structured and searchable personal journal archive.
5. Multilingual adaptive output (Match the user's primary language): All reminders, transcription outputs, and guided messages are automatically delivered in the user's primary language. Language detection is based on interaction history and system language settings. Supported languages include but are not limited to Simplified Chinese, Traditional Chinese, English, and Japanese.
6. Adaptive communication style (Match the user's chat habits): Poke analyzes the user's historical interaction patterns to identify their preferred communication style — including language choice, level of formality, verbosity, and use of casual or technical expressions. Daily reminders and proactive messages are dynamically adjusted to match these habits, making interactions feel natural and personally resonant rather than generic.
## 六、设计原则
1. 低门槛录入：以语音为主要输入方式，年老或打字不便的用户同样能轻松上手。
2. 尊重原意：转写润色以保留用户原意为首要原则，修改仅限于语句结构与可读性。
3. 持续性延伸：定时提醒机制旨在帮助用户建立长期山记录习惯，而非单次不定期的使用。
4. 全局化适配：语言、时区与归档格式均以用户实际环境为准，无需额外配置。