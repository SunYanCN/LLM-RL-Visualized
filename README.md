<p align="center">
  <img src="src/assets/banner/幻灯片2.SVG" alt="图解大模型算法：LLM / RL / VLM 核心技术图谱" />
</p>

<p align="center">
  <a href="./src/README_EN.md">
    <img
      alt="English Version"
      src="https://img.shields.io/badge/English-Version-blue?style=for-the-badge"
      width="250"
      height="50"
    />
  </a> 
  &nbsp; &nbsp;&nbsp;

  <a href="./README.md">
    <img
      alt="Chinese 中文版本"
      src="https://img.shields.io/badge/Chinese-中文版本-red?style=for-the-badge"
      width="250"
      height="50"
    />
  </a>    
</p>

---

## 项目说明
🎉 **原创 100+ 架构图，重磅开源！大模型算法一览无余！** 涵盖 LLM、VLM 等大模型技术，训练算法（RL、RLHF、GRPO、DPO、SFT 与 CoT 蒸馏等）、效果优化与 RAG 等。  

🎉 架构图的<strong>文字详解、更多架构图</strong> 详见：<a href="https://book.douban.com/subject/37331056/">《大模型算法：强化学习、微调与对齐》</a>

🎉 本项目 **长期勘误、更新、追加**，欢迎点击右上角 ↗ 的 **Star ⭐** 关注！  

🎉 点击图片可查看高清大图，或浏览仓库目录中的 `.svg` 格式矢量图（支持无限缩放）


