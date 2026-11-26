<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0B132B,48:1C5D99,100:2A9D8F&text=STliuEN&fontSize=48&fontColor=ffffff&fontAlignY=36&desc=メジロ%20ステルン%20·%20AI%20Agent%20%26%20LLM%20Systems&descAlignY=58&descSize=16&descColor=D9F3EE&animation=fadeIn" alt="STliuEN banner" />

<p>
  <img src="https://img.shields.io/badge/CS%20Master's-Research%20%26%20Engineering-1C5D99?style=flat-square" alt="CS Master's Student" />
  <img src="https://img.shields.io/badge/Focus-Agentic%20AI%20%C2%B7%20RAG%20%C2%B7%20Systems-2A9D8F?style=flat-square" alt="Focus" />
  <a href="mailto:sternliu@foxmail.com"><img src="https://img.shields.io/badge/Email-sternliu%40foxmail.com-0A66C2?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

</div>

计算机科学与技术硕士在读，专注于 **大模型应用架构、Agentic Workflow、大规模检索与自动化评测**，兼顾 Python / Go / TypeScript 全栈工程实现与图形学/3D 内容创作。

> **TL;DR**：擅长在复杂约束下设计**高可靠、可验证、可观测**的 AI 系统——将模型的语义推理能力与确定性编译、规则引擎、状态机及自动化验收解耦协同。

---

## 核心技术方向

| 领域 | 工程实践与架构关注点 |
| :--- | :--- |
| **可控 Agent 架构** | Planning → Deterministic Compilation / Generation → Independent Verifier 分离架构；JSON Schema 约束输出与代码级状态机管理；控制面与数据面解耦 |
| **大规模检索与 Text-to-SQL** | 百表千字段级 Schema 紧凑表示压缩（大幅降低上下文冗余并保留 100% 召回）；基于安全边界的防幻觉机制；Hybrid RAG（BM25 + Dense + HyDE + Rerank） |
| **多模态与证据链溯源** | 服务解耦与版本化交接契约设计；业务数据流与证据链分离，实现全链路可回溯至原始文档位置；确定性逻辑穷举与端到端回归评测 |

---

## 代表项目与研究

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/Doki-Assistant">Doki-Assistant</a></h3>
      <p><b>全栈 AI Agent 运行时与多模型协作工作台</b></p>
      <p>将对话、知识库、记忆系统、实时翻译、多模型路由与外部工具整合为统一运行时；支持混合检索（BM25 + 向量 + HyDE + Cross-Encoder Rerank）、MCP 工具接入与 SSE 流式可观测链路，让每次推理与工具调用过程完全透明、可调试。</p>
      <sub><b>FastAPI · React 19 · LangChain · ChromaDB · MCP · SSE · Ollama</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3>Campus Agent（线上校园智能体）</h3>
      <p><b>高可用 Multi-Agent 系统核心贡献者（累计 ~10,000 次访问）</b></p>
      <p>面向真实校园流量持续迭代核心 Agent 能力与线上稳定性：基于 <b>Go / Temporal</b> 分布式工作流实现结构化服务查询（复用 PostgreSQL 排班数据），扩建端到端评测集（工具问答准确率达 0.8），主导多环境验收与 Bad Case 闭环。</p>
      <sub><b>Go · TypeScript · Temporal · Hono · React · PostgreSQL · MCP</b></sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/ppt-figure-maker">ppt-figure-maker</a></h3>
      <p><b>基于双向 Manifest 同步的科研绘图 Agent Skill</b></p>
      <p>解决学术图表“多轮修改不可逆”的痛点：通过结构化 Manifest 与<b>可编辑 PPTX</b> 的双向 Round-trip 同步，实现版本快照管理；内置文本溢出、图元重叠与箭头拓扑的视觉自动化自检，形成“生成—微调—回读”闭环。</p>
      <sub><b>Python · Agent Skill · Manifest ⇄ PPTX Round-trip · Visual Self-Check</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/DSAFC">DSAFC（图深度学习研究）</a></h3>
      <p><b>不完美图上的自适应双结构融合深度图聚类</b></p>
      <p>针对真实图数据中普遍存在的噪声边与缺边问题，提出自适应融合原始拓扑与特征构造结构的深度图聚类框架（论文投稿 <i>Applied Intelligence</i>）；开源完整 PyTorch 训练管线、多数据集复现脚本与评估基准。</p>
      <sub><b>PyTorch · Graph Representation Learning · Deep Clustering</b></sub>
    </td>
  </tr>
