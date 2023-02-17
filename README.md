# Awesome RLHF (RL with Human Feedback)

This is a collection of research papers for **Reinforcement Learning with Human Feedback**.
And the repository will be continuously updated to track the frontier of RLHF.

Welcome to follow and star!

## Table of Contents

- [Overview of RLHF](#overview-of-rlhf)
- [Papers](#papers)
- [Codebases](#codebases)
- [Blogs](#blogs)
- [Contributing](#contributing)

## Overview of RLHF

The idea of RLHF is to use methods from reinforcement learning to directly optimize a language model with human feedback. RLHF has enabled language models to begin to align a model trained on a general corpus of text data to that of complex human values.

- RLHF for Large Language Model

![image info](./overview_chatgpt.png)

- RLHF for Video Game (e.g. Atari)

![image info](./overview_video_game.png)

## Papers

```
format:
- [title](paper link) [links]
  - author1, author2, and author3...
  - publisher
  - keyword 
  - code 
  - experiment environments and datasets
```

### 2022

- [Is Reinforcement Learning (Not) for Natural Language Processing?: Benchmarks, Baselines, and Building Blocks for Natural Language Policy Optimization](https://arxiv.org/abs/2210.01241) (NLPO)
- [Scaling Laws for Reward Model Overoptimization](https://arxiv.org/abs/2210.10760)
- [Improving alignment of dialogue agents via targeted human judgements](https://arxiv.org/abs/2209.14375) (Sparrow)
- [Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned](https://arxiv.org/abs/2209.07858)
- [Dynamic Planning in Open-Ended Dialogue using Reinforcement Learning](https://arxiv.org/abs/2208.02294)
- [Quark: Controllable Text Generation with Reinforced Unlearning](https://arxiv.org/abs/2205.13636)
- [Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2204.05862)
- [Teaching language models to support answers with verified quotes](https://arxiv.org/abs/2203.11147) (GopherCite)
- [Training language models to follow instructions with human feedback](https://arxiv.org/abs/2203.02155) (InstructGPT)
  - Long Ouyang, Jeff Wu, Xu Jiang, et al.
  - Keyword: Large Language Model, Align Language Model with Human Intent
  - Code: [official](https://github.com/openai/following-instructions-human-feedback)
  - Dataset: [TruthfulQA](https://github.com/sylinrl/TruthfulQA) [RealToxicityPrompts](https://allenai.org/data/real-toxicity-prompts)

### 2021
- [WebGPT: Browser-assisted question-answering with human feedback](https://arxiv.org/abs/2112.09332) (WebGPT)
- [Recursively Summarizing Books with Human Feedback](https://arxiv.org/abs/2109.10862)
- [Revisiting the Weaknesses of Reinforcement Learning for Neural Machine Translation](https://arxiv.org/abs/2106.08942)


### 2020 and before

- [Learning to summarize from human feedback](https://arxiv.org/abs/2009.01325)
- [Fine-Tuning Language Models from Human Preferences](https://arxiv.org/abs/1909.08593)
- [Scalable agent alignment via reward modeling: a research direction](https://arxiv.org/abs/1811.07871)
- [Reward learning from human preferences and demonstrations in Atari](https://arxiv.org/abs/1811.06521)
- [Deep TAMER: Interactive Agent Shaping in High-Dimensional State Spaces](https://arxiv.org/abs/1709.10163)
- [Deep reinforcement learning from human preferences](https://arxiv.org/abs/1706.03741)
- [Interactive Learning from Policy-Dependent Human Feedback](https://arxiv.org/abs/1701.06049)

## Codebases
```
format:
- [title](codebase link) [links]
  - author1, author2, and author3...
  - keyword 
  - experiment environments, datasets or tasks
```

- [PaLM + RLHF - Pytorch](https://github.com/lucidrains/PaLM-rlhf-pytorch)
- [lm-human-preferences](https://github.com/openai/lm-human-preferences)
- [following-instructions-human-feedback](https://github.com/openai/following-instructions-human-feedback)
- [Transformer Reinforcement Learning (TRL)](https://github.com/lvwerra/trl)
  - Leandro von Werra, Younes Belkada, Lewis Tunstall, et al.
  - Keyword: Train LM with RL, PPO, Transformer
  - Task: IMDB sentiment
- [Transformer Reinforcement Learning X (TRLX)](https://github.com/CarperAI/trlx)
- [RL4LMs (A modular RL library to fine-tune language models to human preferences)](https://github.com/allenai/RL4LMs)
- [HH-RLHF](https://github.com/anthropics/hh-rlhf)
- [LaMDA-rlhf-pytorch](https://github.com/conceptofmind/LaMDA-rlhf-pytorch)
- [TextRL](https://github.com/voidful/TextRL)
- [minRLHF](https://github.com/thomfoster/minRLHF)



## Blogs
- [OpenAI] [ChatGPT:Optimizing Language Models for Dialogue](https://openai.com/blog/chatgpt)
- [Hugging Face] [Illustrating Reinforcement Learning from Human Feedback (RLHF)](https://huggingface.co/blog/rlhf)
- [ZhiHu] [通向AGI之路：大型语言模型（LLM）技术精要](https://zhuanlan.zhihu.com/p/597586623)


## Contributing

Our purpose is to make this repo even better. If you are interested in contributing, please refer to [HERE](CONTRIBUTING.md) for instructions in contribution.

## License

Awesome RLHF is released under the Apache 2.0 license.
