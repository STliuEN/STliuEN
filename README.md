<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0B132B,48:1C5D99,100:2A9D8F&text=STliuEN&fontSize=48&fontColor=ffffff&fontAlignY=36&desc=メジロ%20ステルン%20&descAlignY=58&descSize=18&descColor=D9F3EE&animation=fadeIn" alt="STliuEN banner" />

<p>
  <img src="https://img.shields.io/badge/CS%20Master's-Student-1C5D99?style=flat-square" alt="CS Master's Student" />
  <img src="https://img.shields.io/badge/Focus-AI%20Agent%20%C2%B7%20RAG%20%C2%B7%20LLM%20Apps-2A9D8F?style=flat-square" alt="Focus" />
  <a href="mailto:sternliu@foxmail.com"><img src="https://img.shields.io/badge/Email-sternliu%40foxmail.com-0A66C2?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

</div>

这里是一些正在折腾、曾经折腾过、以及以后大概率还会继续折腾的东西。

计算机硕士在读，业余乐手。平时主要折腾 AI Agent、工具调用、评测和各种后端胶水代码，顺手攒了一堆有用没用的小工具。

> TL;DR：做 LLM 应用落地，检索、工具调用、评测这几段都自己搭过也修过。后端主要写 Python、Go 和 TypeScript。

---

## 最近的状态

- 正在慢慢整理手头的项目，把以前零散的小工具收拢到一起
- 被改图改到吐血，于是写了 [ppt-figure-maker](https://github.com/STliuEN/ppt-figure-maker)
- [Doki-Assistant](https://github.com/STliuEN/Doki-Assistant) 还在慢慢长大

## 正经在做的

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/Doki-Assistant">Doki-Assistant</a></h3>
      <p>个人 AI Agent 工作台：对话、知识库、笔记、记忆中心、翻译、模型配置和工具管理都在同一个工作空间里。</p>
      <p>最开始做这玩意只是想在 VRChat 里方便实时打字交流，后来慢慢演变成了一个实验场——把一次回答背后的检索、工具、记忆和上下文都摊开来看。</p>
      <sub><b>FastAPI · React 19 · LangChain · ChromaDB · HyDE / Rerank · MCP · SSE · Ollama</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3>Campus Agent（校园智能体）</h3>
      <p>学校的校园问答 Agent，团队一起做的，私有仓库就不放链接了。本质上是个 Multi-Agent 校园小助手，帮大家查查校内信息和日常服务。</p>
      <p>我是维护者之一。接手之后主要负责新工具接入、效果评测和日常修修补补，也算是在课题组之外练手维护一个真正有人在用的线上项目。</p>
      <sub><b>Go · TypeScript · Temporal · Hono · React · PostgreSQL · MCP</b></sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/ppt-figure-maker">ppt-figure-maker</a></h3>
      <p>写本子不会画图，改到十几版，导师还是说「第一版好」，可第一版早淹没在 <code>final_v12_真最终版.pptx</code> 里了。</p>
      <p>一个 AI Skill：AI 写一份 manifest 渲染成<b>可编辑的 pptx</b>；你手改完它能读回来接着改，每一版都留着。字溢出、框叠在一起、箭头乱飞这类毛病，它会自己挑出来。</p>
      <sub><b>Python · Agent Skill · manifest ⇄ pptx round-trip · 版本快照 · 视觉检查</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/DSAFC">DSAFC</a></h3>
      <p>深度图聚类的公开训练代码，以及复现实验需要的脚本。</p>
      <p>科研代码有时候不华丽，但它很诚实：参数、数据、指标、日志，哪一步没对上都很难假装没发生。</p>
      <sub><b>PyTorch · Graph Representation Learning · Clustering</b></sub>
    </td>
  </tr>
</table>

## 兴趣使然的小玩意

| 项目 | 一句话 |
| --- | --- |
| [dsh-mode-intro-card](https://github.com/STliuEN/dsh-mode-intro-card) | DeepSeek Harness Web 的两个 DeepSeek 娘 roleplay 模式：「蓝色大肥鱼」是第一轮直接入戏的全功能编码 Agent；「超级蓝色大肥鱼」会先在后台跑一轮预热再进入角色。偶尔傲娇，始终认真求证 |
| [music_list_tools](https://github.com/STliuEN/music_list_tools) | 给乐队做的本地多轨分离工作台，纯属个人爱好。跑 BS-Roformer 把一首歌拆成六轨，每次运行的日志和 manifest 都留着，还顺手接了个 stdio MCP 服务方便 Agent 直接调用 |

<details>
<summary><b>以前挖的坑（点开看看）</b></summary>

<br />

**[VirtualTryonApplycation](https://github.com/STliuEN/VirtualTryonApplycation)**：早一些的虚拟试衣项目，链路是图像预处理 → 人体姿态 / 解析 → 掩膜生成 → VITON-HD 合成，再接 Java 后端和 Android 端。现在回头看还有很多地方能整理得更好，但这是我第一次比较完整地把模型推理、服务调用和应用入口串起来，还产出了一个软著。虽然已经不做 CV 了，还是值得纪念。
<sub>OpenPose · Graphonomy · VITON-HD · Java · Android</sub>

**[Bert-Base-Chinese-Police-Analysing](https://github.com/STliuEN/Bert-Base-Chinese-Police-Analysing)**：中文文本分析和分类的 Notebook，包括清洗、关键词抽取、BERT 微调、结果分析和可视化。那段时间主要在理解 NLP 项目里「数据处理」到底占多大比重。后来发现，很多模型问题最后都会绕回数据、标签、样例和评估方式。
<sub>BERT · Chinese NLP · Text Classification · Jupyter</sub>

</details>

## 常用工具

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" alt="Django" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Temporal-000000?style=flat-square&logo=temporal&logoColor=white" alt="Temporal" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/RAG-2F80ED?style=flat-square" alt="RAG" />
  <img src="https://img.shields.io/badge/MCP-111827?style=flat-square" alt="MCP" />
  <img src="https://img.shields.io/badge/ChromaDB-F54E42?style=flat-square" alt="ChromaDB" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/BERT-8A2BE2?style=flat-square" alt="BERT" />
  <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white" alt="Java" />
</p>

不算什么豪华全家桶，只是目前经常碰到、也还在继续补熟的东西。

<div align="center">
  <img height="170" src="https://github-stats-extended.vercel.app/api/top-langs/?username=STliuEN&layout=compact&hide_border=true&hide=powershell" alt="Top languages" />
  <img height="170" src="https://streak-stats.demolab.com?user=STliuEN&hide_border=true&background=00000000&ring=1C5D99&fire=2A9D8F&currStreakLabel=1C5D99" alt="GitHub streak" />
  <br />
  <img width="94%" src="https://ghchart.rshah.org/1C5D99/STliuEN" alt="Contribution chart" />
</div>

## 碎碎念

我喜欢那种能留下痕迹的系统：日志能查，错误能复现，回答有来源，改动有理由。
也喜欢把一个模糊的问题慢慢拆小，拆到终于能写代码、能测、能改。

有些仓库还在整理，有些代码现在看会觉得青涩，但也挺好：起码知道自己做的东西不够好，也算是一种进步。

有好玩的项目想聊，或者单纯路过打个招呼，欢迎来信 [sternliu@foxmail.com](mailto:sternliu@foxmail.com)。

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=100&section=footer&color=0:2A9D8F,52:1C5D99,100:0B132B" alt="footer" />
</div>
