# STliuEN的碎碎念

这里是一些正在折腾、曾经折腾过、以及以后大概率还会继续折腾的东西。

最近写得比较多的是 AI Agent、RAG、工具调用、知识库、评测和各种后端胶水代码。比起只让 demo 跑起来，我更在意它后面能不能继续被调试、被观察、被修、被复盘。模型回答错了也挺正常，关键是错在哪里、为什么错、下一轮怎么少错一点。

## 最近的状态

北京不是个人待的地方！

- 在把 Agent/RAG 的链路拆得更清楚：入口、上下文、检索、工具、证据、回答、日志
- 在补一些工程基本功：接口、数据表、缓存、鉴权、流式返回、测试和文档
- 在整理自己的项目，让它们不只是能跑，也能让别人看懂当时到底想解决什么
- 偶尔也会回头看看 CV、NLP、图聚类和一些游戏工具链相关的旧坑


## 放几个项目

### [Doki-Assistant](https://github.com/STliuEN/Doki-Assistant)

一个个人 AI Agent 工作台。里面有对话、知识库、笔记、记忆中心、翻译、模型配置和工具管理。最开始做这玩意完全是因为想要一个实时对话的工作台方便我在vrc和人打字交流

它现在更像一个把很多 AI 应用零件放到同一个运行时里的实验场：FastAPI 后端、React 前端、LangChain Agent、ChromaDB 检索、MCP 工具接入、SSE 事件流、用户上下文隔离。  
我比较喜欢这个项目的一点是，它不只是在“问答”，而是在试着把一次回答背后的工具、检索、记忆和上下文都摊开来看。

### Campus Wiki Agent/RAG System

一个校园信息问答 Agent/RAG 系统的维护和工程化经历，现在还在做，刚接手，只简单记一下这段工作里比较有意思的部分：

- 顺请求链路，看一个问题从入口到 Agent 再到检索和回答生成发生了什么
- 查无召回、答非所问、引用不清楚这类问题
- 整理 evidence、Bad Case 和评测用例
- 把“这个回答看起来不太对”变成更具体、后续能复现的问题

### [DSAFC](https://github.com/STliuEN/DSAFC)

深度图聚类相关的公开训练代码。主要是图数据、模型训练、K-means 聚类、ACC/NMI/ARI/F1 指标评估，以及一些实验复现需要的脚本。

科研代码有时候不华丽，但它很诚实：参数、数据、指标、日志，哪一步没对上都很难假装没发生。顺带一提审稿也太慢了！we了好久都没动静

### [VirtualTryonApplycation](https://github.com/STliuEN/VirtualTryonApplycation)

早一些的虚拟试衣项目。大致链路是图像预处理、人体姿态/解析、掩膜生成、VITON-HD 合成，再接 Java 后端和 Android 端。

现在回头看，里面有不少地方还能整理得更好，尤其 README 编码和项目结构。但它确实是我第一次比较完整地把模型推理、服务调用和一个应用入口串起来，不过产出了一个软著还可以。虽然已经不做cv方向了但是还是值得纪念的事情。

### [Bert-Base-Chinese-Police-Analysing](https://github.com/STliuEN/Bert-Base-Chinese-Police-Analysing)

中文文本分析和分类的 Notebook。包括文本清洗、关键词抽取、BERT 微调、分类结果分析和可视化。

那段时间主要在理解 NLP 项目里“数据处理”到底占多大比重。后来发现，很多模型问题最后都会绕回数据、标签、样例和评估方式。

## 一些常用工具和关键词

Python / FastAPI / Django / React / LangChain / RAG / MCP / ChromaDB / MySQL / Redis / PyTorch / BERT / Java / SQLite

不算什么豪华全家桶，只是目前经常会碰到、也还在继续补熟的东西。

## 碎碎念

我喜欢那种能留下痕迹的系统：日志能查，错误能复现，回答有来源，改动有理由。  
也喜欢把一个模糊的问题慢慢拆小，拆到终于能写代码、能测、能改。

有些仓库还在整理，有些代码现在看会觉得青涩，但也挺好，起码知道自己做的东西不好也算是一种进步

<p>
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=STliuEN&show_icons=true&hide_border=true&theme=transparent" alt="GitHub stats" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=STliuEN&layout=compact&hide_border=true&theme=transparent" alt="Top languages" />
</p>