</table>

---

## 工程工具链与极客探索

| 项目 / 方向 | 核心实现与技术亮点 |
| :--- | :--- |
| **多模型网关与 Agent 编排** | 自建 OpenAI 兼容网关实现“规划—实现—审阅”多模型分层路由，按任务复杂度与成本动态分配推理资源；封装为可复用 Agent Skill 并在隔离沙箱中跑通 Codex CLI 调用链路 |
| **[music_list_tools](https://github.com/STliuEN/music_list_tools)** | 基于 **BS-Roformer** 的本地六轨音频分离工作台，自研**零依赖 stdio MCP 服务**（暴露模型列表、环境检查、分离规划、下载、异步提交、状态查询 6 项标准接口），支持代码 Agent 端到端自主调度 |
| **Unity3D / VRChat 与游戏 Mod** | 使用 Unity3D 与 Blender 开发 **20 个高精度虚拟模型（Avatar）** 及 **3 张在线交互地图**，定制插件化资产工作流；参与多款游戏 Mod 的资源解包复现与三方扩展设计 |
| **[dsh-mode-intro-card](https://github.com/STliuEN/dsh-mode-intro-card)** | 为 DeepSeek Harness Web 设计的双态编码 Agent 角色模式（即时全功能编码 / 后台预热协同），兼顾交互趣味与严谨求证链路 |

<details>
<summary><b>早期全栈与算法原型归档（点击展开）</b></summary>

<br />

- **[VirtualTryonApplycation](https://github.com/STliuEN/VirtualTryonApplycation)**：移动端智能虚拟试衣系统（软件著作权），打通“图像预处理 → 人体姿态与解析 → 掩膜生成 → **VITON-HD** 图像合成 → Java 后端与 Android 端侧交互”完整推理链路。`OpenPose · Graphonomy · VITON-HD · Java · Android`
- **[Bert-Base-Chinese-Police-Analysing](https://github.com/STliuEN/Bert-Base-Chinese-Police-Analysing)**：中文舆情分析与事件分类系统，微调 **BERT** 完成粗细两级文本分类（交叉验证精度 89%），结合词性过滤构建关键词可视化管线。`BERT · Chinese NLP · Text Classification`

</details>

---

## 技术栈

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Temporal-000000?style=flat-square&logo=temporal&logoColor=white" alt="Temporal" />
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/RAG%20%26%20Text--to--SQL-2F80ED?style=flat-square" alt="RAG & Text-to-SQL" />
  <img src="https://img.shields.io/badge/MCP-111827?style=flat-square" alt="MCP" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/ChromaDB-F54E42?style=flat-square&logo=chromadb&logoColor=white" alt="ChromaDB" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
  <img src="https://img.shields.io/badge/Unity%203D-000000?style=flat-square&logo=unity&logoColor=white" alt="Unity 3D" />
</p>

<div align="center">
  <img height="170" src="https://github-stats-extended.vercel.app/api/top-langs/?username=STliuEN&layout=compact&hide_border=true&hide=powershell" alt="Top languages" />
  <img height="170" src="https://streak-stats.demolab.com?user=STliuEN&hide_border=true&background=00000000&ring=1C5D99&fire=2A9D8F&currStreakLabel=1C5D99" alt="GitHub streak" />
  <br />
  <img width="94%" src="https://ghchart.rshah.org/1C5D99/STliuEN" alt="Contribution chart" />
</div>

---

## 关于工程态度

我相信好的 AI 系统应当是**可解释、可复现、可演进**的：每次回答有证据溯源，每次状态流转有契约约束，每次 Bad Case 都能沉淀为自动化测试。

如果你对 Agentic AI、检索架构、开源工具链或有趣的技术想法感兴趣，欢迎随时交流：[sternliu@foxmail.com](mailto:sternliu@foxmail.com)。

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=100&section=footer&color=0:2A9D8F,52:1C5D99,100:0B132B" alt="footer" />
</div>
