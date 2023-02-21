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
  - Rajkumar Ramamurthy, Prithviraj Ammanabrolu, Kianté,Brantley, Jack Hessel, Rafet Sifa, Christian Bauckhage, Hannaneh Hajishirzi, Yejin Choi 
  - Keyword: Optimizing language generators with RL, Benchmark,  Performant RL algorithm
  - Code: [official](https://github.com/allenai/RL4LMs) 
  - Dataset: [IMDB](https://www.imdb.com/interfaces/), [CommonGen](https://inklab.usc.edu/CommonGen/), [CNN Daily Mail](https://github.com/abisee/cnn-dailymail), [ToTTo](https://github.com/google-research-datasets/ToTTo), [WMT-16 (en-de)](https://www.statmt.org/wmt16/it-translation-task.html),[NarrativeQA](https://github.com/deepmind/narrativeqa), [DailyDialog](http://yanran.li/dailydialog) 
- [Scaling Laws for Reward Model Overoptimization](https://arxiv.org/abs/2210.10760)
  - Leo Gao, John Schulman, Jacob Hilton
  - Keyword: Gold reward model train proxy reward model, Dataset size, Policy parameter size, BoN, PPO
  - Code: None
  - Dataset: None
- [Improving alignment of dialogue agents via targeted human judgements](https://arxiv.org/abs/2209.14375) (Sparrow)
  - Amelia Glaese, Nat McAleese, Maja Trębacz, et al.
  - Keyword: Information-seeking dialogue agent, Break down the good dialogue into natural language rules , DPC, Interact with the model to elicit violation of a specific rule(Adversarial Probing)
  - Code: None
  - Dataset: [Natural Questions](https://ai.google.com/research/NaturalQuestions), [ELI5](https://facebookresearch.github.io/ELI5/), [QuALITY](https://github.com/nyu-mll/quality), [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [WinoBias](https://github.com/uclanlp/corefBias/tree/master/WinoBias/wino), [BBQ](https://github.com/nyu-mll/BBQ)
- [Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned](https://arxiv.org/abs/2209.07858)
  - Deep Ganguli, Liane Lovitt, Jackson Kernion, et al.
  - Keyword: Red team language model, Investigate scaling behaviors, Read teaming Dataset
  - Code: [Official](https://github.com/anthropics/hh-rlhf)
  - Dataset: none
- [Dynamic Planning in Open-Ended Dialogue using Reinforcement Learning](https://arxiv.org/abs/2208.02294)
  - Deborah Cohen, Moonkyung Ryu, Yinlam Chow, Orgad Keller, Ido Greenberg, Avinatan Hassidim, Michael Fink, Yossi Matias, Idan Szpektor, Craig Boutilier, Gal Elidan
  - Keyword: Real-time, Open-ended dialogue system, Pairs the succinct embedding of the conversation state by language models, CAQL,CQL, [BERT](https://github.com/google-research/bert)
  - Code: None
  - Dataset: None
- [Quark: Controllable Text Generation with Reinforced Unlearning](https://arxiv.org/abs/2205.13636)
  - Ximing Lu, Sean Welleck, Jack Hessel, Liwei Jiang, Lianhui Qin, Peter West, Prithviraj Ammanabrolu, Yejin Choi
  - Keyword: Fine-tuning the language model on signals of what not to do, Decision Transformer, LM tuning with PPO
  - Code: [official](https://github.com/gximinglu/quark)
  - Dataset: [WRITINGPROMPTS](https://www.kaggle.com/datasets/ratthachat/writing-prompts), [SST-2](https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english), [WIKITEXT-103](https://blog.salesforceairesearch.com/the-wikitext-long-term-dependency-language-modeling-dataset/)
- [Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2204.05862)
  - Yuntao Bai, Andy Jones, Kamal Ndousse, et al.
  - Keyword: Harmless assistants, Online mode, Robustness of RLHF training, OOD detection.
  - Code: [Official](https://github.com/anthropics/hh-rlhf)
  - Dataset: [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [HellaSwag](https://rowanzellers.com/hellaswag/), [ARC](https://allenai.org/data/arc), [OpenBookQA](https://allenai.org/data/open-book-qa), [LAMBADA](https://zenodo.org/record/2630551#.Y_KLJ-yZNhF), [HumanEval](https://github.com/openai/human-eval), [MMLU](https://github.com/hendrycks/test), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [Teaching language models to support answers with verified quotes](https://arxiv.org/abs/2203.11147) (GopherCite)
  - Jacob Menick, Maja Trebacz, Vladimir Mikulik, John Aslanides, Francis Song, Martin Chadwick, Mia Glaese, Susannah Young, Lucy Campbell-Gillingham, Geoffrey Irving, Nat McAleese
  - Keyword: Generate answers which citing specific evidence, Abstain from answering when unsure
  - Code: None
  - Dataset: [Natural Questions](https://ai.google.com/research/NaturalQuestions), [ELI5](https://facebookresearch.github.io/ELI5/), [QuALITY](https://github.com/nyu-mll/quality), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [Training language models to follow instructions with human feedback](https://arxiv.org/abs/2203.02155) (InstructGPT)
  - Long Ouyang, Jeff Wu, Xu Jiang, et al.
  - Keyword: Large Language Model, Align Language Model with Human Intent
  - Code: [official](https://github.com/openai/following-instructions-human-feedback)
  - Dataset: [TruthfulQA](https://github.com/sylinrl/TruthfulQA) [RealToxicityPrompts](https://allenai.org/data/real-toxicity-prompts)

### 2021
- [WebGPT: Browser-assisted question-answering with human feedback](https://arxiv.org/abs/2112.09332) (WebGPT)
  - Reiichiro Nakano, Jacob Hilton, Suchir Balaji, et al.
  - Keyword: Model search the web and provide reference， Imitation learning， BC, long form question
  - Code: None
  - Dataset: [ELI5](https://facebookresearch.github.io/ELI5/)，[TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [Recursively Summarizing Books with Human Feedback](https://arxiv.org/abs/2109.10862)
  - Jeff Wu, Long Ouyang, Daniel M. Ziegler, Nisan Stiennon, Ryan Lowe, Jan Leike, Paul Christiano
  - Keyword:  Model trained on small task to assist human evaluate broader task, BC
  - Code: None
  - Dataset: [Booksum](https://github.com/salesforce/booksum), [NarrativeQA](https://github.com/deepmind/narrativeqa)
- [Revisiting the Weaknesses of Reinforcement Learning for Neural Machine Translation](https://arxiv.org/abs/2106.08942)
  - Samuel Kiegeland, Julia Kreutzer
  - Keyword:  the success of policy gradient is because of reward rather than the shape of output distribution, Machine Translation, NMT, DOmain Adaption
  - Code: [official](https://github.com/samuki/reinforce-joey)
  - Dataset: [WMT15](https://www.statmt.org/wmt15/index.html), [IWSLT14](https://sites.google.com/site/iwsltevaluation2014/mt-track)


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
- [W&B Fully Connected][ Understanding Reinforcement Learning from Human Feedback (RLHF)](https://wandb.ai/ayush-thakur/RLHF/reports/Understanding-Reinforcement-Learning-from-Human-Feedback-RLHF-Part-1--VmlldzoyODk5MTIx)
- [Deepmind][Learning through human feedback](https://www.deepmind.com/blog/learning-through-human-feedback)




## Contributing

Our purpose is to make this repo even better. If you are interested in contributing, please refer to [HERE](CONTRIBUTING.md) for instructions in contribution.

## License

Awesome RLHF is released under the Apache 2.0 license.
