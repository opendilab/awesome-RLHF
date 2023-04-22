Türkçe

# Müthiş RLHF (İnsan Geri Bildirimi ile RL)

Bu, **İnsan Geri Bildirimiyle Güçlendirmeli Öğrenim** (RLHF) için araştırma makalelerinin bir derlemesidir.
Ve depo, RLHF sınırını izlemek için sürekli olarak güncellenecektir.

Takip etmeye ve yıldız vermeye hoş geldiniz!


## İçindekiler

- [RLHF'ye Genel Bakış](#overview-of-rlhf)
- [Kağıtlar](#kağıtlar)
- [Kod tabanları](#kod tabanları)
- [Bloglar](#bloglar)
- [Katkıda Bulunan](#katkıda bulunan)

## RLHF'ye Genel Bakış

RLHF fikri, bir dil modelini insan geri bildirimiyle doğrudan optimize etmek için pekiştirmeli öğrenme yöntemlerini kullanmaktır. RLHF, dil modellerinin genel bir metin verileri külliyatı üzerinde eğitilmiş bir modeli karmaşık insan değerlerininkiyle hizalamaya başlamasını sağladı.

- Büyük Dil Modeli (LLM) için RLHF

![image info](./overview_chatgpt.png)

- Video Oyunu için RLHF (ör. Atari)

![image info](./overview_video_game.png)

### Detaylı açıklama

**(Aşağıdaki bölüm ChatGPT tarafından otomatik olarak oluşturulmuştur)**

RLHF tipik olarak "İnsan Geri Bildirimiyle Güçlendirmeli Öğrenme" anlamına gelir. Takviyeli Öğrenim (RL), ortamından gelen geri bildirime dayalı kararlar vermesi için bir aracıyı eğitmeyi içeren bir makine öğrenimi türüdür. RLHF'de aracı ayrıca, daha hızlı ve doğru bir şekilde öğrenmesine yardımcı olabilecek eylemlerinin derecelendirmeleri veya değerlendirmeleri şeklinde insanlardan geri bildirim alır.

RLHF, robotik, oyun ve kişiselleştirilmiş öneri sistemleri gibi alanlardaki uygulamalarıyla yapay zeka alanında aktif bir araştırma alanıdır. Temsilcinin ortamdan gelen geri bildirimlere sınırlı erişiminin olduğu ve performansını iyileştirmek için insan girdisine ihtiyaç duyduğu senaryolarda RL'nin zorluklarını ele almaya çalışır.

İnsan Geri Bildirimiyle Takviyeli Öğrenme (RLHF), yapay zeka alanında hızla gelişen bir araştırma alanıdır ve RLHF sistemlerinin performansını iyileştirmek için geliştirilmiş birkaç gelişmiş teknik vardır. İşte bazı örnekler:

- `Ters Takviyeli Öğrenme (IRL)`: IRL, aracının, önceden tanımlanmış ödül fonksiyonlarına güvenmek yerine insan geribildiriminden bir ödül fonksiyonu öğrenmesini sağlayan bir tekniktir. Bu, aracının, istenen davranışın gösterilmesi gibi daha karmaşık geri bildirim sinyallerinden öğrenmesini mümkün kılar.

- "Çıraklık Eğitimi": Çıraklık öğrenimi, temsilcinin hem insan geri bildiriminden hem de uzman gösterilerinden öğrenmesini sağlamak için IRL'yi denetimli öğrenmeyle birleştiren bir tekniktir. Bu, temsilcinin hem olumlu hem de olumsuz geri bildirimlerden öğrenebildiği için daha hızlı ve etkili bir şekilde öğrenmesine yardımcı olabilir.

- `Etkileşimli Makine Öğrenimi (IML)`: IML, aracı ile insan uzman arasındaki aktif etkileşimi içeren ve uzmanın aracının eylemleri hakkında gerçek zamanlı olarak geri bildirim sağlamasına olanak tanıyan bir tekniktir. Bu, aracının öğrenme sürecinin her adımında eylemleri hakkında geri bildirim alabildiği için daha hızlı ve verimli bir şekilde öğrenmesine yardımcı olabilir.

- `İnsan-in-the-Loop Takviyeli Öğrenim (HITLRL)`: HITLRL, ödül şekillendirme, eylem seçimi ve politika optimizasyonu gibi insan geri bildirimini RL sürecine birden çok düzeyde entegre etmeyi içeren bir tekniktir. Bu, hem insanların hem de makinelerin güçlü yönlerinden yararlanarak RLHF sisteminin verimliliğini ve etkililiğini artırmaya yardımcı olabilir.

İşte İnsan Geri Bildirimi (RLHF) ile Güçlendirmeli Öğrenimden bazı örnekler:

- `Oyun Oynama`: Oyun oynarken, insan geri bildirimi, temsilcinin farklı oyun senaryolarında etkili olan stratejileri ve taktikleri öğrenmesine yardımcı olabilir. Örneğin, popüler Go oyununda insan uzmanlar, temsilciye hareketleriyle ilgili geri bildirimde bulunarak, temsilcinin oynanışını ve karar verme sürecini iyileştirmesine yardımcı olabilir.

- "Kişiselleştirilmiş Öneri Sistemleri": Öneri sistemlerinde, insan geri bildirimi, temsilcinin bireysel kullanıcıların tercihlerini öğrenmesine yardımcı olarak kişiselleştirilmiş öneriler sunmayı mümkün kılar. Örneğin temsilci, hangi özelliklerin onlar için en önemli olduğunu öğrenmek için önerilen ürünlerle ilgili kullanıcılardan gelen geri bildirimleri kullanabilir.

- "Robotik": Robotikte insan geri bildirimi, aracının fiziksel çevreyle güvenli ve verimli bir şekilde nasıl etkileşim kuracağını öğrenmesine yardımcı olabilir. Örneğin, bir robot, bir insan operatörden alınacak en iyi yol veya hangi nesnelerden kaçınılması gerektiği konusunda geri bildirim alarak yeni bir ortamda daha hızlı gezinmeyi öğrenebilir.

- "Eğitim": Eğitimde, insan geri bildirimi aracının öğrencilere nasıl daha etkili bir şekilde öğreteceğini öğrenmesine yardımcı olabilir. Örneğin, yapay zeka tabanlı bir öğretmen, hangi öğretim stratejilerinin farklı öğrencilerle en iyi şekilde çalıştığı konusunda öğretmenlerden gelen geri bildirimleri kullanarak öğrenme deneyimini kişiselleştirmeye yardımcı olabilir.

## Makaleler

```
biçim:
- [başlık](kağıt bağlantı) [bağlantılar]
  - yazar1, yazar2 ve yazar3...
  - Yayımcı
  - anahtar kelime
  - kod
  - deney ortamları ve veri kümeleri
```

### 2023
- [GPT-4 Teknik Raporu](https://cdn.openai.com/papers/gpt-4.pdf)
  - OpenAI
  - Anahtar Kelime: Büyük ölçekli, çok modlu bir model, Trafo tabanlı model, İnce ayarlı kullanılmış RLHF
  - Kod:[official](https://github.com/openai/evals)
   - Dataset: [DROP](https://allenai.org/data/drop), [WinoGrande](https://winogrande.allenai.org/), [HellaSwag](https://rowanzellers.com/hellaswag/), [ARC](https://allenai.org/data/arc), [HumanEval](https://github.com/openai/human-eval), [GSM8K](https://paperswithcode.com/dataset/gsm8k), [MMLU](https://paperswithcode.com/dataset/mmlu), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)

- [RRHF: Dil Modellerini Gözyaşları olmadan İnsan Geri Bildirimiyle Hizalamaya Yanıtları Derecelendirin](https://arxiv.org/pdf/2304.05302v1.pdf)
  - Zheng Yuan, Hongyi Yuan, Chuanqi Tan, Wei Wang, Songfang Huang, Fei Huang
  - Keyword: New paradigm for RLHF
  - Code: [official](https://github.com/GanjinZero/RRHF)

- [İnsan-in-the-Loop RL için Birkaç Adımlık Tercihli Öğrenme](https://openreview.net/pdf?id=IKC5TfXLuW0)
  - Joey Hejna, Dorsa Sadigh
  - Anahtar Kelime: Tercihli Öğrenme, Etkileşimli Öğrenme, Çok Görevli Öğrenme, Döngüdeki insan RL'yi görüntüleyerek mevcut veri havuzunu genişletme
  - Code: [official](https://github.com/jhejna/few-shot-preference-rl)

- [Metinden Görüntüye Modelleri İnsan Tercihiyle Daha İyi Hizalama](https://arxiv.org/abs/2303.14420)
  - Xiaoshi Wu, Keqiang Sun, Feng Zhu, Rui Zhao, Hongsheng Li
  - Anahtar Kelime: Difüzyon Modeli, Metinden Görüntüye, Estetik
  - Code: [official](https://github.com/tgxs002/align_sd)

- [ImageReward: Learning and Evaluating Human Preferences for Text-to-Image Generation](https://arxiv.org/pdf/2304.05977v2.pdf)
  - Jiazheng Xu, Xiao Liu, Yuchen Wu, Yuxuan Tong, Qinkai Li, Ming Ding, Jie Tang, Yuxiao Dong
  - Anahtar Kelime: Genel amaçlı metinden resme insan tercihi RM, Metinden resme Üretken Modellerin Değerlendirilmesi
  - Code: [official](https://github.com/THUDM/ImageReward)
  - Dataset: [COCO](https://cocodataset.org/#home), [DiffusionDB](https://poloclub.github.io/diffusiondb/)

- [Aligning Text-to-Image Models using Human Feedback](https://arxiv.org/pdf/2302.12192.pdf)
  - Kimin Lee, Hao liu, MoonKyung Ryu, Olivia Watkins, Yuqing Du, Craig Boutilier, Pieter Abbeel, Mohammad Ghavamzadeh, Shixiang Shane Gu
  - Keyword: Text-to-Image, Stable diffusion model, Reward function that predicts human feedback

- [Visual ChatGPT: Talking, Drawing and Editing with Visual Foundation Models](https://arxiv.org/pdf/2303.04671.pdf)
  - Chenfei Wu, Shengming Yin, Weizhen Qi, Xiaodong Wang, Zecheng Tang, Nan Duan
  - Keyword: Visual Foundation Models, Visual ChatGPT 
  - Code: [official](https://github.com/microsoft/visual-chatgpt)

- [Pretraining Language Models with Human Preferences](https://arxiv.org/abs/2302.08582) (PHF)
  - Tomasz Korbak, Kejian Shi, Angelica Chen, Rasika Bhalerao, Christopher L. Buckley, Jason Phang, Samuel R. Bowman, Ethan Perez
  - Keyword: Pretraining, offline RL, Decision transformer
  - Code: [official](https://github.com/tomekkorbak/pretraining-with-human-feedback)

- [Aligning Language Models with Preferences through f-divergence Minimization](https://arxiv.org/abs/2302.08215) (f-DPG)
  - Dongyoung Go, Tomasz Korbak, Germán Kruszewski, Jos Rozen, Nahyeon Ryu, Marc Dymetman
  - Keyword: f-divergence, RL with KL penalties

- [Principled Reinforcement Learning with Human Feedback from Pairwise or K-wise Comparisons](https://arxiv.org/pdf/2301.11270.pdf)
  - Banghua Zhu, Jiantao Jiao, Michael I. Jordan
  - Keyword: Pessimistic MLE, Max-entropy IRL

- [The Capacity for Moral Self-Correction in Large Language Models](https://arxiv.org/pdf/2302.07459.pdf)
  - Anthropic
  - Keyword: Improve moral self-correction capability by increasing RLHF training
  - Dataset; [BBQ](https://github.com/nyu-mll/BBQ)

### 2022

- [Is Reinforcement Learning (Not) for Natural Language Processing?: Benchmarks, Baselines, and Building Blocks for Natural Language Policy Optimization](https://arxiv.org/abs/2210.01241) (NLPO)
  - Rajkumar Ramamurthy, Prithviraj Ammanabrolu, Kianté,Brantley, Jack Hessel, Rafet Sifa, Christian Bauckhage, Hannaneh Hajishirzi, Yejin Choi
  - Keyword: Optimizing language generators with RL, Benchmark,  Performant RL algorithm
  - Code: [official](https://github.com/allenai/RL4LMs)
  - Dataset: [IMDB](https://www.imdb.com/interfaces/), [CommonGen](https://inklab.usc.edu/CommonGen/), [CNN Daily Mail](https://github.com/abisee/cnn-dailymail), [ToTTo](https://github.com/google-research-datasets/ToTTo), [WMT-16 (en-de)](https://www.statmt.org/wmt16/it-translation-task.html),[NarrativeQA](https://github.com/deepmind/narrativeqa), [DailyDialog](http://yanran.li/dailydialog)
- [Scaling Laws for Reward Model Overoptimization](https://arxiv.org/abs/2210.10760)
  - Leo Gao, John Schulman, Jacob Hilton
  - Keyword: Gold reward model train proxy reward model, Dataset size, Policy parameter size, BoN, PPO
- [Improving alignment of dialogue agents via targeted human judgements](https://arxiv.org/abs/2209.14375) (Sparrow)
  - Amelia Glaese, Nat McAleese, Maja Trębacz, et al.
  - Keyword: Information-seeking dialogue agent, Break down the good dialogue into natural language rules, DPC, Interact with the model to elicit violation of a specific rule (Adversarial Probing)
  - Dataset: [Natural Questions](https://ai.google.com/research/NaturalQuestions), [ELI5](https://facebookresearch.github.io/ELI5/), [QuALITY](https://github.com/nyu-mll/quality), [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [WinoBias](https://github.com/uclanlp/corefBias/tree/master/WinoBias/wino), [BBQ](https://github.com/nyu-mll/BBQ)
- [Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned](https://arxiv.org/abs/2209.07858)
  - Deep Ganguli, Liane Lovitt, Jackson Kernion, et al.
  - Keyword: Red team language model, Investigate scaling behaviors, Read teaming Dataset
  - Code: [official](https://github.com/anthropics/hh-rlhf)
- [Dynamic Planning in Open-Ended Dialogue using Reinforcement Learning](https://arxiv.org/abs/2208.02294)
  - Deborah Cohen, Moonkyung Ryu, Yinlam Chow, Orgad Keller, Ido Greenberg, Avinatan Hassidim, Michael Fink, Yossi Matias, Idan Szpektor, Craig Boutilier, Gal Elidan
  - Keyword: Real-time, Open-ended dialogue system, Pairs the succinct embedding of the conversation state by language models, CAQL, CQL, [BERT](https://github.com/google-research/bert)
- [Quark: Controllable Text Generation with Reinforced Unlearning](https://arxiv.org/abs/2205.13636)
  - Ximing Lu, Sean Welleck, Jack Hessel, Liwei Jiang, Lianhui Qin, Peter West, Prithviraj Ammanabrolu, Yejin Choi
  - Keyword: Fine-tuning the language model on signals of what not to do, Decision Transformer, LLM tuning with PPO
  - Code: [official](https://github.com/gximinglu/quark)
  - Dataset: [WRITINGPROMPTS](https://www.kaggle.com/datasets/ratthachat/writing-prompts), [SST-2](https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english), [WIKITEXT-103](https://blog.salesforceairesearch.com/the-wikitext-long-term-dependency-language-modeling-dataset/)
- [Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2204.05862)
  - Yuntao Bai, Andy Jones, Kamal Ndousse, et al.
  - Keyword: Harmless assistants, Online mode, Robustness of RLHF training, OOD detection.
  - Code: [official](https://github.com/anthropics/hh-rlhf)
  - Dataset: [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [HellaSwag](https://rowanzellers.com/hellaswag/), [ARC](https://allenai.org/data/arc), [OpenBookQA](https://allenai.org/data/open-book-qa), [LAMBADA](https://zenodo.org/record/2630551#.Y_KLJ-yZNhF), [HumanEval](https://github.com/openai/human-eval), [MMLU](https://github.com/hendrycks/test), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [Teaching language models to support answers with verified quotes](https://arxiv.org/abs/2203.11147) (GopherCite)
  - Jacob Menick, Maja Trebacz, Vladimir Mikulik, John Aslanides, Francis Song, Martin Chadwick, Mia Glaese, Susannah Young, Lucy Campbell-Gillingham, Geoffrey Irving, Nat McAleese
  - Keyword: Generate answers which citing specific evidence, Abstain from answering when unsure
  - Dataset: [Natural Questions](https://ai.google.com/research/NaturalQuestions), [ELI5](https://facebookresearch.github.io/ELI5/), [QuALITY](https://github.com/nyu-mll/quality), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [Training language models to follow instructions with human feedback](https://arxiv.org/abs/2203.02155) (InstructGPT)
  - Long Ouyang, Jeff Wu, Xu Jiang, et al.
  - Keyword: Large Language Model, Align Language Model with Human Intent
  - Code: [official](https://github.com/openai/following-instructions-human-feedback)
  - Dataset: [TruthfulQA](https://github.com/sylinrl/TruthfulQA), [RealToxicityPrompts](https://allenai.org/data/real-toxicity-prompts)
- [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/pdf/2212.08073.pdf)
  - Yuntao Bai, Saurav Kadavath, Sandipan Kundu, Amanda Askell, Jackson Kernion, et al.
  - Keyword: RL from AI feedback(RLAIF), Training a harmless AI assistant through selfimprovement, Chain-of-thought style, Control AI behavior more precisely
  - Code: [official](https://github.com/anthropics/ConstitutionalHarmlessnessPaper)
- [Discovering Language Model Behaviors with Model-Written Evaluations](https://arxiv.org/abs/2212.09251)
  - Ethan Perez, Sam Ringer, Kamilė Lukošiūtė, Karina Nguyen, Edwin Chen, et al.
  - Keyword: Automatically generate evaluations with LMs, More RLHF makes LMs worse, LM-written evaluations are highquality
  - Code: [official](https://github.com/anthropics/evals)
  - Dataset: [BBQ](https://github.com/nyu-mll/BBQ), [Winogender Schemas](https://github.com/rudinger/winogender-schemas)
- [Non-Markovian Reward Modelling from Trajectory Labels via Interpretable Multiple Instance Learning](https://arxiv.org/abs/2205.15367)
  - Joseph Early, Tom Bewley, Christine Evers, Sarvapali Ramchurn
  - Keyword: Reward Modelling (RLHF), Non-Markovian, Multiple Instance Learning, Interpretability
  - Code: [official](https://github.com/JAEarly/MIL-for-Non-Markovian-Reward-Modelling)

### 2021
- [WebGPT: Browser-assisted question-answering with human feedback](https://arxiv.org/abs/2112.09332) (WebGPT)
  - Reiichiro Nakano, Jacob Hilton, Suchir Balaji, et al.
  - Keyword: Model search the web and provide reference， Imitation learning， BC, long form question
  - Dataset: [ELI5](https://facebookresearch.github.io/ELI5/), [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [Recursively Summarizing Books with Human Feedback](https://arxiv.org/abs/2109.10862)
  - Jeff Wu, Long Ouyang, Daniel M. Ziegler, Nisan Stiennon, Ryan Lowe, Jan Leike, Paul Christiano
  - Keyword:  Model trained on small task to assist human evaluate broader task, BC
  - Dataset: [Booksum](https://github.com/salesforce/booksum), [NarrativeQA](https://github.com/deepmind/narrativeqa)
- [Revisiting the Weaknesses of Reinforcement Learning for Neural Machine Translation](https://arxiv.org/abs/2106.08942)
  - Samuel Kiegeland, Julia Kreutzer
  - Keyword:  The success of policy gradient is because of reward rather than the shape of output distribution, Machine Translation, NMT, DOmain Adaption
  - Code: [official](https://github.com/samuki/reinforce-joey)
  - Dataset: [WMT15](https://www.statmt.org/wmt15/index.html), [IWSLT14](https://sites.google.com/site/iwsltevaluation2014/mt-track)

### 2020 and before

- [Learning to summarize from human feedback](https://arxiv.org/abs/2009.01325)
  - Nisan Stiennon, Long Ouyang, Jeff Wu, Daniel M. Ziegler, Ryan Lowe, Chelsea Voss, Alec Radford, Dario Amodei, Paul Christiano
  - Keyword: Care about summary quality, Training loss affect the model behavior, Reward model generalizes to new datasets
  - Code: [official](https://github.com/openai/summarize-from-feedback)
  - Dataset: [TL;DR](https://www.tensorflow.org/datasets/catalog/reddit), [CNN/DM](https://github.com/abisee/cnn-dailymail)
- [Fine-Tuning Language Models from Human Preferences](https://arxiv.org/abs/1909.08593)
  - Daniel M. Ziegler, Nisan Stiennon, Jeffrey Wu, Tom B. Brown, Alec Radford, Dario Amodei, Paul Christiano, Geoffrey Irving
  - Keyword: Reward learning for language, Continuing text with positive sentiment, Summary task, Physical descriptive
  - Code: [official](https://github.com/openai/lm-human-preferences)
  - Dataset: [TL;DR](https://www.tensorflow.org/datasets/catalog/reddit), [CNN/DM](https://github.com/abisee/cnn-dailymail)
- [Scalable agent alignment via reward modeling: a research direction](https://arxiv.org/abs/1811.07871)
  - Jan Leike, David Krueger, Tom Everitt, Miljan Martic, Vishal Maini, Shane Legg
  - Keyword: Agent alignment problem, Learn reward from interaction, Optimize reward with RL, Recursive reward modeling
  - Code: [official](https://github.com/rddy/ReQueST)
  - Env: Atari
- [Reward learning from human preferences and demonstrations in Atari](https://arxiv.org/abs/1811.06521)
  - Borja Ibarz, Jan Leike, Tobias Pohlen, Geoffrey Irving, Shane Legg, Dario Amodei
  - Keyword: Expert demonstration trajectory preferences reward hacking problem, Noise in human label
  - Code: [official](https://github.com/rddy/ReQueST)
  - Env: Atari
- [Deep TAMER: Interactive Agent Shaping in High-Dimensional State Spaces](https://arxiv.org/abs/1709.10163)
  - Garrett Warnell, Nicholas Waytowich, Vernon Lawhern, Peter Stone
  - Keyword:  High dimension state, Leverage the input of Human trainer
  - Code: [third party](https://github.com/bharadwaj1098/Tamer)
  - Env: Atari
- [Deep reinforcement learning from human preferences](https://arxiv.org/abs/1706.03741)
  - Paul Christiano, Jan Leike, Tom B. Brown, Miljan Martic, Shane Legg, Dario Amodei
  - Keyword: Explore goal defined in human preferences between pairs of trajectories segmentation, Learn more complex thing than human feedback
  - Code: [official](https://github.com/mrahtz/learning-from-human-preferences)
  - Env: Atari, MuJoCo
- [Interactive Learning from Policy-Dependent Human Feedback](https://arxiv.org/abs/1701.06049)
  - James MacGlashan, Mark K Ho, Robert Loftin, Bei Peng, Guan Wang, David Roberts, Matthew E. Taylor, Michael L. Littman
  - Keyword: Decision is influenced by current policy rather than human feedback, Learn from policy dependent feedback that converges to a local optimal

## Codebases
```
format:
- [title](codebase link) [links]
  - author1, author2, and author3...
  - keyword
  - experiment environments, datasets or tasks
```

- [PaLM + RLHF - Pytorch](https://github.com/lucidrains/PaLM-rlhf-pytorch)
  - Phil Wang, Yachine Zahidi, Ikko Eltociear Ashimine, Eric Alcaide
  - Keyword: Transformers, PaLM architecture
  - Dataset: [enwik8](http://prize.hutter1.net/)
- [lm-human-preferences](https://github.com/openai/lm-human-preferences)
  - Daniel M. Ziegler, Nisan Stiennon, Jeffrey Wu, Tom B. Brown, Alec Radford, Dario Amodei, Paul Christiano, Geoffrey Irving
  - Keyword: Reward learning for language, Continuing text with positive sentiment, Summary task, Physical  descriptive
  - Dataset: [TL;DR](https://www.tensorflow.org/datasets/catalog/reddit), [CNN/DM](https://github.com/abisee/cnn-dailymail)
- [following-instructions-human-feedback](https://github.com/openai/following-instructions-human-feedback)
  - Long Ouyang, Jeff Wu, Xu Jiang, et al.
  - Keyword: Large Language Model, Align Language Model with Human Intent
  - Dataset: [TruthfulQA](https://github.com/sylinrl/TruthfulQA) [RealToxicityPrompts](https://allenai.org/data/real-toxicity-prompts)
- [Transformer Reinforcement Learning (TRL)](https://github.com/lvwerra/trl)
  - Leandro von Werra, Younes Belkada, Lewis Tunstall, et al.
  - Keyword: Train LLM with RL, PPO, Transformer
  - Task: [IMDB sentiment](https://www.imdb.com/interfaces/)
- [Transformer Reinforcement Learning X (TRLX)](https://github.com/CarperAI/trlx)
  - Jonathan Tow, Leandro von Werra, et al.
  - Keyword: Distributed training framework, T5-based language models, Train LLM with RL, PPO, ILQL
  - Task: Fine tuning LLM with RL using provided reward function or reward-labeled dataset
- [RL4LMs (A modular RL library to fine-tune language models to human preferences)](https://github.com/allenai/RL4LMs)
  - Rajkumar Ramamurthy, Prithviraj Ammanabrolu, Kianté,Brantley, Jack Hessel, Rafet Sifa, Christian Bauckhage, Hannaneh Hajishirzi, Yejin Choi
  - Keyword: Optimizing language generators with RL, Benchmark,  Performant RL algorithm
  - Dataset: [IMDB](https://www.imdb.com/interfaces/), [CommonGen](https://inklab.usc.edu/CommonGen/), [CNN Daily Mail](https://github.com/abisee/cnn-dailymail), [ToTTo](https://github.com/google-research-datasets/ToTTo), [WMT-16 (en-de)](https://www.statmt.org/wmt16/it-translation-task.html), [NarrativeQA](https://github.com/deepmind/narrativeqa), [DailyDialog](http://yanran.li/dailydialog)
- [HH-RLHF](https://github.com/anthropics/hh-rlhf)
  - Ben Mann, Deep Ganguli
  - Keyword: Human preference dataset, Red teaming data, machine-written
  - Task: Open-source dataset for human preference data about helpfulness and harmlessness
- [LaMDA-rlhf-pytorch](https://github.com/conceptofmind/LaMDA-rlhf-pytorch)
  - Phil Wang
  - Keyword: LaMDA, Attention-mechanism
  - Task: Open-source pre-training implementation of Google's LaMDA research paper in PyTorch
- [TextRL](https://github.com/voidful/TextRL)
  - Eric Lam
  - Keyword: huggingface's transformer
  - Task: Text generation
  - Env: PFRL, gym
- [minRLHF](https://github.com/thomfoster/minRLHF)
  - Thomfoster
  - Keyword: PPO, Minimal library
  - Task: educational purposes
- [Stanford Human Preferences Dataset(SHP)](https://huggingface.co/datasets/stanfordnlp/SHP)
  - Ethayarajh, Kawin and Zhang, Heidi and Wang, Yizhong and Jurafsky, Dan
  - Keyword: Naturally occurring and human-written dataset,18 different subject areas
  - Task: Intended to be used for training RLHF reward models 
- [PromptSource](https://github.com/bigscience-workshop/promptsource)
  - Stephen H. Bach, Victor Sanh, Zheng-Xin Yong et al.
  - Keyword: Prompted English datasets,  Mapping a data example into natural language
  - Task:  Toolkit for creating, Sharing and using natural language prompts
- [Structured Knowledge Grounding(SKG) Resources Collections](https://unifiedskg.com/)
  - Tianbao Xie, Chen Henry Wu, Peng Shi et al.
  - Keyword: Structured Knowledge Grounding
  - Task:  Collection of datasets are related to structured knowledge grounding
- [The Flan Collection](https://github.com/google-research/FLAN/tree/main/flan/v2)
  - Longpre Shayne, Hou Le, Vu Tu et al.
  - Task: Collection compiles datasets from Flan 2021, P3, Super-Natural Instructions


## Blogs
- [OpenAI] [ChatGPT: Optimizing Language Models for Dialogue](https://openai.com/blog/chatgpt)
- [Hugging Face] [Illustrating Reinforcement Learning from Human Feedback (RLHF)](https://huggingface.co/blog/rlhf)
- [ZhiHu] [通向AGI之路：大型语言模型 (LLM) 技术精要](https://zhuanlan.zhihu.com/p/597586623)
- [ZhiHu] [大语言模型的涌现能力：现象与解释](https://zhuanlan.zhihu.com/p/621438653)
- [W&B Fully Connected][ Understanding Reinforcement Learning from Human Feedback (RLHF)](https://wandb.ai/ayush-thakur/RLHF/reports/Understanding-Reinforcement-Learning-from-Human-Feedback-RLHF-Part-1--VmlldzoyODk5MTIx)
- [Deepmind] [Learning through human feedback](https://www.deepmind.com/blog/learning-through-human-feedback)
- [Notion] [深入理解语言模型的突现能力](https://yaofu.notion.site/514f4e63918749398a1a8a4c660e0d5b)
- [Notion] [拆解追溯 GPT-3.5 各项能力的起源](https://yaofu.notion.site/GPT-3-5-360081d91ec245f29029d37b54573756#cf00f4e11d974187956122ce7d534386)



## Katkı

Amacımız bu depoyu daha da iyi hale getirmek. Katkıda bulunmakla ilgileniyorsanız, katkıyla ilgili talimatlar için lütfen [BURAYA](CONTRIBUTING.md) bakın.

## Lisans

Müthiş RLHF, Apache 2.0 lisansı altında yayınlandı.







