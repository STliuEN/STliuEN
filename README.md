<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0B132B,48:1C5D99,100:2A9D8F&text=STliuEN&fontSize=48&fontColor=ffffff&fontAlignY=36&desc=メジロ%20ステルン%20的碎碎念&descAlignY=58&descSize=18&descColor=D9F3EE&animation=fadeIn" alt="STliuEN banner" />

<img width="720" src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&pause=1400&color=1C5D99&center=true&vCenter=true&width=720&lines=AI+Agent+%2F+RAG+%2F+Tool+Calling+%2F+Backend;%E8%AE%A9+AI+%E6%90%AC%E7%A0%96%EF%BC%8C%E4%BD%86%E6%AF%8F%E4%B8%80%E6%AD%A5%E9%83%BD%E8%83%BD%E7%9C%8B%E3%80%81%E8%83%BD%E6%9F%A5%E3%80%81%E8%83%BD%E6%94%B9;%E6%8A%8A%E3%80%8C%E7%9C%8B%E8%B5%B7%E6%9D%A5%E4%B8%8D%E5%A4%AA%E5%AF%B9%E3%80%8D%E5%8F%98%E6%88%90%E8%83%BD%E5%A4%8D%E7%8E%B0%E7%9A%84%E7%94%A8%E4%BE%8B" alt="typing intro" />

<p>
  <img src="https://img.shields.io/badge/CS%20Master's-Student-1C5D99?style=flat-square" alt="CS Master's Student" />
  <img src="https://img.shields.io/badge/Focus-AI%20Agent%20%C2%B7%20RAG%20%C2%B7%20LLM%20Apps-2A9D8F?style=flat-square" alt="Focus" />
  <a href="mailto:sternliu@foxmail.com"><img src="https://img.shields.io/badge/Email-sternliu%40foxmail.com-0A66C2?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

</div>

这里是一些正在折腾、曾经折腾过、以及以后大概率还会继续折腾的东西。

计算机硕士在读，最近写得最多的是 AI Agent、RAG、工具调用、知识库、评测和各种后端胶水代码。比起只让 demo 跑起来，我更在意它后面能不能继续被调试、被观察、被修、被复盘。模型回答错了也挺正常，关键是错在哪里、为什么错、下一轮怎么少错一点。

> TL;DR（给赶时间的面试官）：**Agent / RAG 工程化** · FastAPI + React 全栈 · Go / TypeScript 服务 · 检索链路与评测 · MCP / Skill 工具接入 · 写过图聚类和 NLP 的科研代码

---

## 最近的状态

- 在维护一个校园问答 Agent：评审、发版、排障、加功能，最近给它加上了可切换的网页搜索后端
- 被改图改到吐血，于是写了 [ppt-figure-maker](https://github.com/STliuEN/ppt-figure-maker)，让 AI 画**能编辑的** PPT 图
- 给 DeepSeek Harness 写了两个 DeepSeek 娘模式插件（[蓝色大肥鱼](https://github.com/STliuEN/dsh-mode-intro-card)）
- 在用 5070 Ti 给日摇 / 术力口做多轨分离（[music_list_tools](https://github.com/STliuEN/music_list_tools)），纯属个人爱好
- [Doki-Assistant](https://github.com/STliuEN/Doki-Assistant) 还在慢慢长大

## 正经在做的

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/Doki-Assistant">Doki-Assistant</a></h3>
      <p>个人 AI Agent 工作台：对话、知识库、笔记、记忆中心、翻译、模型配置和工具管理放在同一个工作空间。</p>
      <p>最开始做它完全是因为想要一个实时对话的工作台，方便我在 VRC 里和人打字交流。后来变成了把各种 AI 应用零件塞进同一个运行时的实验场：不只是「问答」，而是把一次回答背后的检索、工具、记忆和上下文都摊开来看。</p>
      <sub><b>FastAPI · React 19 · LangChain · ChromaDB · HyDE / Rerank · MCP · SSE · Ollama</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3>Campus Agent（校园问答助手）</h3>
      <p>面向学生和访客的校园助手（团队私有仓库），只依据已发布的学校资料和开放的校园服务回答，确认不了就说不知道，不拿模型猜测补事实。</p>
      <p>我是核心维护者之一，今年接手后承担了大量日常维护：需求讨论、代码评审、发布与运维、线上问题排查。做过的一些东西：</p>
      <ul>
        <li><b>网页搜索后端可切换</b>：DeepSeek / Exa 双后端，准入时冻结 provider，失败不偷偷换后端；网页引用和校内引用共用一套编号</li>
        <li><b>食堂地图与菜品</b>：基于 tldraw 的平面图编辑器、地图包导入导出、菜品投稿与治理</li>
        <li><b>回答质量</b>：顺着请求链路查无召回、答非所问、引用不清，把「看起来不太对」变成能复现的用例</li>
      </ul>
      <sub><b>Go · TypeScript · Temporal · Hono · React · PostgreSQL · MCP</b></sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/ppt-figure-maker">ppt-figure-maker</a></h3>
      <p>写本子不会画图？导师说「还是第一版好」，但第一版早就淹没在 <code>final_v12_真最终版.pptx</code> 里了？</p>
      <p>一个 AI Skill：AI 用 manifest「图纸」渲染出<b>可编辑的 PPT</b>，你手动改完它还能读回来接着改；每一版都存着，批注自动整理成清单，溢出、重叠、箭头乱飞会被自动检查出来。</p>
      <sub><b>Python · Agent Skill · manifest ⇄ pptx round-trip · 版本快照 · 视觉检查</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/STliuEN/DSAFC">DSAFC</a></h3>
      <p>深度图聚类的公开训练代码：图数据、模型训练、K-means 聚类、ACC / NMI / ARI / F1 评估，以及复现实验需要的脚本。</p>
      <p>科研代码有时候不华丽，但它很诚实：参数、数据、指标、日志，哪一步没对上都很难假装没发生。</p>
      <sub><b>PyTorch · Graph Representation Learning · Clustering</b></sub>
    </td>
  </tr>
</table>

## 兴趣使然的小玩意

| 项目 | 一句话 |
| --- | --- |
| [dsh-mode-intro-card](https://github.com/STliuEN/dsh-mode-intro-card) | DeepSeek Harness Web 的两个 DeepSeek 娘 roleplay 模式：「蓝色大肥鱼」是第一轮直接入戏的全功能编码 Agent；「超级蓝色大肥鱼」会先在后台跑一轮预热再进入角色。偶尔傲娇，始终认真求证 |
| [music_list_tools](https://github.com/STliuEN/music_list_tools) | 本地多模型音轨分离工作台。基于 Pymss CUDA 做六轨分离，带 GPU 单任务锁、运行日志和 manifest，规划中还要统一调度 UVR / Demucs / MSST 这些模型 |

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

想聊项目、实习或者工作机会，欢迎来信 [sternliu@foxmail.com](mailto:sternliu@foxmail.com)

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=100&section=footer&color=0:2A9D8F,52:1C5D99,100:0B132B" alt="footer" />
</div>
