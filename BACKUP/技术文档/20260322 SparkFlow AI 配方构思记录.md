# 20260322 SparkFlow AI 配方构思记录

Source URL: https://www.notion.so/32bd75c13c6a8186874df9fb313f0ae6

## Properties

| Property | Value |
| --- | --- |
| title | 20260322 SparkFlow AI 配方构思记录 |

## Content

本文档详细记录 SparkFlow AI 配方的构思背景与完整实现逻辑，涵盖灵感捕捉、碎片聚合、自动孔化与语义查重等核心模块。
## 一、配方名称
SparkFlow AI
## 二、核心逻辑设计
### 2.1 灵感捕捉
用户可通过语音或文字随时向 SparkFlow AI 发送灵感碎片，无需整理、无需归类。系统接收内容后自动执行以下处理：语音内容进行转写，文字内容直接录入；自动打上时间戳，记录当前日期与来源标识；将片段到临时储存区，等待后续聚合处理。捕捉过程应尽可能轻量，确保用户在任何场景下都能不加思索地实时记录。
### 2.2 碎片聚合
系统定期对用户的全部灵感碎片执行聚合分析，通过语义理解模型识别内容之间的主题关联、逆辑连接与潜在展开方向。具有相似语义的碎片自动归类至同一主题群组，跨主题的内容则以关联边连接。续层面呈现结果时，系统将主动提示用户审阅聚合内容，用户可确认合并、拆分或调整归类。
### 2.3 语义查重
每次录入新癵感碎片时，系统将其与历史库中所有已存内容进行语义相似度计算。若检测到重复度超过阈值的内容，系统将主动提示用户：对当前输入与历史確展示内容的差异琄面，并询问用户是否希望与已有内容合并、以新视角补充，或保留为独立记录。语义查重机制确保内容库不冗余、磁领清晰。
### 2.4 自动孔化
系统为每个已归档的主题群组设置独立的孔化周期。孔化周期内，系统将在适当时间自动重新呢醒这些确思，以问题引导或提示推算的形式推动用户进一步深化思考。孔化时间可由用户配置，默认为 24 小时内推进一次。对于长期未能深化的主题，系统将定期增强呢醒频率，直至用户将其标记为「暂缓」或「已完成」。
### 2.5 Notion 增量归档
用户确认归档后，各主题群组以结构化页面的形式写入用户指定的 Notion 数据库。每个页面包含：主题标题、创建日期、关联碎片列表、当前孔化状态及 AI 生成的推展建议。新癵感增加时自动增量更新对应页面，无需重建。
### 2.6 多语言自适应
系统支持全球化语言自适应（Match the user's primary language）。所有呢醒提示、聚合报告、孔化建议及引导消息，均自动识别用户的母语偏好并以对应语言输出。
## 三、Welcome Message 欢迎语
此消息为 Poke 在用户安装配方后主动发送的第一条欢迎与引导消息，语调专业而不失亲切。
- 中文版：你好，我是你的 SparkFlow AI 灵感管家。从现在起，你只需把每个闪光的想法直接说给我就好——不用整理，不用分类。我会帮你将它们自动聚合、查重、孔化，并在最合适的时刻重新呢醒你思考。现在，就把最近脑海里转着的一个想法发给我吧。
- 英文版：Hello! I am your SparkFlow AI inspiration manager. From now on, all you need to do is send me your ideas the moment they surface — no need to organize, categorize, or structure anything. I will automatically cluster your thoughts, check for overlaps with existing ideas, and gently incubate them over time, resurfacing them when the moment is right. Go ahead and share the first idea that has been on your mind lately.
## 四、英文 Context（配方完整描述）
SparkFlow AI is an intelligent inspiration management assistant designed to eliminate the friction of capturing, organizing, and developing creative ideas. The recipe operates on a capture-first, structure-later principle: users send raw thoughts freely, and the system handles all downstream organization, deduplication, clustering, and incubation automatically.
Key capabilities include:
1. Frictionless idea capture: Users submit inspiration fragments at any time via voice or text, with no requirement to organize or categorize upfront. Voice input is automatically transcribed. Each fragment is timestamped, tagged with a source identifier, and placed in a temporary staging area pending further processing.
2. Semantic clustering and aggregation: The system periodically analyzes all stored fragments using a semantic understanding model to identify thematic relationships, logical connections, and potential expansion directions. Fragments with high semantic similarity are automatically grouped into thematic clusters. Cross-theme associations are preserved as relational links. Users are notified when clustering is complete and can confirm merges, split clusters, or adjust groupings.
3. Semantic deduplication: Each new fragment is evaluated against the full existing content library using semantic similarity scoring. When the similarity exceeds a defined threshold, the system surfaces both the new input and the existing related content side by side, and asks the user whether to merge them, add a new perspective, or retain as a separate entry. This mechanism ensures the knowledge base remains clean, non-redundant, and navigable.
4. Automated incubation: Each confirmed thematic cluster is assigned an independent incubation cycle. During incubation, the system resurfaces the cluster at appropriate intervals using question prompts or AI-generated expansion suggestions to encourage deeper thinking. The default incubation cadence is once per 24 hours. Clusters that remain undeveloped over time receive progressively more frequent nudges until the user marks them as "on hold" or "completed".
5. Notion incremental archiving: Upon user confirmation, each thematic cluster is written to the user's designated Notion database as a structured page. Each page includes the cluster title, creation date, a list of associated fragments, current incubation status, and AI-generated expansion suggestions. When new fragments are added to an existing cluster, the corresponding Notion page is incrementally updated without requiring the page to be recreated.
6. Adaptive communication style (Match the user's chat habits): Poke analyzes the user's historical interaction patterns to identify their preferred tone, language, and level of formality. Incubation prompts, aggregation reports, and all proactive messages are dynamically adjusted to feel natural and personally resonant.
7. Multilingual adaptive output (Match the user's primary language): All nudges, summaries, and guided messages are delivered in the user's primary language. Language detection is based on interaction history and system language settings. Supported languages include but are not limited to Simplified Chinese, Traditional Chinese, English, and Japanese.
## 五、设计原则
1. 捕捉优先，结构滓后：用户在输入时不承担任何组织负担，所有结构化工作均由系统在后台完成。
2. 语义优先于关键词：聚合与查重均基于语义理解，而非字面匹配，确保内容相似性的判断准确而灵活。
3. 孔化式驱动：系统不仅存录想法，更主动推动思考深化，帮助用户将碎片灵感演变为成熟想法。
4. 用户权威保留：对于所有聚合、查重处理与归档操作，系统均呈送建议而非直接执行，用户始终拥有最终确认权。
5. 全局化适配：语言、时区与通知格式均以用户实际环境为准，无需额外配置。