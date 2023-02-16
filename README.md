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

- [Training language models to follow instructions with human feedback](https://arxiv.org/abs/2203.02155) (InstructGPT)
  - Long Ouyang, Jeff Wu, Xu Jiang, et al
  - Keyword: GPT-3, LM alignment

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
- [Transformer Reinforcement Learning (TRL)](https://github.com/lvwerra/trl)
  - Leandro von Werra, Younes Belkada, Lewis Tunstall, et al
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
