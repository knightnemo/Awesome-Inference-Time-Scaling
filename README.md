# Awesome-Inference-Time-Scaling
**Paper List of Inference/Test Time Scaling/Computing**

If you think our paper list is helpful, please Star⭐. Thanks! We will continue to update.

<!-- ![Scaling](./fig/Scaling.webp) -->
<p align="center">
    <img src="./fig/Scaling.webp" alt="Scaling" width="400">
</p>

Generated by DALL·E.

## How to Contribute? 

We understand that Inference/Test Time Scaling/Computing is a broad field. If you feel that our list is incomplete, we warmly welcome your contributions.

```
python fetch_semantic_info.py --paper_name "Paper Name"
```
Example:
```
python fetch_semantic_info.py --paper_name "ARMAP"
```

If you find our code useful when you would like to organize your own repo, feel free to use. Also, thanks for the free use of [Semantic Scholar API](https://www.semanticscholar.org/product/api).

## 📖 Paper List (Listed in Time Order)

🔹 [SANA 1.5: Efficient Scaling of Training-Time and Inference-Time Compute in Linear Diffusion Transformer](https://arxiv.org/abs/2501.18427)
- 🔗 **arXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2501.18427)
- 👤 **Authors:** Enze Xie, Junsong Chen, Yuyang Zhao, Jincheng Yu, Ligeng Zhu, Yujun Lin, Zhekai Zhang, Muyang Li, Junyu Chen, Han Cai, Bingchen Liu, Daquan Zhou, Song Han
- 🗓️ **Date:** 2025-01-30
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    This paper presents SANA-1.5, a linear Diffusion Transformer for efficient scaling in text-to-image generation. Building upon SANA-1.0, we introduce three key innovations: (1) Efficient Training Scaling: A depth-growth paradigm that enables scaling from 1.6B to 4.8B parameters with significantly reduced computational resources, combined with a memory-efficient 8-bit optimizer. (2) Model Depth Pruning: A block importance analysis technique for efficient model compression to arbitrary sizes with minimal quality loss. (3) Inference-time Scaling: A repeated sampling strategy that trades computation for model capacity, enabling smaller models to match larger model quality at inference time. Through these strategies, SANA-1.5 achieves a text-image alignment score of 0.72 on GenEval, which can be further improved to 0.80 through inference scaling, establishing a new SoTA on GenEval benchmark. These innovations enable efficient model scaling across different compute budgets while maintaining high quality, making high-quality image generation more accessible.
    </details>


🔹 [CodeMonkeys: Scaling Test-Time Compute for Software Engineering](https://arxiv.org/abs/2501.14723)
- 🔗 **arXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2501.14723)
- 👤 **Authors:** Ryan Ehrlich, Bradley Brown, Jordan Juravsky, Ronald Clark, Christopher R'e, Azalia Mirhoseini
- 🗓️ **Date:** 2025-01-24
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Scaling test-time compute is a promising axis for improving LLM capabilities. However, test-time compute can be scaled in a variety of ways, and effectively combining different approaches remains an active area of research. Here, we explore this problem in the context of solving real-world GitHub issues from the SWE-bench dataset. Our system, named CodeMonkeys, allows models to iteratively edit a codebase by jointly generating and running a testing script alongside their draft edit. We sample many of these multi-turn trajectories for every issue to generate a collection of candidate edits. This approach lets us scale"serial"test-time compute by increasing the number of iterations per trajectory and"parallel"test-time compute by increasing the number of trajectories per problem. With parallel scaling, we can amortize up-front costs across multiple downstream samples, allowing us to identify relevant codebase context using the simple method of letting an LLM read every file. In order to select between candidate edits, we combine voting using model-generated tests with a final multi-turn trajectory dedicated to selection. Overall, CodeMonkeys resolves 57.4% of issues from SWE-bench Verified using a budget of approximately 2300 USD. Our selection method can also be used to combine candidates from different sources. Selecting over an ensemble of edits from existing top SWE-bench Verified submissions obtains a score of 66.2% and outperforms the best member of the ensemble on its own. We fully release our code and data at https://scalingintelligence.stanford.edu/pubs/codemonkeys.
    </details>


🔹 [Inference-Time Scaling for Diffusion Models beyond Scaling Denoising Steps](https://arxiv.org/abs/2501.09732)
- 🔗 **arXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2501.09732)
- 👤 **Authors:** Nanye Ma, Shangyuan Tong, Haolin Jia, Hexiang Hu, Yu-Chuan Su, Mingda Zhang, Xuan Yang, Yandong Li, T. Jaakkola, Xuhui Jia, Saining Xie
- 🗓️ **Date:** 2025-01-16
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Generative models have made significant impacts across various domains, largely due to their ability to scale during training by increasing data, computational resources, and model size, a phenomenon characterized by the scaling laws. Recent research has begun to explore inference-time scaling behavior in Large Language Models (LLMs), revealing how performance can further improve with additional computation during inference. Unlike LLMs, diffusion models inherently possess the flexibility to adjust inference-time computation via the number of denoising steps, although the performance gains typically flatten after a few dozen. In this work, we explore the inference-time scaling behavior of diffusion models beyond increasing denoising steps and investigate how the generation performance can further improve with increased computation. Specifically, we consider a search problem aimed at identifying better noises for the diffusion sampling process. We structure the design space along two axes: the verifiers used to provide feedback, and the algorithms used to find better noise candidates. Through extensive experiments on class-conditioned and text-conditioned image generation benchmarks, our findings reveal that increasing inference-time compute leads to substantial improvements in the quality of samples generated by diffusion models, and with the complicated nature of images, combinations of the components in the framework can be specifically chosen to conform with different application scenario.
    </details>


🔹 [A General Framework for Inference-time Scaling and Steering of Diffusion Models](https://arxiv.org/abs/2501.06848)
- 🔗 **ArXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2501.06848)
- 👤 **Authors:** Raghav Singhal, Zachary Horvitz, Ryan Teehan, Mengye Ren, Zhou Yu, Kathleen McKeown, Rajesh Ranganath
- 🗓️ **Date:** 2025-01-12
- 📑 **Publisher:** ArXiv
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Diffusion models produce impressive results in modalities ranging from images and video to protein design and text. However, generating samples with user-specified properties remains a challenge. Recent research proposes fine-tuning models to maximize rewards that capture desired properties, but these methods require expensive training and are prone to mode collapse. In this work, we propose Feynman Kac (FK) steering, an inference-time framework for steering diffusion models with reward functions. FK steering works by sampling a system of multiple interacting diffusion processes, called particles, and resampling particles at intermediate steps based on scores computed using functions called potentials. Potentials are defined using rewards for intermediate states and are selected such that a high value indicates that the particle will yield a high-reward sample. We explore various choices of potentials, intermediate rewards, and samplers. We evaluate FK steering on text-to-image and text diffusion models. For steering text-to-image models with a human preference reward, we find that FK steering a 0.8B parameter model outperforms a 2.6B parameter fine-tuned model on prompt fidelity, with faster sampling and no training. For steering text diffusion models with rewards for text quality and specific text attributes, we find that FK steering generates lower perplexity, more linguistically acceptable outputs and enables gradient-free control of attributes like toxicity. Our results demonstrate that inference-time scaling and steering of diffusion models, even with off-the-shelf rewards, can provide significant sample quality gains and controllability benefits. Code is available at https://github.com/zacharyhorvitz/Fk-Diffusion-Steering.
    </details>


🔹 [O1 Replication Journey -- Part 3: Inference-time Scaling for Medical Reasoning](https://arxiv.org/abs/2501.06458)
- 🔗 **ArXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2501.06458)
- 👤 **Authors:** Zhongzhen Huang, Gui Geng, Shengyi Hua, Zhen Huang, Haoyang Zou, Shaoting Zhang, Pengfei Liu, Xiaofan Zhang
- 🗓️ **Date:** 2025-01-11
- 📑 **Publisher:** ArXiv
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Building upon our previous investigations of O1 replication (Part 1: Journey Learning [Qin et al., 2024] and Part 2: Distillation [Huang et al., 2024]), this work explores the potential of inference-time scaling in large language models (LLMs) for medical reasoning tasks, ranging from diagnostic decision-making to treatment planning. Through extensive experiments on medical benchmarks of varying complexity (MedQA, Medbullets, and JAMA Clinical Challenges), our investigation reveals several key insights: (1) Increasing inference time does lead to improved performance. With a modest training set of 500 samples, our model yields substantial performance improvements of 6%-11%. (2) Task complexity directly correlates with the required length of reasoning chains, confirming the necessity of extended thought processes for challenging problems. (3) The differential diagnoses generated by our model adhere to the principles of the hypothetico-deductive method, producing a list of potential conditions that may explain a patient's symptoms and systematically narrowing these possibilities by evaluating the evidence. These findings demonstrate the promising synergy between inference-time scaling and journey learning in advancing LLMs' real-world clinical reasoning capabilities.
    </details>


🔹 [Agent Q: Advanced Reasoning and Learning for Autonomous AI Agents](https://arxiv.org/abs/2408.07199)
- 🔗 **arXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2408.07199)
- 👤 **Authors:** Pranav Putta, Edmund Mills, Naman Garg, S. Motwani, Chelsea Finn, Divyansh Garg, Rafael Rafailov
- 🗓️ **Date:** 2024-08-13
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Large Language Models (LLMs) have shown remarkable capabilities in natural language tasks requiring complex reasoning, yet their application in agentic, multi-step reasoning within interactive environments remains a difficult challenge. Traditional supervised pre-training on static datasets falls short in enabling autonomous agent capabilities needed to perform complex decision-making in dynamic settings like web navigation. Previous attempts to bridge this ga-through supervised fine-tuning on curated expert demonstrations-often suffer from compounding errors and limited exploration data, resulting in sub-optimal policy outcomes. To overcome these challenges, we propose a framework that combines guided Monte Carlo Tree Search (MCTS) search with a self-critique mechanism and iterative fine-tuning on agent interactions using an off-policy variant of the Direct Preference Optimization (DPO) algorithm. Our method allows LLM agents to learn effectively from both successful and unsuccessful trajectories, thereby improving their generalization in complex, multi-step reasoning tasks. We validate our approach in the WebShop environment-a simulated e-commerce platform where it consistently outperforms behavior cloning and reinforced fine-tuning baseline, and beats average human performance when equipped with the capability to do online search. In real-world booking scenarios, our methodology boosts Llama-3 70B model's zero-shot performance from 18.6% to 81.7% success rate (a 340% relative increase) after a single day of data collection and further to 95.4% with online search. We believe this represents a substantial leap forward in the capabilities of autonomous agents, paving the way for more sophisticated and reliable decision-making in real-world settings.
    </details>

🔹 [Scaling LLM Test-Time Compute Optimally can be More Effective than Scaling Model Parameters](https://arxiv.org/abs/2408.03314)
- 🔗 **arXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2408.03314)
- 👤 **Authors:** Charlie Snell, Jaehoon Lee, Kelvin Xu, Aviral Kumar
- 🗓️ **Date:** 2024-08-06
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Enabling LLMs to improve their outputs by using more test-time computation is a critical step towards building generally self-improving agents that can operate on open-ended natural language. In this paper, we study the scaling of inference-time computation in LLMs, with a focus on answering the question: if an LLM is allowed to use a fixed but non-trivial amount of inference-time compute, how much can it improve its performance on a challenging prompt? Answering this question has implications not only on the achievable performance of LLMs, but also on the future of LLM pretraining and how one should tradeoff inference-time and pre-training compute. Despite its importance, little research attempted to understand the scaling behaviors of various test-time inference methods. Moreover, current work largely provides negative results for a number of these strategies. In this work, we analyze two primary mechanisms to scale test-time computation: (1) searching against dense, process-based verifier reward models; and (2) updating the model's distribution over a response adaptively, given the prompt at test time. We find that in both cases, the effectiveness of different approaches to scaling test-time compute critically varies depending on the difficulty of the prompt. This observation motivates applying a"compute-optimal"scaling strategy, which acts to most effectively allocate test-time compute adaptively per prompt. Using this compute-optimal strategy, we can improve the efficiency of test-time compute scaling by more than 4x compared to a best-of-N baseline. Additionally, in a FLOPs-matched evaluation, we find that on problems where a smaller base model attains somewhat non-trivial success rates, test-time compute can be used to outperform a 14x larger model.
    </details>


🔹 [Inference Scaling Laws: An Empirical Analysis of Compute-Optimal Inference for Problem-Solving with Language Models](https://arxiv.org/abs/2408.00724)
- 🔗 **ArXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2408.00724)
- 👤 **Authors:** Yangzhen Wu, Zhiqing Sun, Shanda Li, S. Welleck, Yiming Yang
- 🗓️ **Date:** 2024-08-01
- 📑 **Publisher:** ArXiv
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    While the scaling laws of large language models (LLMs) training have been extensively studied, optimal inference configurations of LLMs remain underexplored. We study inference scaling laws and compute-optimal inference, focusing on the trade-offs between model sizes and generating additional tokens with different inference strategies. As a first step towards understanding and designing compute-optimal inference methods, we studied cost-performance trade-offs for inference strategies such as greedy search, majority voting, best-of-$n$, weighted voting, and two different tree search algorithms, using different model sizes and compute budgets. Our findings indicate smaller models (e.g., Llemma-7B) can outperform larger models given the same computation budgets, and that smaller models paired with advanced inference algorithms yield Pareto-optimal cost-performance trade-offs. For instance, the Llemma-7B model, equipped with our novel tree search algorithm, consistently outperforms Llemma-34B with standard majority voting on the MATH benchmark across all FLOPs budgets. We hope these findings contribute to a broader understanding of inference scaling laws for LLMs.
    </details>


🔹 [Large Language Monkeys: Scaling Inference Compute with Repeated Sampling](https://arxiv.org/abs/2407.21787)
- 🔗 **ArXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2407.21787)
- 👤 **Authors:** Bradley Brown, Jordan Juravsky, Ryan Ehrlich, Ronald Clark, Quoc V. Le, Christopher R'e, Azalia Mirhoseini
- 🗓️ **Date:** 2024-07-31
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Scaling the amount of compute used to train language models has dramatically improved their capabilities. However, when it comes to inference, we often limit models to making only one attempt at a problem. Here, we explore inference compute as another axis for scaling, using the simple technique of repeatedly sampling candidate solutions from a model. Across multiple tasks and models, we observe that coverage -- the fraction of problems that are solved by any generated sample -- scales with the number of samples over four orders of magnitude. Interestingly, the relationship between coverage and the number of samples is often log-linear and can be modelled with an exponentiated power law, suggesting the existence of inference-time scaling laws. In domains like coding and formal proofs, where answers can be automatically verified, these increases in coverage directly translate into improved performance. When we apply repeated sampling to SWE-bench Lite, the fraction of issues solved with DeepSeek-Coder-V2-Instruct increases from 15.9% with one sample to 56% with 250 samples, outperforming the single-sample state-of-the-art of 43%. In domains without automatic verifiers, we find that common methods for picking from a sample collection (majority voting and reward models) plateau beyond several hundred samples and fail to fully scale with the sample budget.
    </details>


🔹 [Tree Search for Language Model Agents](https://arxiv.org/abs/2407.01476)
- 🔗 **arXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2407.01476)
- 👤 **Authors:** Jing Yu Koh, Stephen McAleer, Daniel Fried, Ruslan Salakhutdinov
- 🗓️ **Date:** 2024-07-01
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    Autonomous agents powered by language models (LMs) have demonstrated promise in their ability to perform decision-making tasks such as web automation. However, a key limitation remains: LMs, primarily optimized for natural language understanding and generation, struggle with multi-step reasoning, planning, and using environmental feedback when attempting to solve realistic computer tasks. Towards addressing this, we propose an inference-time search algorithm for LM agents to explicitly perform exploration and multi-step planning in interactive web environments. Our approach is a form of best-first tree search that operates within the actual environment space, and is complementary with most existing state-of-the-art agents. It is the first tree search algorithm for LM agents that shows effectiveness on realistic web tasks. On the challenging VisualWebArena benchmark, applying our search algorithm on top of a GPT-4o agent yields a 39.7% relative increase in success rate compared to the same baseline without search, setting a state-of-the-art success rate of 26.4%. On WebArena, search also yields a 28.0% relative improvement over a baseline agent, setting a competitive success rate of 19.2%. Our experiments highlight the effectiveness of search for web agents, and we demonstrate that performance scales with increased test-time compute. We conduct a thorough analysis of our results to highlight improvements from search, limitations, and promising directions for future work. Our code and models are publicly released at https://jykoh.com/search-agents.
    </details>


🔹 [From Decoding to Meta-Generation: Inference-time Algorithms for Large Language Models](https://arxiv.org/abs/2406.16838)
- 🔗 **ArXiv PDF Link:** [Paper Link](https://arxiv.org/pdf/2406.16838)
- 👤 **Authors:** S. Welleck, Amanda Bertsch, Matthew Finlayson, Hailey Schoelkopf, Alex Xie, Graham Neubig, Ilia Kulikov, Zaid Harchaoui
- 🗓️ **Date:** 2024-06-24
- 📑 **Publisher:** arXiv.org
- 📝 **Abstract:** 
    <details>
    <summary>Expand</summary>
    One of the most striking findings in modern research on large language models (LLMs) is that scaling up compute during training leads to better results. However, less attention has been given to the benefits of scaling compute during inference. This survey focuses on these inference-time approaches. We explore three areas under a unified mathematical formalism: token-level generation algorithms, meta-generation algorithms, and efficient generation. Token-level generation algorithms, often called decoding algorithms, operate by sampling a single token at a time or constructing a token-level search space and then selecting an output. These methods typically assume access to a language model's logits, next-token distributions, or probability scores. Meta-generation algorithms work on partial or full sequences, incorporating domain knowledge, enabling backtracking, and integrating external information. Efficient generation methods aim to reduce token costs and improve the speed of generation. Our survey unifies perspectives from three research communities: traditional natural language processing, modern LLMs, and machine learning systems.
    </details>








