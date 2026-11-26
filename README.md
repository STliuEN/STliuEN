<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=210&color=0:0B132B,48:1C5D99,100:2A9D8F&text=STliuEN&fontSize=48&fontColor=ffffff&fontAlignY=36&desc=メジロ%20ステルン%20·%20Building%20Evaluable%20AI%20Systems&descAlignY=58&descSize=16&descColor=D9F3EE&animation=fadeIn" alt="STliuEN banner" />

<p>
  <img src="https://img.shields.io/badge/CS_Master's-2028-1C5D99?style=flat-square" alt="CS Master" />
  <img src="https://img.shields.io/badge/Focus-Agentic_AI_·_RAG_·_Eval-2A9D8F?style=flat-square" alt="Focus" />
  <a href="mailto:sternliu@foxmail.com"><img src="https://img.shields.io/badge/Mail-sternliu%40foxmail.com-181717?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

</div>

```text
> whoami
CS Master's student · Amateur Musician · Systems Tinkerer
把大模型放进确定性边界里：模型负责语义与复杂生成，代码负责状态机、规则引擎与证据溯源。
```

---

### ⚡ 正在打磨与开源的项目

- **[Doki-Assistant](https://github.com/STliuEN/Doki-Assistant)** — *Personal AI Agent Runtime & Workbench*  
  最初是为了在 VRChat 里方便打字翻译，后来长成了一个全栈 Agent 实验场：把多模型路由、Hybrid RAG（BM25 + Dense + HyDE + Rerank）、记忆中心、MCP 工具和 SSE 流式输出塞进同一套可观测运行时里。  
  `FastAPI` · `React 19` · `LangChain` · `ChromaDB` · `MCP`

- **Campus Agent** *(Private)* — *Multi-Agent Campus Assistant (~10k visits)*  
  校内在线运行的 Multi-Agent 助手。在 **Go / Temporal** 分布式工作流里接了结构化排班查询（PostgreSQL），把工具问答评测集扩到 0.8 准确率，顺带治好了不少线上 Bad Case。  
  `Go` · `TypeScript` · `Temporal` · `PostgreSQL`

- **[ppt-figure-maker](https://github.com/STliuEN/ppt-figure-maker)** — *Round-trip Research Figure Agent Skill*  
  被改图改到吐血后的产物：AI 生成结构化 Manifest 渲染成**可编辑 PPTX**，你手改完它还能读回来接着改，自带版本快照和文字溢出 / 重叠 / 箭头乱飞的视觉自检。  
  `Python` · `Agent Skill` · `Manifest ⇄ PPTX`

- **[DSAFC](https://github.com/STliuEN/DSAFC)** — *Deep Graph Clustering on Imperfect Graphs*  
  面向真实图里“噪声边 & 缺边”的自适应双结构融合深度图聚类（投稿 *Applied Intelligence*）。科研代码不花哨但很诚实：哪组超参、哪份日志没对上都藏不住。  
  `PyTorch` · `Graph Learning` · `Clustering`

---

### 🏗️ 私有生产环境下的 Agent 架构实践

在企业级业务中台打磨过几套跑在真实流量上的智能体系统，核心思路只有一条：**不把所有赌注都押在 Prompt 上**。

- **大规模数仓 Text-to-SQL**：面对 **83 表 / 1,886 字段**且缺外键关系的 Doris 数仓，设计 `Planning → Deterministic Compilation / LLM Gen → Independent Verifier` 混合架构；紧凑 Schema 压缩减少 55%–66% 提示体积，未确认关系禁写 JOIN，单轮调用压到 2–3 次、首轮响应压进 1 分钟内。
- **流式规则异常研判**：用“先分类、再比较”两阶段引擎 + 五态语义区分数据脏污与真实异常；做控制面与数据面分离后，工作流从 81 节点收敛至 17 节点，节点输出从 `128 MB → 1.1 MB`、耗时降 **74%**。
- **多模态合规稽核**：将 OCR 抽取与稽核报告拆成双服务（`OCR_HANDOFF_1.0`），业务流与证据链分离可回溯至原文位置，代码确定性判定并穷举 **16,384** 种状态组合验收，模型只负责写报告。

---

### 🛠️ 极客副产物 & 兴趣使然

- **多模型编排网关 & Codex CLI Skill**：自建 OpenAI 兼容网关，按“规划 / 审阅 / 轻量执行”分层调度不同模型，在隔离沙箱跑通代码 Agent 自动派活。
- **[music_list_tools](https://github.com/STliuEN/music_list_tools)**：给乐队写的本地六轨音频分离工作台（**BS-Roformer**），手搓了一个**零依赖 stdio MCP 服务**（6 个标准工具接口），让 Agent 能自己查环境、规划、提交并轮询分离任务。
- **Unity3D / VRChat & Modding**：用 Unity 与 Blender 捏过 **20 个虚拟模型（Avatar）**、搭过 **3 张公开地图**，也折腾过《赛马娘》《战争雷霆》等游戏的 Mod 资源复现。
- **[dsh-mode-intro-card](https://github.com/STliuEN/dsh-mode-intro-card)**：DeepSeek Harness Web 的双态编码 Agent 角色卡（「蓝色大肥鱼」直接入戏 / 「超级蓝色大肥鱼」后台预热后入戏）。

<details>
<summary>📦 以前挖的坑（VirtualTryon / BERT NLP）</summary>

- **[VirtualTryonApplycation](https://github.com/STliuEN/VirtualTryonApplycation)**：移动端虚拟试衣原型（拿过一个软著），串通 `OpenPose → Graphonomy → VITON-HD → Java 后端 → Android`。
- **[Bert-Base-Chinese-Police-Analysing](https://github.com/STliuEN/Bert-Base-Chinese-Police-Analysing)**：中文事件分类与舆情分析 Notebook（BERT 微调交叉验证 89%），踩坑后明白“大多数模型问题最终都是数据问题”。

</details>

---

### 🧰 Core Stack

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/MCP-111827?style=flat-square" alt="MCP" />
</p>

<div align="center">
  <img height="165" src="https://github-stats-extended.vercel.app/api/top-langs/?username=STliuEN&layout=compact&hide_border=true&hide=powershell,jupyter%20notebook" alt="Top languages" />
  <img height="165" src="https://streak-stats.demolab.com?user=STliuEN&hide_border=true&background=00000000&ring=1C5D99&fire=2A9D8F&currStreakLabel=1C5D99" alt="GitHub streak" />
  <br />
  <img width="94%" src="https://ghchart.rshah.org/1C5D99/STliuEN" alt="Contribution chart" />
</div>

---

<div align="center">
  <sub>喜欢能留下痕迹的系统：日志可查、错误可复现、回答有来源、改动有理由。欢迎交流 → <a href="mailto:sternliu@foxmail.com">sternliu@foxmail.com</a></sub>
  <br /><br />
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=95&section=footer&color=0:2A9D8F,52:1C5D99,100:0B132B" alt="footer" />
</div>