## 内容索引
- [大模型算法总体架构（以LLM、VLM为主）](#header-1)
- [强化学习算法图谱 (rl-algo-map).pdf————全网最大！](#header-126)
- [【LLM基础】LLM结构总图————全网最大！](#header-2)
- [【LLM基础】LLM（Large Language Model）结构](#header-3)
- [【LLM基础】LLM生成与解码（Decoding）过程](#header-4)
- [【LLM基础】LLM输入层](#header-5)
- [【LLM基础】LLM输出层](#header-6)
- [【LLM基础】多模态模型结构（VLM、MLLM ...）](#header-7)
- [【LLM基础】LLM训练流程](#header-8)
- [【SFT】微调（Fine-Tuning）技术分类](#header-9)
- [【SFT】LoRA（1 of 2）](#header-10)
- [【SFT】LoRA（2 of 2）](#header-11)
- [【SFT】Prefix-Tuning](#header-12)
- [【SFT】TokenID与词元的映射关系](#header-13)
- [【SFT】SFT的Loss（交叉熵）](#header-14)
- [【SFT】指令数据的来源](#header-15)
- [【SFT】多个数据的拼接（Packing）](#header-16)
- [【DPO】RLHF与DPO的训练架构对比](#header-17)
- [【DPO】Prompt的收集](#header-18)
- [【DPO】DPO（Direct Preference Optimization）](#header-19)
- [【DPO】DPO训练全景图](#header-20)
- [【DPO】β参数对DPO的影响](#header-21)
- [【DPO】隐式奖励差异对参数更新幅度的影响](#header-22)
- [【免训练的优化技术】CoT（Chain of Thought）与传统问答的对比](#header-23)
- [【免训练的优化技术】CoT、Self-consistency CoT、ToT、GoT <sup>[<a href="./src/references.md">87</a>]</sup>](#header-24)
- [【免训练的优化技术】穷举搜索（Exhaustive Search）](#header-25)
- [【免训练的优化技术】贪婪搜索（Greedy Search）](#header-26)
- [【免训练的优化技术】波束搜索（Beam Search）](#header-27)
- [【免训练的优化技术】多项式采样（Multinomial Sampling）](#header-28)
- [【免训练的优化技术】Top-K采样（Top-K Sampling）](#header-29)
- [【免训练的优化技术】Top-P采样（Top-P Sampling）](#header-30)
- [【免训练的优化技术】RAG（检索增强生成,Retrieval-Augmented Generation）](#header-31)
- [【免训练的优化技术】功能调用（Function Calling）](#header-32)
- [【强化学习基础】强化学习(Reinforcement Learning, RL)的发展历程](#header-33)
- [【强化学习基础】三大机器学习范式](#header-34)
- [【强化学习基础】强化学习的基础架构](#header-35)
- [【强化学习基础】强化学习的运行轨迹](#header-36)
- [【强化学习基础】马尔可夫链vs马尔可夫决策过程（MDP）](#header-37)
- [【强化学习基础】探索与利用问题（Exploration and Exploitation）](#header-38)
- [【强化学习基础】Ɛ-贪婪策略下使用动态的Ɛ值](#header-39)
- [【强化学习基础】强化学习训练范式的对比](#header-40)
- [【强化学习基础】强化学习算法分类](#header-41)
- [【强化学习基础】回报（累计奖励，Return）](#header-42)
- [【强化学习基础】反向迭代并计算回报G](#header-43)
- [【强化学习基础】奖励（Reward）、回报（Return）、价值（Value）的关系](#header-44)
- [【强化学习基础】价值函数Qπ与Vπ的关系](#header-45)
- [【强化学习基础】蒙特卡洛（Monte Carlo，MC）法预估状态St的价值](#header-46)
- [【强化学习基础】TD目标与TD误差的关系（TD target and TD error）](#header-47)
- [【强化学习基础】TD(0)、多步TD与蒙特卡洛（MC）的关系](#header-48)
- [【强化学习基础】蒙特卡洛方法与TD方法的特性](#header-49)
- [【强化学习基础】蒙特卡洛、TD、DP、穷举搜索的关系 <sup>[<a href="./src/references.md">32</a>]</sup>](#header-50)
- [【强化学习基础】两种输入输出结构的DQN（Deep Q-Network）模型](#header-51)
- [【强化学习基础】DQN的实际应用示例](#header-52)
- [【强化学习基础】DQN的“高估”问题](#header-53)
- [【强化学习基础】基于价值vs基于策略（Value-Based vs Policy-Based）](#header-54)
- [【强化学习基础】策略梯度（Policy Gradient）](#header-55)
- [【强化学习基础】多智能体强化学习（MARL，Multi-agent reinforcement learning）](#header-56)
- [【强化学习基础】多智能体DDPG <sup>[<a href="./src/references.md">41</a>]</sup>](#header-57)
- [【强化学习基础】模仿学习（IL，Imitation Learning）](#header-58)
- [【强化学习基础】行为克隆（BC，Behavior Cloning）](#header-59)
- [【强化学习基础】逆向强化学习（IRL，Inverse RL）、强化学习（RL）](#header-60)
- [【强化学习基础】有模型（Model-Based）、无模型（Model-Free）](#header-61)
- [【强化学习基础】封建等级强化学习（Feudal RL）](#header-62)
- [【强化学习基础】分布价值强化学习（Distributional RL）](#header-63)
- [【策略优化架构算法及其衍生】Actor-Critic架构](#header-64)
- [【策略优化架构算法及其衍生】引入基线与优势（Advantage）函数A的作用](#header-65)
- [【策略优化架构算法及其衍生】GAE（广义优势估计,Generalized Advantage Estimation）算法](#header-66)
- [【策略优化架构算法及其衍生】PPO（Proximal Policy Optimization）算法的演进](#header-67)
- [【策略优化架构算法及其衍生】TRPO（Trust Region Policy Optimization）及其置信域](#header-68)
- [【策略优化架构算法及其衍生】重要性采样（Importance sampling）](#header-69)
- [【策略优化架构算法及其衍生】PPO-Clip](#header-70)
- [【策略优化架构算法及其衍生】PPO训练中策略模型的更新过程](#header-71)
- [【策略优化架构算法及其衍生】PPO与GRPO（Group Relative Policy Optimization） <sup>[<a href="./src/references.md">72</a>]</sup>](#header-72)
- [【策略优化架构算法及其衍生】确定性策略vs随机性策略（Deterministic policy vs. Stochastic policy）](#header-73)
- [【策略优化架构算法及其衍生】确定性策略梯度（DPG）](#header-74)
- [【策略优化架构算法及其衍生】DDPG（Deep Deterministic Policy Gradient）](#header-75)
- [【RLHF与RLAIF】语言模型的强化学习建模](#header-76)
- [【RLHF与RLAIF】RLHF的两阶段式训练流程](#header-77)
- [【RLHF与RLAIF】奖励模型（RM）的结构](#header-78)
- [【RLHF与RLAIF】奖励模型的输入输出](#header-79)
- [【RLHF与RLAIF】奖励模型预测偏差与Loss的关系](#header-80)
- [【RLHF与RLAIF】奖励模型的训练](#header-81)
- [【RLHF与RLAIF】PPO训练中四种模型的合作关系](#header-82)
- [【RLHF与RLAIF】PPO训练中四种模型的结构与初始化](#header-83)
- [【RLHF与RLAIF】一个双头结构的价值模型](#header-84)
- [【RLHF与RLAIF】RLHF：四种模型可以共享同一个底座](#header-85)
- [【RLHF与RLAIF】PPO训练中各模型的输入与输出](#header-86)
- [【RLHF与RLAIF】PPO训练中KL距离的计算过程](#header-87)
- [【RLHF与RLAIF】基于PPO进行RLHF训练的原理图](#header-88)
- [【RLHF与RLAIF】拒绝采样（Rejection Sampling）微调](#header-89)
- [【RLHF与RLAIF】RLAIF与RLHF的区别](#header-90)
- [【RLHF与RLAIF】Claude模型应用的宪法AI（CAI）原理](#header-91)
- [【RLHF与RLAIF】OpenAI RBR（基于规则的奖励）](#header-92)
- [【逻辑推理能力优化】基于CoT的知识蒸馏（Knowledge Distillation）](#header-93)
- [【逻辑推理能力优化】基于DeepSeek进行蒸馏](#header-94)
- [【逻辑推理能力优化】ORM和PRM（结果奖励模型和过程奖励模型）](#header-95)
- [【逻辑推理能力优化】MCTS每次迭代的四个关键步骤](#header-96)
- [【逻辑推理能力优化】MCTS的运行过程](#header-97)
- [【逻辑推理能力优化】语言场景下的搜索树示例](#header-98)
- [【逻辑推理能力优化】BoN（Best-of-N）采样](#header-99)
- [【逻辑推理能力优化】多数投票（Majority Vote）方法](#header-100)
- [【逻辑推理能力优化】AlphaGoZero在训练时的性能增长趋势 <sup>[<a href="./src/references.md">179</a>]</sup>](#header-101)
- [【LLM基础拓展】大模型性能优化技术图谱](#header-102)
- [【LLM基础拓展】ALiBi位置编码](#header-103)
- [【LLM基础拓展】传统的知识蒸馏](#header-104)
- [【LLM基础拓展】数值表示、量化（Quantization）](#header-105)
- [【LLM基础拓展】常规训练时前向和反向过程](#header-106)
- [【LLM基础拓展】梯度累积（Gradient Accumulation）训练](#header-107)
- [【LLM基础拓展】Gradient Checkpoint（梯度重计算）](#header-108)
- [【LLM基础拓展】Full recomputation(完全重计算)](#header-109)
- [【LLM基础拓展】LLM Benchmark](#header-110)
- [【LLM基础拓展】MHA、GQA、MQA、MLA](#header-111)
- [【LLM基础拓展】RNN（Recurrent Neural Network）](#header-112)
- [【LLM基础拓展】Pre-norm和Post-norm](#header-113)
- [【LLM基础拓展】BatchNorm和LayerNorm](#header-114)
- [【LLM基础拓展】RMSNorm](#header-115)
- [【LLM基础拓展】Prune（剪枝）](#header-116)
- [【LLM基础拓展】温度系数的作用](#header-117)
- [【LLM基础拓展】SwiGLU](#header-118)
- [【LLM基础拓展】AUC、PR、F1、Precision、Recall](#header-119)
- [【LLM基础拓展】RoPE位置编码](#header-120)
- [【LLM基础拓展】RoPE对各序列位置、各维度的作用](#header-121)
- [所有架构图的 文字详解✍️、更多架构图🖼️](#header-122)
- [书籍参考文献](#header-123)
- [用于参考文献（引用格式）](#header-124)
- [BibTeX（引用格式）](#header-125)

<br>

---

### <a name="header-1"></a>大模型算法总体架构（以LLM、VLM为主）
<img src="src/assets/大模型算法-内容架构-zh.png" alt="大模型算法-内容架构">

### <a name="header-126"></a> 强化学习算法图谱 (rl-algo-map).pdf————全网最大！
- 我历时数天、呕心沥血之作，点击本仓库右上角 ↗ 的 **Star ⭐** ，就是对我最大的鼓励啦！
- 下图仅为预览图，高清图见： <a href="https://github.com/changyeyu/LLM-RL-Visualized/blob/master/%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%AE%97%E6%B3%95%E5%9B%BE%E8%B0%B1%20(rl-algo-map).pdf"> 强化学习算法图谱 (rl-algo-map).pdf </a>
[![强化学习算法图谱 (rl-algo-map).pdf](images_chinese/rl-algo-map-preview.png)](https://github.com/changyeyu/LLM-RL-Visualized/blob/master/%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%AE%97%E6%B3%95%E5%9B%BE%E8%B0%B1%20(rl-algo-map).pdf)

### <a name="header-2"></a>【LLM基础】LLM结构总图————全网最大！
- 我几十个小时、呕心沥血之作，点击本仓库右上角 ↗ 的 **Star ⭐** ，就是对我最大的鼓励啦！
- LLM主要有Decoder-Only（仅解码器）或MoE（Mixture of Experts, 专家混合模型）两种形式，两者在整体架构上较为相似，主要区别为MoE在FFN（前馈网络）部分引入了多个专家网络。
[![【LLM基础】LLM结构全视图](images_chinese/source_svg/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E7%BB%93%E6%9E%84%E5%85%A8%E8%A7%86%E5%9B%BE.svg)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/source_svg/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E7%BB%93%E6%9E%84%E5%85%A8%E8%A7%86%E5%9B%BE.svg)

### <a name="header-3"></a>【LLM基础】LLM（Large Language Model）结构
- LLM主要有Decoder-Only（仅解码器）或MoE（Mixture of Experts, 专家混合模型）两种形式，两者在整体架构上较为**相似**，主要区别为MoE在FFN（前馈网络）部分引入了多个专家网络。
- 一个典型的LLM结构，可分为**三部分**——输入层、多层Decoder堆叠结构和输出层（包括语言模型头与解码模块）

[![【LLM基础】LLM结构](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E7%BB%93%E6%9E%84.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E7%BB%93%E6%9E%84.png)

### <a name="header-4"></a>【LLM基础】LLM生成与解码（Decoding）过程
- LLM的输出层负责根据概率分布，应用**解码算法**确定最终预测的下一个/N个词元。
- 根据概率分布，应用解码策略（例如随机采样或选择最大概率）确定最终预测的**下一个**词元。例如，在贪婪搜索解码策略下，选择概率最高的词元“我”作为预测结果。
- 每一个token（词元）的生成都需要**重新走一遍**所有层Transformer结构。
- 这里只展示了每次预测一个词元的方案，也有一次性预测多个词元的方案，详见《大模型算法：强化学习、微调与对齐》第四章。
[![【LLM基础】LLM生成与解码过程](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E7%94%9F%E6%88%90%E4%B8%8E%E8%A7%A3%E7%A0%81%E8%BF%87%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E7%94%9F%E6%88%90%E4%B8%8E%E8%A7%A3%E7%A0%81%E8%BF%87%E7%A8%8B.png)

### <a name="header-5"></a>【LLM基础】LLM输入层
- LLM的输入层将输入**文本**转换为多维**数值矩阵**（Tensor，张量），以便送往模型主体结构进行计算。
[![【LLM基础】LLM输入层](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E8%BE%93%E5%85%A5%E5%B1%82.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E8%BE%93%E5%85%A5%E5%B1%82.png)

### <a name="header-6"></a>【LLM基础】LLM输出层
LLM的输出层负责根据隐藏状态（多维数值矩阵）预测下一个词元（文本）。处理流程如图所示：
- （1）**输入隐藏状态**：Decoder最后一层的隐藏状态（Hidden States）作为LLM输出层的输入。如图中所示维度为3×896的数值矩阵，包含了前缀序列的所有语义信息。
- （2）**语言模型头**（LM Head）：通常是一个全连接层，用于将隐藏状态转换为Logits（推理时只计算最后一个位置的Logits）。如图所示，Logits的形状为3×151936，对应于词表中每个词元的得分。
- （3）**提取最后位置的Logits**：预测下一个词元仅依赖于前缀序列最后一个位置的Logits，因此需要从所有位置的Logits中提取最后一个位置的Logits。如图所示，提取得到一个151936维的向量 [2.0, 3.1, −1.7, ... , −1.7]，用于后续预测。
- （4）**转换为概率分布**（Softmax）：通过Softmax函数将Logits转换为概率分布，得到词表中每个词元的概率。例如，生成的151936维概率向量为[0.01, 0.03, 0.001, ... , 0.001]，该向量内所有概率之和为1。概率值越大，表示该词元作为下一个词元的可能性越高。例如，“我”的概率为0.34。
- （5）**解码（Decoding）**：根据概率分布，应用解码策略（例如随机采样或选择最大概率）确定最终预测的下一个词元。例如，在贪婪搜索解码策略下，选择概率最高的词元“我”作为预测结果。
[![【LLM基础】LLM输出层](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E8%BE%93%E5%87%BA%E5%B1%82.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E8%BE%93%E5%87%BA%E5%B1%82.png)

### <a name="header-7"></a>【LLM基础】多模态模型结构（VLM、MLLM ...）
多模态模型根据侧重不同，通常有以下称呼方法：
- VLM（Vision-Language Model，视觉语言模型）
- MLLM（Multimodal Large Language Model，多模态大语言模型）
- VLA（Vision-Language-Action Model，视觉语言动作模型）
[![【LLM基础】多模态模型结构](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91%E5%A4%9A%E6%A8%A1%E6%80%81%E6%A8%A1%E5%9E%8B%E7%BB%93%E6%9E%84.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91%E5%A4%9A%E6%A8%A1%E6%80%81%E6%A8%A1%E5%9E%8B%E7%BB%93%E6%9E%84.png)

### <a name="header-8"></a>【LLM基础】LLM训练流程
- 大模型的训练主要分为**两个阶段**——预训练（Pre-Training）和后训练（Post-Training）。在每个阶段，所使用的训练数据、训练范式（算法）、训练目标和超参数均有所不同。
- **预训练**阶段包括初期训练（基于海量数据的短上下文训练）、中期训练（长文本/长上下文训练）以及退火（Annealing）训练等。此阶段以自监督学习为主，使用的数据量最大，同时也是最消耗算力的环节。
- **后训练**阶段则包含多种可选的训练范式（算法），包括但不限于SFT（监督微调）、蒸馏、RSFT（拒绝采样微调）、RLHF（基于人类反馈的强化学习）、DPO（直接偏好优化），以及其他强化学习方法，例如GRPO（群体相对策略优化）、PPO（近端策略优化）等。其中，某些环节也可进行多轮迭代训练，例如多轮拒绝采样微调（Rejection Sampling Fine-Tuning, RSFT）。
[![【LLM基础】LLM训练流程](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E8%AE%AD%E7%BB%83%E6%B5%81%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E3%80%91LLM%E8%AE%AD%E7%BB%83%E6%B5%81%E7%A8%8B.png)

### <a name="header-9"></a>【SFT】微调（Fine-Tuning）技术分类
- 可用于SFT的微调技术种类多样，如下图的分类图所示：前两种方法仅需基于预训练模型主体进行微调，开发成本较低；而并联低秩微调和Adapter Tuning则需要引入额外的新模块，实施过程相对复杂一些。这些方法均是针对模型参数进行微调，而基于Prompt的微调则另辟蹊径，从模型的输入着手进行微调。
[![【SFT】微调技术分类](images_chinese/png_small/%E3%80%90SFT%E3%80%91%E5%BE%AE%E8%B0%83%E6%8A%80%E6%9C%AF%E5%88%86%E7%B1%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91%E5%BE%AE%E8%B0%83%E6%8A%80%E6%9C%AF%E5%88%86%E7%B1%BB.png)

### <a name="header-10"></a>【SFT】LoRA（1 of 2）
- LoRA（Low-Rank Adaptation, 低秩适配微调）由微软的研究团队于2021年发表。由于其高效的微调方式和良好的效果，在各类模型中得到广泛的应用。LoRA的**核心思想**在于——微调前后模型的参数差异∆W具有低秩性。
- 一个矩阵具有**低秩性**，意味着它包含较多的冗余信息，将其分解为多个低维矩阵后，不会损失过多有用信息。例如，如图所示，一个1024×1024的矩阵可以被近似分解为一个1024×2矩阵与一个2×1024矩阵的乘积，从而将参数量约减少至原来的0.4%。

[![【SFT】LoRA（1 of 2）](images_chinese/png_small/%E3%80%90SFT%E3%80%91LoRA%EF%BC%881%20of%202%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91LoRA%EF%BC%881%20of%202%EF%BC%89.png)

### <a name="header-11"></a>【SFT】LoRA（2 of 2）
- A和B的**初始化**方式：
- （1）矩阵A使用随机数初始化，如kaiming初始化；
- （2）矩阵B使用全0初始化，或使用极小的随机数初始化。
- **目的**在于——确保在训练初期，插入的LoRA模块不会对模型整体输出造成过大的扰动。
[![【SFT】LoRA（2 of 2）](images_chinese/png_small/%E3%80%90SFT%E3%80%91LoRA%EF%BC%882%20of%202%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91LoRA%EF%BC%882%20of%202%EF%BC%89.png)

### <a name="header-12"></a>【SFT】Prefix-Tuning
- Prefix-Tuning由斯坦福大学的研究团队提出，可以用于对语言模型进行轻量级微调。如图所示，该方法在输入的起始位置插入一段连续的、可训练的向量（Embedding），称为前缀（Prefix）。在处理后续的Token时，Transformer将这些向量视为 **虚拟Token**，并参与Attention计算。

[![【SFT】Prefix-Tuning](images_chinese/png_small/%E3%80%90SFT%E3%80%91Prefix-Tuning.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91Prefix-Tuning.png)

### <a name="header-13"></a>【SFT】TokenID与词元的映射关系
- 以SFT数据（经过ChatML格式预处理）为例，该数据经过Tokenizer处理后，被转换为33个Token，对应33个序列位置，如图所示。每个Token ID与相应的词元**一一对应**。
[![【SFT】TokenID与词元的映射关系](images_chinese/png_small/%E3%80%90SFT%E3%80%91TokenID%E4%B8%8E%E8%AF%8D%E5%85%83%E7%9A%84%E6%98%A0%E5%B0%84%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91TokenID%E4%B8%8E%E8%AF%8D%E5%85%83%E7%9A%84%E6%98%A0%E5%B0%84%E5%85%B3%E7%B3%BB.png)

### <a name="header-14"></a>【SFT】SFT的Loss（交叉熵）
- 与预训练阶段类似，SFT的Loss也是基于交叉熵（CE，Cross Entropy）
[![【SFT】SFT的Loss（交叉熵）](images_chinese/png_small/%E3%80%90SFT%E3%80%91SFT%E7%9A%84Loss%EF%BC%88%E4%BA%A4%E5%8F%89%E7%86%B5%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91SFT%E7%9A%84Loss%EF%BC%88%E4%BA%A4%E5%8F%89%E7%86%B5%EF%BC%89.png)

### <a name="header-15"></a>【SFT】指令数据的来源
- **指令数据**（Instructions）是指为模型提供的一组引导性输入及期望输出的描述，通常包括问题（或任务提示）及其对应的答案，常用于对模型进行微调训练。
[![【SFT】指令数据的来源](images_chinese/png_small/%E3%80%90SFT%E3%80%91%E6%8C%87%E4%BB%A4%E6%95%B0%E6%8D%AE%E7%9A%84%E6%9D%A5%E6%BA%90.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91%E6%8C%87%E4%BB%A4%E6%95%B0%E6%8D%AE%E7%9A%84%E6%9D%A5%E6%BA%90.png)

### <a name="header-16"></a>【SFT】多个数据的拼接（Packing）
- （待续，持续补充注释中 ...）
[![【SFT】多个数据的拼接（Packing）](images_chinese/png_small/%E3%80%90SFT%E3%80%91%E5%A4%9A%E4%B8%AA%E6%95%B0%E6%8D%AE%E7%9A%84%E6%8B%BC%E6%8E%A5%EF%BC%88Packing%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90SFT%E3%80%91%E5%A4%9A%E4%B8%AA%E6%95%B0%E6%8D%AE%E7%9A%84%E6%8B%BC%E6%8E%A5%EF%BC%88Packing%EF%BC%89.png)

### <a name="header-17"></a>【DPO】RLHF与DPO的训练架构对比
[![【DPO】RLHF与DPO的训练架构对比](images_chinese/png_small/%E3%80%90DPO%E3%80%91RLHF%E4%B8%8EDPO%E7%9A%84%E8%AE%AD%E7%BB%83%E6%9E%B6%E6%9E%84%E5%AF%B9%E6%AF%94.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90DPO%E3%80%91RLHF%E4%B8%8EDPO%E7%9A%84%E8%AE%AD%E7%BB%83%E6%9E%B6%E6%9E%84%E5%AF%B9%E6%AF%94.png)

### <a name="header-18"></a>【DPO】Prompt的收集
[![【DPO】Prompt的收集](images_chinese/png_small/%E3%80%90DPO%E3%80%91Prompt%E7%9A%84%E6%94%B6%E9%9B%86.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90DPO%E3%80%91Prompt%E7%9A%84%E6%94%B6%E9%9B%86.png)

### <a name="header-19"></a>【DPO】DPO（Direct Preference Optimization）
[![【DPO】DPO（Direct Preference Optimization）](images_chinese/png_small/%E3%80%90DPO%E3%80%91DPO%EF%BC%88Direct%20Preference%20Optimization%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90DPO%E3%80%91DPO%EF%BC%88Direct%20Preference%20Optimization%EF%BC%89.png)

### <a name="header-20"></a>【DPO】DPO训练全景图
[![【DPO】DPO训练全景图](images_chinese/png_small/%E3%80%90DPO%E3%80%91DPO%E8%AE%AD%E7%BB%83%E5%85%A8%E6%99%AF%E5%9B%BE.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90DPO%E3%80%91DPO%E8%AE%AD%E7%BB%83%E5%85%A8%E6%99%AF%E5%9B%BE.png)

### <a name="header-21"></a>【DPO】β参数对DPO的影响
[![【DPO】β参数对DPO的影响](images_chinese/png_small/%E3%80%90DPO%E3%80%91%CE%B2%E5%8F%82%E6%95%B0%E5%AF%B9DPO%E7%9A%84%E5%BD%B1%E5%93%8D.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90DPO%E3%80%91%CE%B2%E5%8F%82%E6%95%B0%E5%AF%B9DPO%E7%9A%84%E5%BD%B1%E5%93%8D.png)

### <a name="header-22"></a>【DPO】隐式奖励差异对参数更新幅度的影响
[![【DPO】隐式奖励差异对参数更新幅度的影响](images_chinese/png_small/%E3%80%90DPO%E3%80%91%E9%9A%90%E5%BC%8F%E5%A5%96%E5%8A%B1%E5%B7%AE%E5%BC%82%E5%AF%B9%E5%8F%82%E6%95%B0%E6%9B%B4%E6%96%B0%E5%B9%85%E5%BA%A6%E7%9A%84%E5%BD%B1%E5%93%8D.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90DPO%E3%80%91%E9%9A%90%E5%BC%8F%E5%A5%96%E5%8A%B1%E5%B7%AE%E5%BC%82%E5%AF%B9%E5%8F%82%E6%95%B0%E6%9B%B4%E6%96%B0%E5%B9%85%E5%BA%A6%E7%9A%84%E5%BD%B1%E5%93%8D.png)

### <a name="header-23"></a>【免训练的优化技术】CoT（Chain of Thought）与传统问答的对比
[![【免训练的优化技术】CoT与传统问答的对比](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91CoT%E4%B8%8E%E4%BC%A0%E7%BB%9F%E9%97%AE%E7%AD%94%E7%9A%84%E5%AF%B9%E6%AF%94.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91CoT%E4%B8%8E%E4%BC%A0%E7%BB%9F%E9%97%AE%E7%AD%94%E7%9A%84%E5%AF%B9%E6%AF%94.png)

### <a name="header-24"></a>【免训练的优化技术】CoT、Self-consistency CoT、ToT、GoT <sup>[<a href="./src/references.md">87</a>]</sup>
[![【免训练的优化技术】CoT、Self-consistencyCoT、ToT、GoT](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91CoT%E3%80%81Self-consistencyCoT%E3%80%81ToT%E3%80%81GoT.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91CoT%E3%80%81Self-consistencyCoT%E3%80%81ToT%E3%80%81GoT.png)

### <a name="header-25"></a>【免训练的优化技术】穷举搜索（Exhaustive Search）
[![【免训练的优化技术】穷举搜索（Exhaustive Search）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E7%A9%B7%E4%B8%BE%E6%90%9C%E7%B4%A2%EF%BC%88Exhaustive%20Search%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E7%A9%B7%E4%B8%BE%E6%90%9C%E7%B4%A2%EF%BC%88Exhaustive%20Search%EF%BC%89.png)

### <a name="header-26"></a>【免训练的优化技术】贪婪搜索（Greedy Search）
[![【免训练的优化技术】贪婪搜索（Greedy Search）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E8%B4%AA%E5%A9%AA%E6%90%9C%E7%B4%A2%EF%BC%88Greedy%20Search%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E8%B4%AA%E5%A9%AA%E6%90%9C%E7%B4%A2%EF%BC%88Greedy%20Search%EF%BC%89.png)

### <a name="header-27"></a>【免训练的优化技术】波束搜索（Beam Search）
[![【免训练的优化技术】波束搜索（Beam Search）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E6%B3%A2%E6%9D%9F%E6%90%9C%E7%B4%A2%EF%BC%88Beam%20Search%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E6%B3%A2%E6%9D%9F%E6%90%9C%E7%B4%A2%EF%BC%88Beam%20Search%EF%BC%89.png)

### <a name="header-28"></a>【免训练的优化技术】多项式采样（Multinomial Sampling）
[![【免训练的优化技术】多项式采样（Multinomial Sampling）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E5%A4%9A%E9%A1%B9%E5%BC%8F%E9%87%87%E6%A0%B7%EF%BC%88Multinomial%20Sampling%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E5%A4%9A%E9%A1%B9%E5%BC%8F%E9%87%87%E6%A0%B7%EF%BC%88Multinomial%20Sampling%EF%BC%89.png)

### <a name="header-29"></a>【免训练的优化技术】Top-K采样（Top-K Sampling）
[![【免训练的优化技术】Top-K采样（Top-K Sampling）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91Top-K%E9%87%87%E6%A0%B7%EF%BC%88Top-K%20Sampling%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91Top-K%E9%87%87%E6%A0%B7%EF%BC%88Top-K%20Sampling%EF%BC%89.png)

### <a name="header-30"></a>【免训练的优化技术】Top-P采样（Top-P Sampling）
[![【免训练的优化技术】Top-P采样（Top-P Sampling）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91Top-P%E9%87%87%E6%A0%B7%EF%BC%88Top-P%20Sampling%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91Top-P%E9%87%87%E6%A0%B7%EF%BC%88Top-P%20Sampling%EF%BC%89.png)

### <a name="header-31"></a>【免训练的优化技术】RAG（检索增强生成,Retrieval-Augmented Generation）
[![【免训练的优化技术】RAG（检索增强生成）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91RAG%EF%BC%88%E6%A3%80%E7%B4%A2%E5%A2%9E%E5%BC%BA%E7%94%9F%E6%88%90%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91RAG%EF%BC%88%E6%A3%80%E7%B4%A2%E5%A2%9E%E5%BC%BA%E7%94%9F%E6%88%90%EF%BC%89.png)

### <a name="header-32"></a>【免训练的优化技术】功能调用（Function Calling）
[![【免训练的优化技术】功能调用（Function Calling）](images_chinese/png_small/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E5%8A%9F%E8%83%BD%E8%B0%83%E7%94%A8%EF%BC%88Function%20Calling%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%85%8D%E8%AE%AD%E7%BB%83%E7%9A%84%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E3%80%91%E5%8A%9F%E8%83%BD%E8%B0%83%E7%94%A8%EF%BC%88Function%20Calling%EF%BC%89.png)

### <a name="header-33"></a>【强化学习基础】强化学习(Reinforcement Learning, RL)的发展历程
[![【强化学习基础】强化学习的发展历程](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%9A%84%E5%8F%91%E5%B1%95%E5%8E%86%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%9A%84%E5%8F%91%E5%B1%95%E5%8E%86%E7%A8%8B.png)

### <a name="header-34"></a>【强化学习基础】三大机器学习范式
[![【强化学习基础】三大机器学习范式](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E4%B8%89%E5%A4%A7%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0%E8%8C%83%E5%BC%8F.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E4%B8%89%E5%A4%A7%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0%E8%8C%83%E5%BC%8F.png)

### <a name="header-35"></a>【强化学习基础】强化学习的基础架构
[![【强化学习基础】强化学习的基础架构](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%9A%84%E5%9F%BA%E7%A1%80%E6%9E%B6%E6%9E%84.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%9A%84%E5%9F%BA%E7%A1%80%E6%9E%B6%E6%9E%84.png)

### <a name="header-36"></a>【强化学习基础】强化学习的运行轨迹
[![【强化学习基础】强化学习的运行轨迹](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%9A%84%E8%BF%90%E8%A1%8C%E8%BD%A8%E8%BF%B9.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%9A%84%E8%BF%90%E8%A1%8C%E8%BD%A8%E8%BF%B9.png)

### <a name="header-37"></a>【强化学习基础】马尔可夫链vs马尔可夫决策过程（MDP）
[![【强化学习基础】马尔可夫链vs马尔可夫决策过程](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E9%A9%AC%E5%B0%94%E5%8F%AF%E5%A4%AB%E9%93%BEvs%E9%A9%AC%E5%B0%94%E5%8F%AF%E5%A4%AB%E5%86%B3%E7%AD%96%E8%BF%87%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E9%A9%AC%E5%B0%94%E5%8F%AF%E5%A4%AB%E9%93%BEvs%E9%A9%AC%E5%B0%94%E5%8F%AF%E5%A4%AB%E5%86%B3%E7%AD%96%E8%BF%87%E7%A8%8B.png)

### <a name="header-38"></a>【强化学习基础】探索与利用问题（Exploration and Exploitation）
[![【强化学习基础】探索与利用问题](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E6%8E%A2%E7%B4%A2%E4%B8%8E%E5%88%A9%E7%94%A8%E9%97%AE%E9%A2%98.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E6%8E%A2%E7%B4%A2%E4%B8%8E%E5%88%A9%E7%94%A8%E9%97%AE%E9%A2%98.png)

### <a name="header-39"></a>【强化学习基础】Ɛ-贪婪策略下使用动态的Ɛ值
[![【强化学习基础】Ɛ-贪婪策略下使用动态的Ɛ值](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%C6%90-%E8%B4%AA%E5%A9%AA%E7%AD%96%E7%95%A5%E4%B8%8B%E4%BD%BF%E7%94%A8%E5%8A%A8%E6%80%81%E7%9A%84%C6%90%E5%80%BC.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%C6%90-%E8%B4%AA%E5%A9%AA%E7%AD%96%E7%95%A5%E4%B8%8B%E4%BD%BF%E7%94%A8%E5%8A%A8%E6%80%81%E7%9A%84%C6%90%E5%80%BC.png)

### <a name="header-40"></a>【强化学习基础】强化学习训练范式的对比
- On-policy，Off-policy，Offline RL
[![【强化学习基础】强化学习训练范式的对比](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E8%AE%AD%E7%BB%83%E8%8C%83%E5%BC%8F%E7%9A%84%E5%AF%B9%E6%AF%94.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E8%AE%AD%E7%BB%83%E8%8C%83%E5%BC%8F%E7%9A%84%E5%AF%B9%E6%AF%94.png)

### <a name="header-41"></a>【强化学习基础】强化学习算法分类
[![【强化学习基础】强化学习算法分类](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%AE%97%E6%B3%95%E5%88%86%E7%B1%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E7%AE%97%E6%B3%95%E5%88%86%E7%B1%BB.png)

### <a name="header-42"></a>【强化学习基础】回报（累计奖励，Return）
[![【强化学习基础】回报（累计奖励）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%9B%9E%E6%8A%A5%EF%BC%88%E7%B4%AF%E8%AE%A1%E5%A5%96%E5%8A%B1%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%9B%9E%E6%8A%A5%EF%BC%88%E7%B4%AF%E8%AE%A1%E5%A5%96%E5%8A%B1%EF%BC%89.png)

### <a name="header-43"></a>【强化学习基础】反向迭代并计算回报G
[![【强化学习基础】反向迭代并计算回报G](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%8F%8D%E5%90%91%E8%BF%AD%E4%BB%A3%E5%B9%B6%E8%AE%A1%E7%AE%97%E5%9B%9E%E6%8A%A5G.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%8F%8D%E5%90%91%E8%BF%AD%E4%BB%A3%E5%B9%B6%E8%AE%A1%E7%AE%97%E5%9B%9E%E6%8A%A5G.png)

### <a name="header-44"></a>【强化学习基础】奖励（Reward）、回报（Return）、价值（Value）的关系
[![【强化学习基础】奖励、回报、价值的关系](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%A5%96%E5%8A%B1%E3%80%81%E5%9B%9E%E6%8A%A5%E3%80%81%E4%BB%B7%E5%80%BC%E7%9A%84%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%A5%96%E5%8A%B1%E3%80%81%E5%9B%9E%E6%8A%A5%E3%80%81%E4%BB%B7%E5%80%BC%E7%9A%84%E5%85%B3%E7%B3%BB.png)

### <a name="header-45"></a>【强化学习基础】价值函数Qπ与Vπ的关系
[![【强化学习基础】价值函数Qπ与Vπ的关系](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E4%BB%B7%E5%80%BC%E5%87%BD%E6%95%B0Q%CF%80%E4%B8%8EV%CF%80%E7%9A%84%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E4%BB%B7%E5%80%BC%E5%87%BD%E6%95%B0Q%CF%80%E4%B8%8EV%CF%80%E7%9A%84%E5%85%B3%E7%B3%BB.png)

### <a name="header-46"></a>【强化学习基础】蒙特卡洛（Monte Carlo，MC）法预估状态St的价值
[![【强化学习基础】蒙特卡洛法预估状态St的价值](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%E6%B3%95%E9%A2%84%E4%BC%B0%E7%8A%B6%E6%80%81St%E7%9A%84%E4%BB%B7%E5%80%BC.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%E6%B3%95%E9%A2%84%E4%BC%B0%E7%8A%B6%E6%80%81St%E7%9A%84%E4%BB%B7%E5%80%BC.png)

### <a name="header-47"></a>【强化学习基础】TD目标与TD误差的关系（TD target and TD error）
[![【强化学习基础】TD目标与TD误差的关系](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91TD%E7%9B%AE%E6%A0%87%E4%B8%8ETD%E8%AF%AF%E5%B7%AE%E7%9A%84%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91TD%E7%9B%AE%E6%A0%87%E4%B8%8ETD%E8%AF%AF%E5%B7%AE%E7%9A%84%E5%85%B3%E7%B3%BB.png)

### <a name="header-48"></a>【强化学习基础】TD(0)、多步TD与蒙特卡洛（MC）的关系
[![【强化学习基础】TD(0)、多步TD与蒙特卡洛（MC）的关系](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91TD%280%29%E3%80%81%E5%A4%9A%E6%AD%A5TD%E4%B8%8E%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%EF%BC%88MC%EF%BC%89%E7%9A%84%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91TD%280%29%E3%80%81%E5%A4%9A%E6%AD%A5TD%E4%B8%8E%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%EF%BC%88MC%EF%BC%89%E7%9A%84%E5%85%B3%E7%B3%BB.png)

### <a name="header-49"></a>【强化学习基础】蒙特卡洛方法与TD方法的特性
[![【强化学习基础】蒙特卡洛方法与TD方法的特性](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%E6%96%B9%E6%B3%95%E4%B8%8ETD%E6%96%B9%E6%B3%95%E7%9A%84%E7%89%B9%E6%80%A7.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%E6%96%B9%E6%B3%95%E4%B8%8ETD%E6%96%B9%E6%B3%95%E7%9A%84%E7%89%B9%E6%80%A7.png)

### <a name="header-50"></a>【强化学习基础】蒙特卡洛、TD、DP、穷举搜索的关系 <sup>[<a href="./src/references.md">32</a>]</sup>
[![【强化学习基础】蒙特卡洛、TD、DP、穷举搜索的关系](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%E3%80%81TD%E3%80%81DP%E3%80%81%E7%A9%B7%E4%B8%BE%E6%90%9C%E7%B4%A2%E7%9A%84%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%92%99%E7%89%B9%E5%8D%A1%E6%B4%9B%E3%80%81TD%E3%80%81DP%E3%80%81%E7%A9%B7%E4%B8%BE%E6%90%9C%E7%B4%A2%E7%9A%84%E5%85%B3%E7%B3%BB.png)

### <a name="header-51"></a>【强化学习基础】两种输入输出结构的DQN（Deep Q-Network）模型
[![【强化学习基础】两种输入输出结构的DQN模型](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E4%B8%A4%E7%A7%8D%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA%E7%BB%93%E6%9E%84%E7%9A%84DQN%E6%A8%A1%E5%9E%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E4%B8%A4%E7%A7%8D%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA%E7%BB%93%E6%9E%84%E7%9A%84DQN%E6%A8%A1%E5%9E%8B.png)

### <a name="header-52"></a>【强化学习基础】DQN的实际应用示例
[![【强化学习基础】DQN的实际应用示例](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91DQN%E7%9A%84%E5%AE%9E%E9%99%85%E5%BA%94%E7%94%A8%E7%A4%BA%E4%BE%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91DQN%E7%9A%84%E5%AE%9E%E9%99%85%E5%BA%94%E7%94%A8%E7%A4%BA%E4%BE%8B.png)

### <a name="header-53"></a>【强化学习基础】DQN的“高估”问题
[![【强化学习基础】DQN的“高估”问题](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91DQN%E7%9A%84%E2%80%9C%E9%AB%98%E4%BC%B0%E2%80%9D%E9%97%AE%E9%A2%98.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91DQN%E7%9A%84%E2%80%9C%E9%AB%98%E4%BC%B0%E2%80%9D%E9%97%AE%E9%A2%98.png)

### <a name="header-54"></a>【强化学习基础】基于价值vs基于策略（Value-Based vs Policy-Based）
[![【强化学习基础】基于价值vs基于策略](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%9F%BA%E4%BA%8E%E4%BB%B7%E5%80%BCvs%E5%9F%BA%E4%BA%8E%E7%AD%96%E7%95%A5.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%9F%BA%E4%BA%8E%E4%BB%B7%E5%80%BCvs%E5%9F%BA%E4%BA%8E%E7%AD%96%E7%95%A5.png)

### <a name="header-55"></a>【强化学习基础】策略梯度（Policy Gradient）
[![【强化学习基础】策略梯度](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E7%AD%96%E7%95%A5%E6%A2%AF%E5%BA%A6.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E7%AD%96%E7%95%A5%E6%A2%AF%E5%BA%A6.png)

### <a name="header-56"></a>【强化学习基础】多智能体强化学习（MARL，Multi-agent reinforcement learning）
[![【强化学习基础】多智能体强化学习（MARL）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%A4%9A%E6%99%BA%E8%83%BD%E4%BD%93%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88MARL%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%A4%9A%E6%99%BA%E8%83%BD%E4%BD%93%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88MARL%EF%BC%89.png)

### <a name="header-57"></a>【强化学习基础】多智能体DDPG <sup>[<a href="./src/references.md">41</a>]</sup>
[![【强化学习基础】多智能体DDPG](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%A4%9A%E6%99%BA%E8%83%BD%E4%BD%93DDPG.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%A4%9A%E6%99%BA%E8%83%BD%E4%BD%93DDPG.png)

### <a name="header-58"></a>【强化学习基础】模仿学习（IL，Imitation Learning）
[![【强化学习基础】模仿学习（IL）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E6%A8%A1%E4%BB%BF%E5%AD%A6%E4%B9%A0%EF%BC%88IL%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E6%A8%A1%E4%BB%BF%E5%AD%A6%E4%B9%A0%EF%BC%88IL%EF%BC%89.png)

### <a name="header-59"></a>【强化学习基础】行为克隆（BC，Behavior Cloning）
[![【强化学习基础】行为克隆（BC）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%A1%8C%E4%B8%BA%E5%85%8B%E9%9A%86%EF%BC%88BC%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E8%A1%8C%E4%B8%BA%E5%85%8B%E9%9A%86%EF%BC%88BC%EF%BC%89.png)

### <a name="header-60"></a>【强化学习基础】逆向强化学习（IRL，Inverse RL）、强化学习（RL）
[![【强化学习基础】逆向强化学习（IRL）、强化学习（RL）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E9%80%86%E5%90%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88IRL%EF%BC%89%E3%80%81%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88RL%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E9%80%86%E5%90%91%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88IRL%EF%BC%89%E3%80%81%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88RL%EF%BC%89.png)

### <a name="header-61"></a>【强化学习基础】有模型（Model-Based）、无模型（Model-Free）
[![【强化学习基础】有模型（Model-Based）、无模型（Model-Free）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E6%9C%89%E6%A8%A1%E5%9E%8B%EF%BC%88Model-Based%EF%BC%89%E3%80%81%E6%97%A0%E6%A8%A1%E5%9E%8B%EF%BC%88Model-Free%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E6%9C%89%E6%A8%A1%E5%9E%8B%EF%BC%88Model-Based%EF%BC%89%E3%80%81%E6%97%A0%E6%A8%A1%E5%9E%8B%EF%BC%88Model-Free%EF%BC%89.png)

### <a name="header-62"></a>【强化学习基础】封建等级强化学习（Feudal RL）
[![【强化学习基础】封建等级强化学习（Feudal RL）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%B0%81%E5%BB%BA%E7%AD%89%E7%BA%A7%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88Feudal%20RL%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%B0%81%E5%BB%BA%E7%AD%89%E7%BA%A7%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88Feudal%20RL%EF%BC%89.png)

### <a name="header-63"></a>【强化学习基础】分布价值强化学习（Distributional RL）
[![【强化学习基础】分布价值强化学习（Distributional RL）](images_chinese/png_small/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%88%86%E5%B8%83%E4%BB%B7%E5%80%BC%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88Distributional%20RL%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%9F%BA%E7%A1%80%E3%80%91%E5%88%86%E5%B8%83%E4%BB%B7%E5%80%BC%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%EF%BC%88Distributional%20RL%EF%BC%89.png)

### <a name="header-64"></a>【策略优化架构算法及其衍生】Actor-Critic架构
[![【策略优化架构算法及其衍生】Actor-Critic架构](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91Actor-Critic%E6%9E%B6%E6%9E%84.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91Actor-Critic%E6%9E%B6%E6%9E%84.png)

### <a name="header-65"></a>【策略优化架构算法及其衍生】引入基线与优势（Advantage）函数A的作用
[![【策略优化架构算法及其衍生】引入基线与优势函数A的作用](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E5%BC%95%E5%85%A5%E5%9F%BA%E7%BA%BF%E4%B8%8E%E4%BC%98%E5%8A%BF%E5%87%BD%E6%95%B0A%E7%9A%84%E4%BD%9C%E7%94%A8.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E5%BC%95%E5%85%A5%E5%9F%BA%E7%BA%BF%E4%B8%8E%E4%BC%98%E5%8A%BF%E5%87%BD%E6%95%B0A%E7%9A%84%E4%BD%9C%E7%94%A8.png)

### <a name="header-66"></a>【策略优化架构算法及其衍生】GAE（广义优势估计,Generalized Advantage Estimation）算法
[![【策略优化架构算法及其衍生】GAE（广义优势估计）算法](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91GAE%EF%BC%88%E5%B9%BF%E4%B9%89%E4%BC%98%E5%8A%BF%E4%BC%B0%E8%AE%A1%EF%BC%89%E7%AE%97%E6%B3%95.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91GAE%EF%BC%88%E5%B9%BF%E4%B9%89%E4%BC%98%E5%8A%BF%E4%BC%B0%E8%AE%A1%EF%BC%89%E7%AE%97%E6%B3%95.png)

### <a name="header-67"></a>【策略优化架构算法及其衍生】PPO（Proximal Policy Optimization）算法的演进
[![【策略优化架构算法及其衍生】PPO算法的演进](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91PPO%E7%AE%97%E6%B3%95%E7%9A%84%E6%BC%94%E8%BF%9B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91PPO%E7%AE%97%E6%B3%95%E7%9A%84%E6%BC%94%E8%BF%9B.png)

### <a name="header-68"></a>【策略优化架构算法及其衍生】TRPO（Trust Region Policy Optimization）及其置信域
[![【策略优化架构算法及其衍生】TRPO及其置信域](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91TRPO%E5%8F%8A%E5%85%B6%E7%BD%AE%E4%BF%A1%E5%9F%9F.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91TRPO%E5%8F%8A%E5%85%B6%E7%BD%AE%E4%BF%A1%E5%9F%9F.png)

### <a name="header-69"></a>【策略优化架构算法及其衍生】重要性采样（Importance sampling）
[![【策略优化架构算法及其衍生】重要性采样](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E9%87%8D%E8%A6%81%E6%80%A7%E9%87%87%E6%A0%B7.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E9%87%8D%E8%A6%81%E6%80%A7%E9%87%87%E6%A0%B7.png)

### <a name="header-70"></a>【策略优化架构算法及其衍生】PPO-Clip
[![【策略优化架构算法及其衍生】PPO-Clip](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91PPO-Clip.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91PPO-Clip.png)

### <a name="header-71"></a>【策略优化架构算法及其衍生】PPO训练中策略模型的更新过程
[![【策略优化架构算法及其衍生】PPO训练中策略模型的更新过程](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E7%AD%96%E7%95%A5%E6%A8%A1%E5%9E%8B%E7%9A%84%E6%9B%B4%E6%96%B0%E8%BF%87%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E7%AD%96%E7%95%A5%E6%A8%A1%E5%9E%8B%E7%9A%84%E6%9B%B4%E6%96%B0%E8%BF%87%E7%A8%8B.png)

### <a name="header-72"></a>【策略优化架构算法及其衍生】PPO与GRPO（Group Relative Policy Optimization） <sup>[<a href="./src/references.md">72</a>]</sup>
[![【策略优化架构算法及其衍生】GRPO&PPO](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91GRPO%26PPO.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91GRPO%26PPO.png)

### <a name="header-73"></a>【策略优化架构算法及其衍生】确定性策略vs随机性策略（Deterministic policy vs. Stochastic policy）
[![【策略优化架构算法及其衍生】确定性策略vs随机性策略](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E7%A1%AE%E5%AE%9A%E6%80%A7%E7%AD%96%E7%95%A5vs%E9%9A%8F%E6%9C%BA%E6%80%A7%E7%AD%96%E7%95%A5.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E7%A1%AE%E5%AE%9A%E6%80%A7%E7%AD%96%E7%95%A5vs%E9%9A%8F%E6%9C%BA%E6%80%A7%E7%AD%96%E7%95%A5.png)

### <a name="header-74"></a>【策略优化架构算法及其衍生】确定性策略梯度（DPG）
[![【策略优化架构算法及其衍生】确定性策略梯度（DPG）](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E7%A1%AE%E5%AE%9A%E6%80%A7%E7%AD%96%E7%95%A5%E6%A2%AF%E5%BA%A6%EF%BC%88DPG%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91%E7%A1%AE%E5%AE%9A%E6%80%A7%E7%AD%96%E7%95%A5%E6%A2%AF%E5%BA%A6%EF%BC%88DPG%EF%BC%89.png)

### <a name="header-75"></a>【策略优化架构算法及其衍生】DDPG（Deep Deterministic Policy Gradient）
[![【策略优化架构算法及其衍生】DDPG](images_chinese/png_small/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91DDPG.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96%E6%9E%B6%E6%9E%84%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E8%A1%8D%E7%94%9F%E3%80%91DDPG.png)

### <a name="header-76"></a>【RLHF与RLAIF】语言模型的强化学习建模
[![【RLHF与RLAIF】语言模型的强化学习建模](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E8%AF%AD%E8%A8%80%E6%A8%A1%E5%9E%8B%E7%9A%84%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%BB%BA%E6%A8%A1.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E8%AF%AD%E8%A8%80%E6%A8%A1%E5%9E%8B%E7%9A%84%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0%E5%BB%BA%E6%A8%A1.png)

### <a name="header-77"></a>【RLHF与RLAIF】RLHF的两阶段式训练流程
[![【RLHF与RLAIF】RLHF的两阶段式训练流程](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91RLHF%E7%9A%84%E4%B8%A4%E9%98%B6%E6%AE%B5%E5%BC%8F%E8%AE%AD%E7%BB%83%E6%B5%81%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91RLHF%E7%9A%84%E4%B8%A4%E9%98%B6%E6%AE%B5%E5%BC%8F%E8%AE%AD%E7%BB%83%E6%B5%81%E7%A8%8B.png)

### <a name="header-78"></a>【RLHF与RLAIF】奖励模型（RM）的结构
[![【RLHF与RLAIF】奖励模型的结构](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E7%9A%84%E7%BB%93%E6%9E%84.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E7%9A%84%E7%BB%93%E6%9E%84.png)

### <a name="header-79"></a>【RLHF与RLAIF】奖励模型的输入输出
[![【RLHF与RLAIF】奖励模型的输入输出](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E7%9A%84%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E7%9A%84%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA.png)

### <a name="header-80"></a>【RLHF与RLAIF】奖励模型预测偏差与Loss的关系
[![【RLHF与RLAIF】奖励模型预测偏差与Loss的关系](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E9%A2%84%E6%B5%8B%E5%81%8F%E5%B7%AE%E4%B8%8ELoss%E7%9A%84%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E9%A2%84%E6%B5%8B%E5%81%8F%E5%B7%AE%E4%B8%8ELoss%E7%9A%84%E5%85%B3%E7%B3%BB.png)

### <a name="header-81"></a>【RLHF与RLAIF】奖励模型的训练
[![【RLHF与RLAIF】奖励模型的训练](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E7%9A%84%E8%AE%AD%E7%BB%83.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%A5%96%E5%8A%B1%E6%A8%A1%E5%9E%8B%E7%9A%84%E8%AE%AD%E7%BB%83.png)

### <a name="header-82"></a>【RLHF与RLAIF】PPO训练中四种模型的合作关系
[![【RLHF与RLAIF】PPO训练中四种模型的合作关系](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E5%9B%9B%E7%A7%8D%E6%A8%A1%E5%9E%8B%E7%9A%84%E5%90%88%E4%BD%9C%E5%85%B3%E7%B3%BB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E5%9B%9B%E7%A7%8D%E6%A8%A1%E5%9E%8B%E7%9A%84%E5%90%88%E4%BD%9C%E5%85%B3%E7%B3%BB.png)

### <a name="header-83"></a>【RLHF与RLAIF】PPO训练中四种模型的结构与初始化
[![【RLHF与RLAIF】PPO训练中四种模型的结构与初始化](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E5%9B%9B%E7%A7%8D%E6%A8%A1%E5%9E%8B%E7%9A%84%E7%BB%93%E6%9E%84%E4%B8%8E%E5%88%9D%E5%A7%8B%E5%8C%96.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E5%9B%9B%E7%A7%8D%E6%A8%A1%E5%9E%8B%E7%9A%84%E7%BB%93%E6%9E%84%E4%B8%8E%E5%88%9D%E5%A7%8B%E5%8C%96.png)

### <a name="header-84"></a>【RLHF与RLAIF】一个双头结构的价值模型
[![【RLHF与RLAIF】一个双头结构的价值模型](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E4%B8%80%E4%B8%AA%E5%8F%8C%E5%A4%B4%E7%BB%93%E6%9E%84%E7%9A%84%E4%BB%B7%E5%80%BC%E6%A8%A1%E5%9E%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E4%B8%80%E4%B8%AA%E5%8F%8C%E5%A4%B4%E7%BB%93%E6%9E%84%E7%9A%84%E4%BB%B7%E5%80%BC%E6%A8%A1%E5%9E%8B.png)

### <a name="header-85"></a>【RLHF与RLAIF】RLHF：四种模型可以共享同一个底座
[![【RLHF与RLAIF】RLHF：四种模型可以共享同一个底座](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91RLHF%EF%BC%9A%E5%9B%9B%E7%A7%8D%E6%A8%A1%E5%9E%8B%E5%8F%AF%E4%BB%A5%E5%85%B1%E4%BA%AB%E5%90%8C%E4%B8%80%E4%B8%AA%E5%BA%95%E5%BA%A7.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91RLHF%EF%BC%9A%E5%9B%9B%E7%A7%8D%E6%A8%A1%E5%9E%8B%E5%8F%AF%E4%BB%A5%E5%85%B1%E4%BA%AB%E5%90%8C%E4%B8%80%E4%B8%AA%E5%BA%95%E5%BA%A7.png)

### <a name="header-86"></a>【RLHF与RLAIF】PPO训练中各模型的输入与输出
[![【RLHF与RLAIF】PPO训练中各模型的输入与输出](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E5%90%84%E6%A8%A1%E5%9E%8B%E7%9A%84%E8%BE%93%E5%85%A5%E4%B8%8E%E8%BE%93%E5%87%BA.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%AD%E5%90%84%E6%A8%A1%E5%9E%8B%E7%9A%84%E8%BE%93%E5%85%A5%E4%B8%8E%E8%BE%93%E5%87%BA.png)

### <a name="header-87"></a>【RLHF与RLAIF】PPO训练中KL距离的计算过程
[![【RLHF与RLAIF】PPO训练中KL距离的计算过程](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%ADKL%E8%B7%9D%E7%A6%BB%E7%9A%84%E8%AE%A1%E7%AE%97%E8%BF%87%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91PPO%E8%AE%AD%E7%BB%83%E4%B8%ADKL%E8%B7%9D%E7%A6%BB%E7%9A%84%E8%AE%A1%E7%AE%97%E8%BF%87%E7%A8%8B.png)

### <a name="header-88"></a>【RLHF与RLAIF】基于PPO进行RLHF训练的原理图
[![【RLHF与RLAIF】基于PPO进行RLHF训练的原理图](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%9F%BA%E4%BA%8EPPO%E8%BF%9B%E8%A1%8CRLHF%E8%AE%AD%E7%BB%83%E7%9A%84%E5%8E%9F%E7%90%86%E5%9B%BE.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E5%9F%BA%E4%BA%8EPPO%E8%BF%9B%E8%A1%8CRLHF%E8%AE%AD%E7%BB%83%E7%9A%84%E5%8E%9F%E7%90%86%E5%9B%BE.png)

### <a name="header-89"></a>【RLHF与RLAIF】拒绝采样（Rejection Sampling）微调
[![【RLHF与RLAIF】拒绝采样微调](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E6%8B%92%E7%BB%9D%E9%87%87%E6%A0%B7%E5%BE%AE%E8%B0%83.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91%E6%8B%92%E7%BB%9D%E9%87%87%E6%A0%B7%E5%BE%AE%E8%B0%83.png)

### <a name="header-90"></a>【RLHF与RLAIF】RLAIF与RLHF的区别
[![【RLHF与RLAIF】RLAIF与RLHF的区别](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91RLAIF%E4%B8%8ERLHF%E7%9A%84%E5%8C%BA%E5%88%AB.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91RLAIF%E4%B8%8ERLHF%E7%9A%84%E5%8C%BA%E5%88%AB.png)

### <a name="header-91"></a>【RLHF与RLAIF】Claude模型应用的宪法AI（CAI）原理
[![【RLHF与RLAIF】Claude模型应用的宪法AI原理](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91Claude%E6%A8%A1%E5%9E%8B%E5%BA%94%E7%94%A8%E7%9A%84%E5%AE%AA%E6%B3%95AI%E5%8E%9F%E7%90%86.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91Claude%E6%A8%A1%E5%9E%8B%E5%BA%94%E7%94%A8%E7%9A%84%E5%AE%AA%E6%B3%95AI%E5%8E%9F%E7%90%86.png)

### <a name="header-92"></a>【RLHF与RLAIF】OpenAI RBR（基于规则的奖励）
[![【RLHF与RLAIF】OpenAI RBR（基于规则的奖励）](images_chinese/png_small/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91OpenAI%20RBR%EF%BC%88%E5%9F%BA%E4%BA%8E%E8%A7%84%E5%88%99%E7%9A%84%E5%A5%96%E5%8A%B1%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90RLHF%E4%B8%8ERLAIF%E3%80%91OpenAI%20RBR%EF%BC%88%E5%9F%BA%E4%BA%8E%E8%A7%84%E5%88%99%E7%9A%84%E5%A5%96%E5%8A%B1%EF%BC%89.png)

### <a name="header-93"></a>【逻辑推理能力优化】基于CoT的知识蒸馏（Knowledge Distillation）
[![【逻辑推理能力优化】基于CoT的知识蒸馏](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E5%9F%BA%E4%BA%8ECoT%E7%9A%84%E7%9F%A5%E8%AF%86%E8%92%B8%E9%A6%8F.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E5%9F%BA%E4%BA%8ECoT%E7%9A%84%E7%9F%A5%E8%AF%86%E8%92%B8%E9%A6%8F.png)

### <a name="header-94"></a>【逻辑推理能力优化】基于DeepSeek进行蒸馏
[![【逻辑推理能力优化】基于DeepSeek进行蒸馏](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E5%9F%BA%E4%BA%8EDeepSeek%E8%BF%9B%E8%A1%8C%E8%92%B8%E9%A6%8F.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E5%9F%BA%E4%BA%8EDeepSeek%E8%BF%9B%E8%A1%8C%E8%92%B8%E9%A6%8F.png)

### <a name="header-95"></a>【逻辑推理能力优化】ORM和PRM（结果奖励模型和过程奖励模型）
[![【逻辑推理能力优化】ORM和PRM](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91ORM%E5%92%8CPRM.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91ORM%E5%92%8CPRM.png)

### <a name="header-96"></a>【逻辑推理能力优化】MCTS每次迭代的四个关键步骤
[![【逻辑推理能力优化】MCTS每次迭代的四个关键步骤](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91MCTS%E6%AF%8F%E6%AC%A1%E8%BF%AD%E4%BB%A3%E7%9A%84%E5%9B%9B%E4%B8%AA%E5%85%B3%E9%94%AE%E6%AD%A5%E9%AA%A4.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91MCTS%E6%AF%8F%E6%AC%A1%E8%BF%AD%E4%BB%A3%E7%9A%84%E5%9B%9B%E4%B8%AA%E5%85%B3%E9%94%AE%E6%AD%A5%E9%AA%A4.png)

### <a name="header-97"></a>【逻辑推理能力优化】MCTS的运行过程
[![【逻辑推理能力优化】MCTS的运行过程](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91MCTS%E7%9A%84%E8%BF%90%E8%A1%8C%E8%BF%87%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91MCTS%E7%9A%84%E8%BF%90%E8%A1%8C%E8%BF%87%E7%A8%8B.png)

### <a name="header-98"></a>【逻辑推理能力优化】语言场景下的搜索树示例
[![【逻辑推理能力优化】语言场景下的搜索树示例](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E8%AF%AD%E8%A8%80%E5%9C%BA%E6%99%AF%E4%B8%8B%E7%9A%84%E6%90%9C%E7%B4%A2%E6%A0%91%E7%A4%BA%E4%BE%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E8%AF%AD%E8%A8%80%E5%9C%BA%E6%99%AF%E4%B8%8B%E7%9A%84%E6%90%9C%E7%B4%A2%E6%A0%91%E7%A4%BA%E4%BE%8B.png)

### <a name="header-99"></a>【逻辑推理能力优化】BoN（Best-of-N）采样
[![【逻辑推理能力优化】BoN（Best-of-N）采样](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91BoN%EF%BC%88Best-of-N%EF%BC%89%E9%87%87%E6%A0%B7.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91BoN%EF%BC%88Best-of-N%EF%BC%89%E9%87%87%E6%A0%B7.png)

### <a name="header-100"></a>【逻辑推理能力优化】多数投票（Majority Vote）方法
[![【逻辑推理能力优化】多数投票（Majority Vote）方法](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E5%A4%9A%E6%95%B0%E6%8A%95%E7%A5%A8%EF%BC%88Majority%20Vote%EF%BC%89%E6%96%B9%E6%B3%95.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91%E5%A4%9A%E6%95%B0%E6%8A%95%E7%A5%A8%EF%BC%88Majority%20Vote%EF%BC%89%E6%96%B9%E6%B3%95.png)

### <a name="header-101"></a>【逻辑推理能力优化】AlphaGoZero在训练时的性能增长趋势 <sup>[<a href="./src/references.md">179</a>]</sup>
[![【逻辑推理能力优化】AlphaGoZero在训练时的性能增长趋势](images_chinese/png_small/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91AlphaGoZero%E5%9C%A8%E8%AE%AD%E7%BB%83%E6%97%B6%E7%9A%84%E6%80%A7%E8%83%BD%E5%A2%9E%E9%95%BF%E8%B6%8B%E5%8A%BF.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90%E9%80%BB%E8%BE%91%E6%8E%A8%E7%90%86%E8%83%BD%E5%8A%9B%E4%BC%98%E5%8C%96%E3%80%91AlphaGoZero%E5%9C%A8%E8%AE%AD%E7%BB%83%E6%97%B6%E7%9A%84%E6%80%A7%E8%83%BD%E5%A2%9E%E9%95%BF%E8%B6%8B%E5%8A%BF.png)

### <a name="header-102"></a>【LLM基础拓展】大模型性能优化技术图谱
[![【LLM基础拓展】大模型性能优化技术图谱](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E5%A4%A7%E6%A8%A1%E5%9E%8B%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E5%9B%BE%E8%B0%B1.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E5%A4%A7%E6%A8%A1%E5%9E%8B%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96%E6%8A%80%E6%9C%AF%E5%9B%BE%E8%B0%B1.png)

### <a name="header-103"></a>【LLM基础拓展】ALiBi位置编码
- RoPE已成主流，ALiBi逐渐被抛弃
[![【LLM基础拓展】ALiBi位置编码](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91ALiBi%E4%BD%8D%E7%BD%AE%E7%BC%96%E7%A0%81.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91ALiBi%E4%BD%8D%E7%BD%AE%E7%BC%96%E7%A0%81.png)

### <a name="header-104"></a>【LLM基础拓展】传统的知识蒸馏
[![【LLM基础拓展】传统的知识蒸馏](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E4%BC%A0%E7%BB%9F%E7%9A%84%E7%9F%A5%E8%AF%86%E8%92%B8%E9%A6%8F.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E4%BC%A0%E7%BB%9F%E7%9A%84%E7%9F%A5%E8%AF%86%E8%92%B8%E9%A6%8F.png)

### <a name="header-105"></a>【LLM基础拓展】数值表示、量化（Quantization）
[![【LLM基础拓展】数值表示、量化](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E6%95%B0%E5%80%BC%E8%A1%A8%E7%A4%BA%E3%80%81%E9%87%8F%E5%8C%96.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E6%95%B0%E5%80%BC%E8%A1%A8%E7%A4%BA%E3%80%81%E9%87%8F%E5%8C%96.png)

### <a name="header-106"></a>【LLM基础拓展】常规训练时前向和反向过程
[![【LLM基础拓展】常规训练时前向和反向过程](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E5%B8%B8%E8%A7%84%E8%AE%AD%E7%BB%83%E6%97%B6%E5%89%8D%E5%90%91%E5%92%8C%E5%8F%8D%E5%90%91%E8%BF%87%E7%A8%8B.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E5%B8%B8%E8%A7%84%E8%AE%AD%E7%BB%83%E6%97%B6%E5%89%8D%E5%90%91%E5%92%8C%E5%8F%8D%E5%90%91%E8%BF%87%E7%A8%8B.png)

### <a name="header-107"></a>【LLM基础拓展】梯度累积（Gradient Accumulation）训练
[![【LLM基础拓展】梯度累积（Gradient Accumulation）训练](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E6%A2%AF%E5%BA%A6%E7%B4%AF%E7%A7%AF%EF%BC%88Gradient%20Accumulation%EF%BC%89%E8%AE%AD%E7%BB%83.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E6%A2%AF%E5%BA%A6%E7%B4%AF%E7%A7%AF%EF%BC%88Gradient%20Accumulation%EF%BC%89%E8%AE%AD%E7%BB%83.png)

### <a name="header-108"></a>【LLM基础拓展】Gradient Checkpoint（梯度重计算）
[![【LLM基础拓展】Gradient Checkpoint（梯度重计算）](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Gradient%20Checkpoint%EF%BC%88%E6%A2%AF%E5%BA%A6%E9%87%8D%E8%AE%A1%E7%AE%97%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Gradient%20Checkpoint%EF%BC%88%E6%A2%AF%E5%BA%A6%E9%87%8D%E8%AE%A1%E7%AE%97%EF%BC%89.png)

### <a name="header-109"></a>【LLM基础拓展】Full recomputation(完全重计算)
[![【LLM基础拓展】Full recomputation(完全重计算)](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Full%20recomputation%28%E5%AE%8C%E5%85%A8%E9%87%8D%E8%AE%A1%E7%AE%97%29.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Full%20recomputation%28%E5%AE%8C%E5%85%A8%E9%87%8D%E8%AE%A1%E7%AE%97%29.png)

### <a name="header-110"></a>【LLM基础拓展】LLM Benchmark
[![【LLM基础拓展】LLM Benchmark](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91LLM%20Benchmark.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91LLM%20Benchmark.png)

### <a name="header-111"></a>【LLM基础拓展】MHA、GQA、MQA、MLA
[![【LLM基础拓展】MHA、GQA、MQA、MLA](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91MHA%E3%80%81GQA%E3%80%81MQA%E3%80%81MLA.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91MHA%E3%80%81GQA%E3%80%81MQA%E3%80%81MLA.png)

### <a name="header-112"></a>【LLM基础拓展】RNN（Recurrent Neural Network）
[![【LLM基础拓展】RNN](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RNN.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RNN.png)

### <a name="header-113"></a>【LLM基础拓展】Pre-norm和Post-norm
[![【LLM基础拓展】Pre-norm和Post-norm](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Pre-norm%E5%92%8CPost-norm.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Pre-norm%E5%92%8CPost-norm.png)

### <a name="header-114"></a>【LLM基础拓展】BatchNorm和LayerNorm
- （待续，持续补充注释中 ...）
[![【LLM基础拓展】BatchNorm和LayerNorm](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91BatchNorm%E5%92%8CLayerNorm.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91BatchNorm%E5%92%8CLayerNorm.png)

### <a name="header-115"></a>【LLM基础拓展】RMSNorm
- RMSNorm（Root Mean Square Layer Normalization）是一种归一化方法，仅基于输入特征的均方根值（RMS）进行规范化，**不计算均值偏移**。  
- 对每个样本的特征向量 \(x\)，先计算 \(\mathrm{RMS}(x)=\sqrt{\tfrac{1}{d}\sum_i x_i^2}\)，再做缩放：\(\hat{x}=x / \mathrm{RMS}(x)\times \gamma + \beta\)。  
- 相较于 LayerNorm，它省略了减均值步骤，计算更高效且在多种 Transformer 架构中表现相近或更优。
[![【LLM基础拓展】RMSNorm](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RMSNorm.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RMSNorm.png)

### <a name="header-116"></a>【LLM基础拓展】Prune（剪枝）
- 剪枝是在训练或静态模型中去除**不重要**的权重（如小于阈值的连接）或整个神经元/通道，以减少模型规模和计算量。  
- 典型流程包括：评估重要性 → 标记待剪参数 → 重训练（Fine-tuning）→ 验证性能。  
- 有助于加速推理、降低内存占用，但需要小心避免过度剪枝导致性能大幅下降。
[![【LLM基础拓展】Prune（剪枝）](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Prune%EF%BC%88%E5%89%AA%E6%9E%9D%EF%BC%89.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91Prune%EF%BC%88%E5%89%AA%E6%9E%9D%EF%BC%89.png)

### <a name="header-117"></a>【LLM基础拓展】温度系数的作用
- 在生成阶段，温度系数 \(T\) 通过放缩模型输出的 logits 分布来控制采样**多样性**。  
- 当 \(T < 1\) 时，分布“尖锐”，模型更倾向于选择概率**最高**的 token，回答更固定。
- 当 \(T > 1\) 时，分布“平坦”，采样结果更具**随机性**。  
- 适当调整温度可以在准确性和创造性之间取得平衡——低温度提升确定性，高温度增强多样性。
[![【LLM基础拓展】温度系数的作用](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E6%B8%A9%E5%BA%A6%E7%B3%BB%E6%95%B0%E7%9A%84%E4%BD%9C%E7%94%A8.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91%E6%B8%A9%E5%BA%A6%E7%B3%BB%E6%95%B0%E7%9A%84%E4%BD%9C%E7%94%A8.png)

### <a name="header-118"></a>【LLM基础拓展】SwiGLU
- 基本结构：SwiGLU 是 Gated Linear Unit（GLU）的变体，将输入向量通过**两条**线性映射，一路直接输出，一路经过 SiLU（Swish）激活后作为门控信号，两者逐元素相乘得到最终输出。
- 激活**优势**：用 SiLU（Swish-1）替换原 GLU 中的 sigmoid，使门控更平滑、梯度更稳定，有助于加速训练收敛并提升下游任务表现。
[![【LLM基础拓展】SwiGLU](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91SwiGLU.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91SwiGLU.png)

### <a name="header-119"></a>【LLM基础拓展】AUC、PR、F1、Precision、Recall
被面试者、工程师经常混淆的算法常用指标，我画了一张图来对比总结，区别一目了然。
- **AUC**（Area Under the ROC Curve）：衡量二分类模型在所有可能阈值下区分正负样本的能力，ROC（Receiver Operating Characteristic）曲线以假正例率（FPR）为横轴、真正例率（TPR）为纵轴，AUC 值越接近 1 越好；若 AUC≈0.5 则相当于随机猜测。
- **PR Curve**（Precision–Recall Curve）：模型在不同召回率（Recall）下的精确率（Precision）变化趋势。可通过曲线下面积来综合评估模型对正类的检出能力。
- **Precision（精确率）**：在所有被预测为正例的样本中，实际为正例的比例，衡量误报率高低，适用于误报成本高的场景，个人认为“查准率”的翻译更贴切。Precision = TP / (TP + FP)
- **Recall （召回率）**：在所有真实为正例的样本中，被正确预测为正例的比例，衡量漏报率高低，适用于漏报成本高的场景，个人认为“查全率”的翻译更贴切。Recall = TP / (TP + FN)
- **F1 Score** （F1 值）：Precision 与 Recall 的调和平均，当两者平衡时取得最高分。F1 Score = 2 * (Precision * Recall) / (Precision + Recall)
- **Accuracy （准确率）**：在所有样本中，预测正确的比例，适用于类别分布较为均衡时的整体性能评估。Accuracy = (TP + TN) / (TP + TN + FP + FN)
- **BLEU**（Bilingual Evaluation Understudy；机器翻译评估指标）：基于 n-gram 重叠率评估翻译结果与参考的相似程度。
- **ROUGE**（Recall-Oriented Understudy for Gisting Evaluation；摘要评估指标）：生成摘要与参考在 n-gram、最长公共子序列或词重叠方面的匹配情况，关注召回性能。

[![【LLM基础拓展】AUC、PR、F1、Precision、Recall](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91AUC%E3%80%81PR%E3%80%81F1%E3%80%81Precision%E3%80%81Recall.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91AUC%E3%80%81PR%E3%80%81F1%E3%80%81Precision%E3%80%81Recall.png)


### <a name="header-120"></a>【LLM基础拓展】RoPE位置编码
- RoPE，Rotary Position Embedding，**旋转**位置编码，由苏剑林提出
- 原理：对 Transformer 中的 Query 和 Key 隐藏向量应用旋转变换（基于正弦、余弦函数），将位置信息编码为向量的**相位差**。
- 相对位置：旋转操作天然地保留了向量之间的相对角度差异，使模型能够捕捉**相对位置**信息而不依赖绝对位置索引。
- 优点：无需额外参数、计算**开销低**；在长序列场景下相较于传统绝对位置编码具有更好的泛化和性能。
[![【LLM基础拓展】RoPE位置编码](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RoPE%E4%BD%8D%E7%BD%AE%E7%BC%96%E7%A0%81.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RoPE%E4%BD%8D%E7%BD%AE%E7%BC%96%E7%A0%81.png)

### <a name="header-121"></a>【LLM基础拓展】RoPE对各序列位置、各维度的作用
- RoPE原理、Base与θ值、作用机制详见：[RoPE-theta-base.xlsx](./src/RoPE-theta-base.xlsx) 
- 维度成对旋转：将嵌入向量按奇偶索引**两两分组**，对每一对子向量应用一个二维旋转矩阵，旋转角度随位置和维度频率共同决定。
**高频**维度：对应下图左半区、角速度大的那些维度。旋转角度随位置变化快，对相邻 token 的位置微小差异非常敏感，擅长捕捉**短距离**的局部相对位置信息。
**低频**维度：对应下图右半区、角速度小的那些维度。旋转角度随位置变化慢，能够区分较**远距离**的相对位置信息，擅长建模全局或长距离依赖。
[![【LLM基础拓展】RoPE对各序列位置、各维度的作用](images_chinese/png_small/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RoPE%E5%AF%B9%E5%90%84%E5%BA%8F%E5%88%97%E4%BD%8D%E7%BD%AE%E3%80%81%E5%90%84%E7%BB%B4%E5%BA%A6%E7%9A%84%E4%BD%9C%E7%94%A8.png)](https://raw.githubusercontent.com/changyeyu/LLM-RL-Visualized/master/images_chinese/png_big/%E3%80%90LLM%E5%9F%BA%E7%A1%80%E6%8B%93%E5%B1%95%E3%80%91RoPE%E5%AF%B9%E5%90%84%E5%BA%8F%E5%88%97%E4%BD%8D%E7%BD%AE%E3%80%81%E5%90%84%E7%BB%B4%E5%BA%A6%E7%9A%84%E4%BD%9C%E7%94%A8.png)

<br>

---

## <a name="header-122"></a>本仓图片的文字详解、更多图见：《大模型算法：强化学习、微调与对齐》
### 书籍目录
#### 
<details>
<summary>折叠 / 展开目录</summary>

```python
第1章 大模型原理与技术概要
    1.1 图解大模型结构
        1.1.1 大语言模型（LLM）结构全景图
        1.1.2 输入层：分词、Token映射与向量生成
        1.1.3 输出层：Logits、概率分布与解码
        1.1.4 多模态语言模型（MLLM）与视觉语言模型（VLM）
    1.2 大模型训练全景图
    1.3 Scaling Law（性能的四大扩展规律）
第2章 SFT（监督微调）
    2.1 多种微调技术图解
        2.1.1 全参数微调、部分参数微调
        2.1.2 LoRA（低秩适配微调）——四两拨千斤
        2.1.3 LoRA衍生：QLoRA、AdaLoRA、PiSSA等
        2.1.4 基于提示的微调：Prefix-Tuning、Prompt Tuning等
        2.1.5 Adapter Tuning
        2.1.6 微调技术对比
        2.1.7 如何选择微调技术
    2.2 SFT原理深入解析
        2.2.1 SFT数据与ChatML格式化
        2.2.2 Logits与Token概率计算
        2.2.3 SFT的Label
        2.2.4 SFT的Loss图解
        2.2.5 对数概率（LogProbs）与LogSoftmax
    2.3 指令收集和处理
        2.3.1 收集指令的渠道和方法
        2.3.2 清洗指令的四要素
        2.3.3 数据预处理及常用工具
    2.4 SFT实践指南
        2.4.1 如何缓解SFT引入的幻觉？
        2.4.2 Token级Batch Size的换算
        2.4.3 Batch Size与学习率的Scaling Law
        2.4.4 SFT的七个技巧
第3章 DPO（直接偏好优化）
    3.1 DPO的核心思想
        3.1.1 DPO的提出背景与意义
        3.1.2 隐式的奖励模型
        3.1.3 Loss和优化目标
    3.2 偏好数据集的构建
        3.2.1 构建流程总览
        3.2.2 Prompt的收集
        3.2.3 问答数据对的清洗
        3.2.4 封装和预处理
    3.3 图解DPO的实现与训练
        3.3.1 模型的初始化
        3.3.2 DPO训练全景图
        3.3.3 DPO核心代码的提炼和解读
    3.4 DPO实践经验
        3.4.1 β参数如何调节
        3.4.2 DPO对模型能力的多维度影响
    3.5 DPO进阶
        3.5.1 DPO和RLHF（PPO）的对比
        3.5.2 理解DPO的梯度
第4章 免训练的效果优化技术
    4.1 提示工程
        4.1.1 Zero-Shot、One-Shot、Few-Shot
        4.1.2 Prompt设计的原则
    4.2 CoT（思维链）
        4.2.1 CoT原理图解
        4.2.2 ToT、GoT、XoT等衍生方法
        4.2.3 CoT的应用技巧
        4.2.4 CoT在多模态领域的应用
    4.3 生成控制和解码策略
        4.3.1 解码的原理与分类
        4.3.2 贪婪搜索
        4.3.3 Beam Search（波束搜索）：图解、衍生方法
        4.3.4 Top-K、Top-P等采样方法图解
        4.3.5 其他解码策略
        4.3.6 多种生成控制参数
    4.4 RAG（检索增强生成）
        4.4.1 RAG技术全景图
        4.4.2 RAG相关框架
    4.5 功能与工具调用（Function Calling）
        4.5.1 功能调用全景图
        4.5.2 功能调用的分类
第5章 强化学习基础
    5.1 强化学习核心
        5.1.1 强化学习：定义与区分
        5.1.2 强化学习的基础架构、核心概念
        5.1.3 马尔可夫决策过程（MDP）
        5.1.4 探索与利用、ε-贪婪策略
        5.1.5 同策略（On-policy）、异策略（Off-policy）
        5.1.6 在线/离线强化学习（Online/Offline RL）
        5.1.7 强化学习分类图
    5.2 价值函数、回报预估
        5.2.1 奖励、回报、折扣因子（R、G、γ）
        5.2.2 反向计算回报
        5.2.3 四种价值函数：Qπ、Vπ、V*、Q*
        5.2.4 奖励、回报、价值的区别
        5.2.5 贝尔曼方程——强化学习的基石
        5.2.6 Q和V的转换关系、转换图
        5.2.7 蒙特卡洛方法（MC）
    5.3 时序差分（TD）
        5.3.1 时序差分方法
        5.3.2 TD-Target和TD-Error
        5.3.3 TD(λ)、多步TD
        5.3.4 蒙特卡洛、TD、DP、穷举搜索的区别
    5.4 基于价值的算法
        5.4.1 Q-learning算法
        5.4.2 DQN
        5.4.3 DQN的Loss、训练过程
        5.4.4 DDQN、Dueling DQN等衍生算法
    5.5 策略梯度算法
        5.5.1 策略梯度（Policy Gradient）
        5.5.2 策略梯度定理
        5.5.3 REINFORCE和Actor-Critic：策略梯度的应用
    5.6 多智能体强化学习（MARL）
        5.6.1 MARL的原理与架构
        5.6.2 MARL的建模
        5.6.3 MARL的典型算法
    5.7 模仿学习（IL）
        5.7.1 模仿学习的定义、分类
        5.7.2 行为克隆（BC）
        5.7.3 逆向强化学习（IRL）
        5.7.4 生成对抗模仿学习（GAIL）
    5.8 强化学习高级拓展
        5.8.1 基于环境模型（Model-Based）的方法
        5.8.2 分层强化学习（HRL）
        5.8.3 分布价值强化学习（Distributional RL）
第6章 策略优化算法
    6.1 Actor-Critic（演员-评委）架构
        6.1.1 从策略梯度到Actor-Critic
        6.1.2 Actor-Critic架构图解
    6.2 优势函数与A2C
        6.2.1 优势函数（Advantage）
        6.2.2 A2C、A3C、SAC算法
        6.2.3 GAE（广义优势估计）算法
        6.2.4 γ和λ的调节作用
    6.3 PPO及其相关算法
        6.3.1 PPO算法的演进
        6.3.2 TRPO（置信域策略优化）
        6.3.3 重要性采样（Importance Sampling）
        6.3.4 PPO-Penalty
        6.3.5 PPO-Clip
        6.3.6 PPO的Loss的扩展
        6.3.7 TRPO与PPO的区别
        6.3.8 图解策略模型的训练
        6.3.9 深入解析PPO的本质
    6.4 GRPO算法
        6.4.1 GRPO的原理
        6.4.2 GRPO与PPO的区别
    6.5 确定性策略梯度（DPG）
        6.5.1 确定性策略vs随机性策略
        6.5.2 DPG、DDPG、TD3算法
第7章 RLHF与RLAIF
    7.1 RLHF（基于人类反馈的强化学习）概要
        7.1.1 RLHF的背景、发展
        7.1.2 语言模型的强化学习建模
        7.1.3 RLHF的训练样本、总流程
    7.2 阶段一：图解奖励模型的设计与训练
        7.2.1 奖励模型（Reward Model）的结构
        7.2.2 奖励模型的输入与奖励分数
        7.2.3 奖励模型的Loss解析
        7.2.4 奖励模型训练全景图
        7.2.5 奖励模型的Scaling Law
    7.3 阶段二：多模型联动的PPO训练
        7.3.1 四种模型的角色图解
        7.3.2 各模型的结构、初始化、实践技巧
        7.3.3 各模型的输入、输出
        7.3.4 基于KL散度的策略约束
        7.3.5 基于PPO的RLHF核心实现
        7.3.6 全景图：基于PPO的训练
    7.4 RLHF实践技巧
        7.4.1 奖励欺骗（Reward Hacking）的挑战与应对
        7.4.2 拒绝采样（Rejection Sampling）微调
        7.4.3 强化学习与RLHF的训练框架
        7.4.4 RLHF的超参数
        7.4.5 RLHF的关键监控指标
    7.5 基于AI反馈的强化学习
        7.5.1 RLAIF的原理图解
        7.5.2 CAI：基于宪法的强化学习
        7.5.3 RBR：基于规则的奖励
第8章 逻辑推理能力优化
    8.1 逻辑推理（Reasoning）相关技术概览
        8.1.1 推理时计算与搜索
        8.1.2 基于CoT的蒸馏
        8.1.3 过程奖励模型与结果奖励模型（PRM/ORM）
        8.1.4 数据合成
    8.2 推理路径搜索与优化
        8.2.1 MCTS（蒙特卡洛树搜索）
        8.2.2 A*搜索
        8.2.3 BoN采样与蒸馏
        8.2.4 其他搜索方法
    8.3 强化学习训练
        8.3.1 强化学习的多种应用
        8.3.2 自博弈（Self-Play）与自我进化
        8.3.3 强化学习的多维创新
第9章 综合实践与性能优化
    9.1 实践全景图
    9.2 训练与部署
        9.2.1 数据与环境准备
        9.2.2 超参数如何设置
        9.2.3 SFT训练
        9.2.4 对齐训练：DPO训练、RLHF训练
        9.2.5 推理与部署
    9.3 DeepSeek的训练与本地部署
        9.3.1 DeepSeek的蒸馏与GRPO训练
        9.3.2 DeepSeek的本地部署与使用
    9.4 效果评估
        9.4.1 评估方法分类
        9.4.2 LLM与VLM的评测框架
    9.5 大模型性能优化技术图谱
```

</details>

<br>
<img src="src/assets/Book_Cover.png" alt="Book Cover" width="750">

<br>



### <a name="header-123"></a>参考文献
- 《大模型算法：强化学习、微调与对齐》原书的参考文献详见： [参考文献](./src/references.md) 

---


## 交流讨论
- 本人的 B站 / 知乎 / 公众号 ，均可私信交流。
- 📺**B 站**（叶子哥AI）：[https://space.bilibili.com/3546693609982728](https://space.bilibili.com/3546693609982728)  
- 📘**知乎**（叶子哥AI）：[https://www.zhihu.com/people/yezibro](https://www.zhihu.com/people/yezibro)  
- 💚**公众号**：叶子哥AI  




## 欢迎共建
- 欢迎为本项目提交原理图、文档、纠错与修正或其他任何改进！绘图模板示例：[images-template.pptx](./src/assets/images-template.pptx) 
- 提交步骤：（1）Fork： 点击页面上的"Fork" 按钮，在你的主页创建独立的子仓库 → （2）Clone：将你Fork后的子仓库Clone到本地 → （3）本地新建分支 → （4）修改提交 → （5）Push到远程子仓库 → （6）提交PR：回到Github页面，在你的子仓库界面点击“Compare & pull request”发起PR，等待维护者审核&合并到母仓库。
- 绘图配色以这些颜色为主： <span style="display:inline-block;width:12px;height:12px;background-color:#71CCF5;border-radius:2px;margin-right:8px;"></span>浅蓝（编码`#71CCF5`） ;   <span style="display:inline-block;width:12px;height:12px;background-color:#FFE699;border-radius:2px;margin-right:8px;"></span>浅黄（编码`#FFE699`）; <span style="display:inline-block;width:12px;height:12px;background-color:#C0BFDE;border-radius:2px;margin-right:8px;"></span>蓝紫（编码`#C0BFDE`） ; <span style="display:inline-block;width:12px;height:12px;background-color:#F0ADB7;border-radius:2px;margin-right:8px;"></span> 粉红（编码`#F0ADB7`）。


## 使用条款
本仓库内所有图片均依据 [LICENSE](./LICENSE) 进行授权。只要遵守下方条款，你就可以自由地使用、修改及二次创作这些材料：  
- 分享 —— 你可以复制并以任何媒介或格式重新发布这些材料。  
- 修改 —— 你可以对材料进行混合、转换，并基于其创作衍生作品。

同时，你必须遵守以下条款：  
- **如果用于网络** —— 如果将材料用于帖子、博客等网络内容，请务必保留图片中已包含的原创作者信息。  
- **如果用于论文、书籍等出版物** —— 如果将材料用于论文、书籍等正式出版物，请按照本仓库规定的[引用格式](#引用格式)在参考文献中注明出处；在这种情况下，图片中原有的原创作者信息可以删除。  
- **非商业性使用** —— 你不得将这些材料用于任何直接的商业用途.



## 引用格式

- 如果你在论文、著作或报告中使用了本仓库/本书中的图片等内容，请按以下格式引用：

### <a name="header-124"></a>📌 用于参考文献

- 中文引用格式（推荐）：

```
余昌叶. 大模型算法：强化学习、微调与对齐[M]. 北京: 电子工业出版社, 2025. https://github.com/changyeyu/LLM-RL-Visualized
```

- 英文(English)引用格式：

```
Yu, Changye. Large Model Algorithms: Reinforcement Learning, Fine-Tuning, and Alignment. 
Beijing: Publishing House of Electronics Industry, 2025. https://github.com/changyeyu/LLM-RL-Visualized
```

### <a name="header-125"></a>📌 BibTeX 引用格式

中文 BibTeX（推荐）：

```bibtex
@book{yu2025largemodel,
  title     = {大模型算法：强化学习、微调与对齐},
  author    = {余昌叶},
  publisher = {电子工业出版社},
  year      = {2025},
  address   = {北京},
  isbn      = {9787121500725},
  url       = {https://github.com/changyeyu/LLM-RL-Visualized},
  language  = {zh}
}
```

英文(English) BibTeX：

```bibtex
@book{yu2025largemodel_en,
  title     = {Large Model Algorithms: Reinforcement Learning, Fine-Tuning, and Alignment},
  author    = {Yu, Changye},
  publisher = {Publishing House of Electronics Industry},
  year      = {2025},
  address   = {Beijing},
  isbn      = {9787121500725},
  url       = {https://github.com/changyeyu/LLM-RL-Visualized},
  language  = {en}
}
```

---

<div align="center">
本仓库图片的<strong>文字详解、更多图</strong> 详见：<a href="https://book.douban.com/subject/37331056/">《大模型算法：强化学习、微调与对齐》</a>

欢迎点击仓库顶部的 **Star ⭐**，   谢谢鼓励~
</div>