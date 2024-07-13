# 学习教程
https://github.com/InternLM/Tutorial/blob/camp2/huixiangdou/readme.md#23-%E8%BF%90%E8%A1%8C%E8%8C%B4%E9%A6%99%E8%B1%86%E7%9F%A5%E8%AF%86%E5%8A%A9%E6%89%8B

# RAG基本内容

RAG（Retrieval-Augmented Generation）技术是一种结合了检索和生成的方法，旨在通过利用外部知识库来增强大型语言模型（LLMs）的性能。这项技术最初由Meta（Facebook）的Lewis等人在2020年提出，并随着时间的推移不断发展和完善。

RAG的工作原理是，当接收到用户的问题时，首先将问题编码成向量，并在向量数据库中检索最相关的文档块。这些文档块随后与原始问题一起作为提示输入到LLM中，以生成更准确、更丰富的回答。这个过程不仅提高了回答的准确性，还降低了成本，并实现了外部记忆，从而解决了LLM在处理知识密集型任务时可能遇到的挑战，如生成幻觉和过时知识。

随着RAG技术的发展，出现了多种 RAG 变体，包括 Naive RAG、Advanced RAG 和 Modular RAG等。这些变体在不同的优化方法上有所侧重，如嵌入优化、索引优化、查询优化和上下文管理等。这些优化方法使得RAG能够更好地适应不同的应用场景，如问答系统、文本生成、信息检索和多模态任务等。

为了评估RAG技术的性能，研究者们建立了一套评估框架和基准测试，包括准确率、召回率、F1分数、BLEU分数等经典评估指标，以及专门针对RAG的评估指标，如检索质量和生成质量。这些评估工具，如RAGAS、ARES和TruLens，帮助研究者们更好地理解和提升RAG技术。

总的来说，RAG技术通过结合检索和生成，有效地提升了LLMs在处理知识密集型任务时的性能，并为未来的AI技术发展提供了新的方向。随着技术的不断进步和优化，RAG有望在更多的领域发挥重要作用，为用户提供更加准确和丰富的信息。

![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG01.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG02.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG03.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG04.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG05.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG06.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG07.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG08.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG09.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/RAG10.png)


# 茴香豆

## 茴香豆介绍
茴香豆是由书生浦语团队开发的开源大型模型应用，专为即时通讯（IM）工具中的群聊场景优化。它通过应用检索增强生成（RAG）技术，能够理解和高效准确地回应与特定知识领域相关的复杂查询。茴香豆旨在提供及时准确的技术支持和自动回答服务，帮助维护者减轻负担，同时确保用户问题得到有效解答。

## 茴香豆的核心特性
茴香豆具有多个显著特性：
- 开源免费，高效准确，专为群聊优化，专业知识快速获取。
- 部署成本低，安全，扩展性强。
- 无需额外训练，可完全本地部署，兼容多种IM软件。
- 本地算力需求少，保护数据和用户隐私。
- 支持多种开源LLMs和云端模型API。

## 茴香豆构建
茴香豆的构建包括前端和后端两部分，其中后端采用PDE（可能是某种开发环境或框架）和LLM作为支撑。

## 茴香豆的工作流
茴香豆的工作流程包括以下几个步骤：
1. **预处理**：对群聊中的query（查询）进行预处理。
2. **拒绝管道**（Rejection Pipeline）：使用特征提取（feature）和文本向量化（text2vec）技术，结合数据库（DB）信息，对查询进行筛选。
3. **LLM评分**：对查询进行评分，以确定是否需要进一步处理。
4. **响应管道**（Response Pipeline）：生成响应并回复到群聊中。

## 香豆完整工作流
茴香豆的完整工作流程更为复杂，包括以下几个关键环节：
1. **拒绝查询**：对不适当或无关的查询进行拒绝。
2. **响应管道**：对查询进行处理，生成响应。
3. **多来源检索**：结合本地和远程的大型模型（LLMs），进行关键词（keywords）检索。
4. **混合大模型服务**（Hybrid LLM Service）：利用本地和远程的LLMs，结合知识图谱（knowledge graph）和向量数据库，进行信息检索和评分。
5. **安全检查**：确保回答的合规性和有效性，避免信息泛滥。

![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd01.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd02.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd03.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd04.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd05.png)

## Demo

### Web运行
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd07.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd08.png)
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd09.png)

### InternLM Studio 部署茴香豆

![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/hxd06.png)