# MintLingo (背单词小程序)

MintLingo 是一款基于浏览器的纯前端单页面应用，致力于为您提供流畅、无广告、完全本地化、且功能极其丰富的英语学习环境。您的所有学习数据均安全地保存在本地。

---

## 🌟 核心亮点架构
- **零后端依赖**：Vue 3 + Tailwind CSS 构建，所有数据基于浏览器 IndexedDB (Dexie.js) 离线存储。
- **SM-2 间隔重复**：智能规划复习频率，对抗遗忘曲线。
- **键盘流极客体验**：支持快捷键一键发音、盲按标记熟练度，沉浸感极强。
- **AI 原生集成**：内置大模型 API 接口连接通道（如 DeepSeek），实现智能场景生成、专业解析释疑。

---

## 🧩 核心功能全景解析

MintLingo 共包含 8 大核心功能模块，满足从词库建立、计划执行到效果反馈的完整闭环：

### 1. 学习统计 (Dashboard)
- **学习热力图 (Heatmap)**：GitHub 风格的打卡记录网格，直观呈现每天的学习强度与坚持天数。
- **遗忘预测曲线**：根据当前队列，智能预测未来 7 天的待复习词汇量分布，帮助合理规划日程。
- **核心数据看板**：直观展示总词汇量、已掌握词数以及累计学习进度。
<img width="1487" height="749" alt="image" src="https://github.com/user-attachments/assets/87eb28e1-cc6f-47f7-b8d0-5ba25a036550" />

### 2. 今日计划 (Plan)
- **自适应任务下发**：自由设定每日新词配额，算法自动混排并穿插需要复习的旧词。
- **备考冲刺模式**：开启后，系统在学习后期将自动停止引入新词，把最后 1/3 的周期全留给纯复习巩固，防止考前遗忘。
<img width="1508" height="747" alt="image" src="https://github.com/user-attachments/assets/92045d52-9418-4a3f-b0dd-33a92a19c5cc" />

### 3. 背单词核心 (Words)
这是整个应用的主战场，基于经典的双面卡片设计：
- **快捷键交互**：`1-不认识`、`2-模糊`、`3-认识`、`4-简单`，以及 `P-一键发音`，彻底解放鼠标。
- **语音引擎支持**：调用浏览器原生 TTS 引擎，纯正美音/英音朗读，支持自动发音。
- **跟读录音机**：内置麦克风录音功能，学习时随时录下自己的发音并回放对比。
- **AI 动态释疑**：遇到词典未收录的冷僻用法，可一键请求 AI 为你生成“专业词源解释”或“生活场景例句”。
<img width="1493" height="747" alt="image" src="https://github.com/user-attachments/assets/2052eb08-381c-4736-bf6a-72813fa898cb" />
<img width="1497" height="745" alt="image" src="https://github.com/user-attachments/assets/2c402a08-cdfe-4387-a21d-485e2d296209" />

### 4. 复习队列 (Queue)
专门针对积压复习单词打造的高效清理模式：
- **释义隐藏开关**：一键使中文释义变模糊，仅在鼠标悬浮时显示，模拟高效闪卡自测。
- **单行极速复习**：点击每行单词专属的绿色“✅”，不进入背词卡片即可直接将其打入下一个记忆周期。
- **批量多选操作**：积压过多时，可勾选数十行单词“一键标记为认识”，快速清空心理负担。
<img width="1499" height="743" alt="image" src="https://github.com/user-attachments/assets/fecd5c50-f483-468a-bef3-fe9f433c4e29" />
<img width="1487" height="743" alt="image" src="https://github.com/user-attachments/assets/c281d8a6-39a4-4871-9b10-3257ac2ed8d4" />

### 5. 例句库 (Sentences)
- **长难句摘录**：收集在外部阅读中遇到的好句子或 AI 生成的经典例句，支持独立管理与复习。
- **折叠背诵**：可将长句折叠收起，通过手动默写或脑内回忆进行自我验证。
<img width="1495" height="745" alt="image" src="https://github.com/user-attachments/assets/76604c64-85c3-4600-a14e-390b91cd20f1" />

### 6. 导入词书与管理 (Wordbooks)
- **多格式支持**：支持拖拽/上传 `.txt`、`.csv` 或 `.json` 文件，系统瞬间解析生成个人词库。
- **词书级管理**：支持创建无数本独立词书。内置强大的词库增删改查、搜索过滤机制。
- **沉浸阅读查词 (电子书支持)**：内置阅读器，支持导入英文原文材料阅读，实现点击查词、划线翻译与生词实时入库。
<img width="1489" height="747" alt="image" src="https://github.com/user-attachments/assets/e4b6ab1a-e83f-4f4b-8fbc-87284b7ba7ea" />

### 7. AI 场景互动 (Scenarios)
- **情景化语言应用**：输入你感兴趣的话题或所处场景（如“在机场过海关”、“用英语买咖啡”），AI 会根据你的当前词书生成一段沉浸式的对话或小故事，帮助你在语境中巩固今天背诵的单词。
<img width="1495" height="743" alt="image" src="https://github.com/user-attachments/assets/b861c7a2-5052-4f48-b876-219202253d2e" />
<img width="1493" height="745" alt="image" src="https://github.com/user-attachments/assets/61088e95-a9c3-4d13-bec1-ca950a1d5037" />

### 8. 系统设置 (Settings)
- **API 接口配置**：自由填入你自己的大模型 API 地址和 Key（如 OpenAI 或 DeepSeek），保障 AI 辅助功能顺畅运行。
<img width="1497" height="743" alt="image" src="https://github.com/user-attachments/assets/9479030e-0000-4be9-86cc-f584a6961a3c" />
- **自定义主题**：自由更换界面、按钮与卡片的主题色（如马卡龙色系）。
<img width="1497" height="745" alt="image" src="https://github.com/user-attachments/assets/5534e510-a7df-4a9a-a91a-36febf5e06f8" />
<img width="1493" height="739" alt="image" src="https://github.com/user-attachments/assets/0789577b-609d-4b61-9aa3-b2c0d836a12d" />
<img width="1507" height="753" alt="image" src="https://github.com/user-attachments/assets/3f4beebc-af7d-4130-b34e-d59e65d613ec" />
- **数据安全堡垒**：提供一键导出全库数据（JSON格式本地备份），无惧浏览器缓存清理；支持换机后一键恢复。
<img width="745" height="385" alt="image" src="https://github.com/user-attachments/assets/fc252787-52b3-41f0-9148-2fca543f2473" />


---

## 📖 极速上手说明

1. 下载或 Clone 本项目文件夹到本地。
2. **无需构建，无需依赖包**：直接使用现代浏览器（推荐 Chrome 或 Edge）双击打开 `index.html` 即可开始使用。
3. 如果需要备份数据或防止浏览器意外清理存储，请养成在“系统设置”页面定期导出的习惯。
