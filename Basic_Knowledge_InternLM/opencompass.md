# 如何通过能力评测促进模型发展？
- **面向未来**：评测体系需增加新能力维度。
- **扎根通用能力**：拓展能力维度，聚焦垂直行业。
- **中文基准**：针对中文场景，开发能准确评估其能力的中文评测基准。
- **反哺能力选代**：通过深入分析评测性能，发现模型不足，研究针对性提升策略。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass01.png)

# 大语言模型评测中的挑战
- **全面性**：大模型应用场景多变，需要设计可扩展的能力维度体系。
- **评测成本**：评测数十万道题需要大量算力资源，人工打分成本高昂。
- **数据污染**：海量语料可能带来评测集污染，需要可靠的数据污染检测技术。
- **鲁棒性**：模型性能在多次采样情况下可能不稳定。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass02.png)

# 我们如何评测大模型？
- **基座模型**：使用海量数据无监督训练的公开权重开源模型。
- **对话模型**：指令数据有监督微调(SFT)，人类偏好对齐(RLHF)。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass03.png)

# 客观评测与主观评测
- **客观问答题**：如“中国的首都是哪里？”，模型需给出明确答案。
- **开放式主观问答**：如“写一首七言律诗，表达对龙年春节的期待”，模型需创作性回答。
- **人类评价与模型评价**：对比人类与模型的回答，进行评分。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass04.png)


# 提示词工程
- **明确性**：提示词应具体明确，避免宽泛和歧义。
- **逐步引导**：提示词应逐步引导，提供清晰的思路。
- **具体描述**：提示词应包含具体的问题描述和范围。
- **反馈**：提供具体清晰的修改建议。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass05.png)

# 长文本评测
- **模型输入**：长文本建模能力，如文档1、文档n等，总长度可达200K。
- **能力分析与性能示意**：例如，文档中包含“小明在上海人工智能实验室实习”，模型应准确抽取信息并回答问题。

![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass06.png)


# 汇集社区力量：工具一基准－榜单三位一体
- **CompassHub**：评测集社区，支持能力分析。
- **CompassRank**：发布权威性能榜单。
- **CompassKit**：全栈评测工具，提供高时效性。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass07.png)

# CompassKit：大模型评测全栈工具链
- **数据污染检查**：提供多种数据污染检测方法。
- **模型推理接入**：支持近20个商业模型API。
- **长文本能力评测**：支持1M长度大海捞针测试。
- **中英文双语主观评测**：支持基于大模型评价的主观评测。

![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass08.png)

# OpenCompass评测流水线
- **任务切分及并行化**：OpenCompass 将评测请求切分为多个独立执行的任务，以最大化利用计算资源。
- **多种输出方案**：支持包括 CSV、TXT、文飞书等多种输出格式。
- **并行执行**：支持本地/Slurm/DLC 等多种并行执行环境。
- **自定义任务**：用户可以自定义任务1、任务2等。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass09.png)

# 基础：自研高质量大模型评测基准
- **CriticBench**：大模型细粒度工具能力评测基准。
- **T-Eval**：多维度的LLM反思能力评估基准。
- **MathBench**：多层次数学能力评测基准。
- **CreationBench**：多场景中文创作能力评测基准。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass10.png)


# 作业

![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass11.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/opencompass12.png)