---
title: "ChatGPT retention rate"
date: 2026-06-22
tags: [Image, LLM, Meta, OpenAI, Privacy]

type: note
status: read
---
ChatGPT retention rate

![image 1.png](./ChatGPT%20retention%20rate-assets/image%201.png)

ChatGPT's product retention curves are a product manager's wet dream.\
\
Their 1 month retention has skyrocketed from <60% 2yrs ago to an unprecedented \~90%! Youtube was best-in-class with \~85%.\
\
6mo retention is trending to \~80%. Rapidly rising smile curve.\
\
Generational product.\
\
Data includes \~28M people and is US only, and doesn't include iOS. It's from a platform called Indagiri



memory， 它是什么？它包括哪些子模块？它如何运作？ 不论对人类还是对llm，都是最重要的问题之一。

今年4月份推出的chatgpt memory功能，是2025年最重要的chatgpt 功能更新之一，是sam altman “最爱的功能”，也是对chatgpt用户体验提升最大的一个功能。

但是，它的**内部工作机制**，却少有人谈论。

chatgpt 目前的 memory 系统，包括**4个记忆子模块**：

- **记忆子模块1 交互元数据（Interaction Metadata）**：包含用户的元数据，例如设备和浏览器、对话深度、消息长度、模型选择占比等，在手机app端和web app端采集的数据维度也不一样；这个记忆子模块，**让chatgpt了解你的基本情况**；

- **记忆子模块2 近期对话内容（Recent Conversation Content）**：按时间回溯的最近若干对话（大约几十条），仅仅包含用户prompt、话题标签和时间戳，不包含模型的回复内容；这个记忆子模块，往往承载了**用户的意图/需求**，成为chatgpt**跨对话时**的隐式上下文，**让chatgpt更“懂你”**；

- **记忆子模块3 模型集上下文（Model Set Context）**：也就是2024年初推出的“saved memories”功能。你在app设置里能看见、能改、能删除的那部分记忆；这个记忆子模块，显示存储了关于你的一些facts，它的**优先级更高**，不同记忆子模块的信息冲突时，它扮演“source of truth”。例如，你对这里告诉chatgpt “我喜欢吃咸豆腐脑，我觉得甜豆腐脑不好吃”，这个信息的优先级就高于其他记忆模块；

- **记忆子模块4 用户知识记忆（User Knowledge Memories）**：这是最重要、最神奇的记忆子模块，也对应chatgpt设置里的“reference chat history”。**它把你和chatgpt多年来数万次的对话，压缩成密度惊人的一系列段落，记住关于你的一切**，而且，这部分记忆是chatgpt对你的认识、理解和总结，你在设置里看不到、改不了，它只会持续更新对你的了解。

**这个模块，是chatgpt对“你”的理解本身。**

**有趣的是：**

chatgpt 实现 memory的方法，并不包括向量数据库、知识图谱、RAG（**此前大家，包括我，都猜测是对历史对话进行embedding，然后RAG**），而是在用户每次和chatgpt对话时，把这四个记忆子模块的内容，一次性全部提供给模型（include everything with every message），让模型自己去识别信息与本次对话相关。记忆内容太多，context window放不下？模型你自己去解决吧！🤣

也就是说，openai在产品和工程上的取舍，表明openai押注两个趋势：

- 1 模型会足够聪明，能在成千上万 token 里自动忽略噪音；  

- 2 模型的context windows 会不断变大，而成本会不断下降。  

甚至，如sam altman所期待的，**以后的模型context window会足够大，数百万token，甚至无限大，能大到包括用户的整个一生（stories of your life）。**

openai的这种取舍，也体现了**ai研究领域的“the bitter lesson”的思想**：少做精细的工程设计，少做复杂外部检索，而是押宝模型本身的能力，把一切都喂给模型，赌更强的模型与更大的上下文。

**为什么推荐这篇文章？**

人脑的memory机制，伴随着我们一生的工作学习生活，每个人都应该理解人脑的记忆机制。

同样，现在和以后，每个人的工作学习生活都离不开chatgpt等llm，那么，理解llm实现memory机制的方法，也很重要。

所以，我制作了双语对照版本，分享给你。祝你阅读愉快～