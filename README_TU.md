LANGUAGE TURKISH
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

- [RAFT: Reward rAnked FineTuning for Generative Foundation Model Alignment](https://arxiv.org/pdf/2304.06767.pdf)
  - Hanze Dong, Wei Xiong, Deepanshu Goyal, Rui Pan, Shizhe Diao, Jipeng Zhang, Kashun Shum, Tong Zhang
  - Keyword: Alternative to PPO, ChatGPT, Diffusion Model
  - Code: [official](https://github.com/OptimalScale/LMFlow)
  
- [RRHF: Rank Responses to Align Language Models with Human Feedback without tears](https://arxiv.org/pdf/2304.05302v1.pdf)
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

- [ImageReward: Metinden Görüntüye Üretim için İnsan Tercihlerini Öğrenmek ve Değerlendirmek](https://arxiv.org/pdf/2304.05977v2.pdf)
  - Jiazheng Xu, Xiao Liu, Yuchen Wu, Yuxuan Tong, Qinkai Li, Ming Ding, Jie Tang, Yuxiao Dong
  - Anahtar Kelime: Genel amaçlı metinden resme insan tercihi RM, Metinden resme Üretken Modellerin Değerlendirilmesi
  - Code: [official](https://github.com/THUDM/ImageReward)
  - Dataset: [COCO](https://cocodataset.org/#home), [DiffusionDB](https://poloclub.github.io/diffusiondb/)

- [Aligning İnsan Geri Bildirimini Kullanan Metinden Görüntüye Modeller](https://arxiv.org/pdf/2302.12192.pdf)
  - Kimin Lee, Hao liu, MoonKyung Ryu, Olivia Watkins, Yuqing Du, Craig Boutilier, Pieter Abbeel, Mohammad Ghavamzadeh, Shixiang Shane Gu
  - Anahtar Kelime: Metinden Görüntüye, Kararlı yayılma modeli, İnsan geri bildirimini tahmin eden Ödül işlevi

- [Visual ChatGPT: Visual Foundation Modelleri ile Konuşma, Çizim ve Düzenleme](https://arxiv.org/pdf/2303.04671.pdf)
  - Chenfei Wu, Shengming Yin, Weizhen Qi, Xiaodong Wang, Zecheng Tang, Nan Duan
  - Anahtar Kelime: Visual Foundation Modelleri, Visual ChatGPT
  - Code: [official](https://github.com/microsoft/visual-chatgpt)

- [İnsan Tercihleriyle Ön Eğitim Dil Modelleri](https://arxiv.org/abs/2302.08582) (PHF)
  - Tomasz Korbak, Kejian Shi, Angelica Chen, Rasika Bhalerao, Christopher L. Buckley, Jason Phang, Samuel R. Bowman, Ethan Perez
  - Anahtar Kelime: Ön eğitim, çevrimdışı RL, Karar dönüştürücü
  - Code: [official](https://github.com/tomekkorbak/pretraining-with-human-feedback)

- [f-diverjans Minimizasyonu yoluyla Dil Modellerini Tercihlerle Hizalama](https://arxiv.org/abs/2302.08215) (f-DPG)
  - Dongyoung Go, Tomasz Korbak, Germán Kruszewski, Jos Rozen, Nahyeon Ryu, Marc Dymetman
  - Anahtar kelime: f-diverjans, KL cezalı RL

- [Principled Reinforcement Learning with Human Feedback from Pairwise or K-wise Comparisons](https://arxiv.org/pdf/2301.11270.pdf)
  - Banghua Zhu, Jiantao Jiao, Michael I. Jordan
  - Anahtar Kelime: Kötümser MLE, Maks-entropi IRL

- [Büyük Dil Modellerinde Ahlaki Kendini Düzeltme Kapasitesi](https://arxiv.org/pdf/2302.07459.pdf)
  - Anthropic
  - Anahtar Kelime: RLHF eğitimini artırarak ahlaki kendi kendini düzeltme yeteneğini geliştirin
  - Dataset; [BBQ](https://github.com/nyu-mll/BBQ)

### 2022

- [Takviyeli Öğrenim Doğal Dil İşleme İçin mi (Değil) mi?: Doğal Dil Politikası Optimizasyonu için Karşılaştırmalar, Temel Çizgiler ve Yapı Taşları](https://arxiv.org/abs/2210.01241) (NLPO)
  - Rajkumar Ramamurthy, Prithviraj Ammanabrolu, Kianté,Brantley, Jack Hessel, Rafet Sifa, Christian Bauckhage, Hannaneh Hajishirzi, Yejin Choi
  - Anahtar Kelime: RL, Benchmark, Performant RL algoritması ile dil oluşturucuları optimize etme
  - Code: [official](https://github.com/allenai/RL4LMs)
  - Dataset: [IMDB](https://www.imdb.com/interfaces/), [CommonGen](https://inklab.usc.edu/CommonGen/), [CNN Daily Mail](https://github.com/abisee/cnn-dailymail), [ToTTo](https://github.com/google-research-datasets/ToTTo), [WMT-16 (en-de)](https://www.statmt.org/wmt16/it-translation-task.html),[NarrativeQA](https://github.com/deepmind/narrativeqa), [DailyDialog](http://yanran.li/dailydialog)
- [Scaling Laws for Reward Model Overoptimization](https://arxiv.org/abs/2210.10760)
  - Leo Gao, John Schulman, Jacob Hilton
  - Anahtar Kelime: Altın ödül modeli tren proxy ödül modeli, Veri kümesi boyutu, Politika parametre boyutu, BoN, PPO
- [Hedeflenen insan yargıları yoluyla diyalog aracılarının uyumunun iyileştirilmesi](https://arxiv.org/abs/2209.14375) (Sparrow)
  - Amelia Glaese, Nat McAleese, Maja Trębacz, et al.
  - Anahtar Sözcük: Bilgi arayan diyalog aracısı, İyi diyaloğu doğal dil kurallarına bölün, DPC, Belirli bir kuralın ihlalini ortaya çıkarmak için modelle etkileşim kurun (Düşmanlı Araştırma)
  - Dataset: [Doğal Sorular](https://ai.google.com/research/NaturalQuestions), [ELI5](https://facebookresearch.github.io/ELI5/), [QuALITY](https://github.com/nyu-mll/quality), [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [WinoBias](https://github.com/uclanlp/corefBias/tree/master/WinoBias/wino), [BBQ](https://github.com/nyu-mll/BBQ)
- [Zararları Azaltmak için Red Teaming Dil Modelleri: Yöntemler, Davranışları Ölçeklendirme ve Alınan Dersler](https://arxiv.org/abs/2209.07858)
  - Deep Ganguli, Liane Lovitt, Jackson Kernion, et al.
  - Anahtar Kelime: Red team dil modeli, Ölçekleme davranışlarını araştırma, Teaming Dataset'i okuma
  - Code: [official](https://github.com/anthropics/hh-rlhf)
- [Takviyeli Öğrenimi Kullanarak Açık Uçlu Diyalogda Dinamik Planlama](https://arxiv.org/abs/2208.02294)
  - Deborah Cohen, Moonkyung Ryu, Yinlam Chow, Orgad Keller, Ido Greenberg, Avinatan Hassidim, Michael Fink, Yossi Matias, Idan Szpektor, Craig Boutilier, Gal Elidan
  - Anahtar Kelime: Gerçek zamanlı, Açık uçlu diyalog sistemi, Konuşma durumunun özlü yerleşimini dil modellerine göre eşleştirir, CAQL, CQL, [BERT]
  - (https://github.com/google-research/bert)
- [Quark: Güçlendirilmiş Unlearning ile Kontrol Edilebilir Metin Oluşturma](https://arxiv.org/abs/2205.13636)
  - Ximing Lu, Sean Welleck, Jack Hessel, Liwei Jiang, Lianhui Qin, Peter West, Prithviraj Ammanabrolu, Yejin Choi
  - Anahtar Kelime: Ne yapılmaması gerektiğine dair sinyaller üzerinde dil modelinin ince ayarı, Decision Transformer, PPO ile LLM ayarı
  - Code: [official](https://github.com/gximinglu/quark)
  - Dataset: [WRITINGPROMPTS](https://www.kaggle.com/datasets/ratthachat/writing-prompts), [SST-2](https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english), [WIKITEXT-103](https://blog.salesforceairesearch.com/the-wikitext-long-term-dependency-language-modeling-dataset/)
- [İnsan Geribildiriminden Güçlendirilmiş Öğrenim ile Yararlı ve Zararsız Bir Asistan Yetiştirmek](https://arxiv.org/abs/2204.05862)
  - Yuntao Bai, Andy Jones, Kamal Ndousse, et al.
  - Anahtar Kelime: Zararsız asistanlar, Çevrimiçi mod, RLHF eğitiminin sağlamlığı, OOD tespiti.
  - Code: [official](https://github.com/anthropics/hh-rlhf)
  - Dataset: [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [HellaSwag](https://rowanzellers.com/hellaswag/), [ARC](https://allenai.org/data/arc), [OpenBookQA](https://allenai.org/data/open-book-qa), [LAMBADA](https://zenodo.org/record/2630551#.Y_KLJ-yZNhF), [HumanEval](https://github.com/openai/human-eval), [MMLU](https://github.com/hendrycks/test), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [Doğrulanmış alıntılarla yanıtları desteklemek için dil modellerini öğretmek](https://arxiv.org/abs/2203.11147) (GopherCite)
  - Jacob Menick, Maja Trebacz, Vladimir Mikulik, John Aslanides, Francis Song, Martin Chadwick, Mia Glaese, Susannah Young, Lucy Campbell-Gillingham, Geoffrey Irving, Nat McAleese
  - Keyword: Generate answers which citing specific evidence, Abstain from answering when unsure
  - Dataset: [Natural Questions](https://ai.google.com/research/NaturalQuestions), [ELI5](https://facebookresearch.github.io/ELI5/), [QuALITY](https://github.com/nyu-mll/quality), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [İnsan geri bildirimi ile talimatları takip etmek için eğitim dil modelleri](https://arxiv.org/abs/2203.02155) (InstructGPT)
  - Long Ouyang, Jeff Wu, Xu Jiang, et al.
  - Anahtar Kelime: Büyük Dil Modeli, Dil Modelini İnsan Niyetiyle Hizala
  - Code: [official](https://github.com/openai/following-instructions-human-feedback)
  - Dataset: [TruthfulQA](https://github.com/sylinrl/TruthfulQA), [RealToxicityPrompts](https://allenai.org/data/real-toxicity-prompts)
- [Yapısal Yapay Zeka: Yapay Zeka Geri Bildiriminden Zararsızlık](https://arxiv.org/pdf/2212.08073.pdf)
  - Yuntao Bai, Saurav Kadavath, Sandipan Kundu, Amanda Askell, Jackson Kernion, et al.
  - Keyword: RL from AI feedback(RLAIF), Training a harmless AI assistant through selfimprovement, Chain-of-thought style, Control AI behavior more precisely
  - Code: [official](https://github.com/anthropics/ConstitutionalHarmlessnessPaper)
-[](https://arxiv.org/abs/2212.09251)
  - Ethan Perez, Sam Ringer, Kamilė Lukošiūtė, Karina Nguyen, Edwin Chen, et al.
  - Anahtar Kelime: LM'lerle otomatik olarak değerlendirmeler oluşturun, Daha Fazla RLHF, LM'leri daha kötü hale getirir, LM'de yazılan değerlendirmeler yüksek kalitededir
  - Code: [official](https://github.com/anthropics/evals)
  - Dataset: [BBQ](https://github.com/nyu-mll/BBQ), [Winogender Schemas](https://github.com/rudinger/winogender-schemas)
- [Yorumlanabilir Çoklu Örnek Öğrenme Yoluyla Yörünge Etiketlerinden Markoviyen Olmayan Ödül Modellemesi](https://arxiv.org/abs/2205.15367)
  - Joseph Early, Tom Bewley, Christine Evers, Sarvapali Ramchurn
  - Anahtar Kelime: Ödül Modelleme (RLHF), Non-Markovian, Çoklu Örnek Öğrenme, Yorumlanabilirlik
  - Code: [official](https://github.com/JAEarly/MIL-for-Non-Markovian-Reward-Modelling)

### 2021
- [WebGPT: İnsan geri bildirimiyle tarayıcı destekli soru yanıtlama](https://arxiv.org/abs/2112.09332) (WebGPT)
  - Reiichiro Nakano, Jacob Hilton, Suchir Balaji, et al.
  - Anahtar Kelime: Web'de model araması yapın ve referans sağlayın， Taklit öğrenme， BC, uzun biçimli soru
  - Dataset: [ELI5](https://facebookresearch.github.io/ELI5/), [TriviaQA](http://nlp.cs.washington.edu/triviaqa/), [TruthfulQA](https://github.com/sylinrl/TruthfulQA)
- [İnsan Geri Bildirimiyle Kitapları Yinelemeli Olarak Özetleme](https://arxiv.org/abs/2109.10862)
  - Jeff Wu, Long Ouyang, Daniel M. Ziegler, Nisan Stiennon, Ryan Lowe, Jan Leike, Paul Christiano
  - Anahtar Kelime: İnsanların daha geniş görevleri değerlendirmesine yardımcı olmak için küçük görevlerde eğitilmiş model, BC
  - Dataset: [Booksum](https://github.com/salesforce/booksum), [NarrativeQA](https://github.com/deepmind/narrativeqa)
- [Nöral Makine Çevirisi için Takviyeli Öğrenmenin Zayıf Yönlerini Yeniden İncelemek](https://arxiv.org/abs/2106.08942)
  - Samuel Kiegeland, Julia Kreutzer
  - Anahtar Kelime: Politika gradyanının başarısı, çıktı dağılımının şeklinden çok ödülden kaynaklanır, Makine Çevirisi, NMT, DOmain Uyarlaması
  - Code: [official](https://github.com/samuki/reinforce-joey)
  - Dataset: [WMT15](https://www.statmt.org/wmt15/index.html), [IWSLT14](https://sites.google.com/site/iwsltevaluation2014/mt-track)

### 2020 and Öncesi

- [İnsan geri bildirimlerinden özetlemeyi öğrenmek](https://arxiv.org/abs/2009.01325)
  - Nisan Stiennon, Long Ouyang, Jeff Wu, Daniel M. Ziegler, Ryan Lowe, Chelsea Voss, Alec Radford, Dario Amodei, Paul Christiano
  - Anahtar Kelime: Özet kalitesini önemsemek, Eğitim kaybı model davranışını etkiler, Ödül modeli yeni veri kümelerine genellenir
  - Code: [official](https://github.com/openai/summarize-from-feedback)
  - Dataset: [TL;DR](https://www.tensorflow.org/datasets/catalog/reddit), [CNN/DM](https://github.com/abisee/cnn-dailymail)
- [İnsan Tercihlerinden Dil Modellerine İnce Ayar](https://arxiv.org/abs/1909.08593)
  - Daniel M. Ziegler, Nisan Stiennon, Jeffrey Wu, Tom B. Brown, Alec Radford, Dario Amodei, Paul Christiano, Geoffrey Irving
  - Anahtar Sözcük: Dil öğrenmeyi ödüllendirme, Olumlu duygularla devam eden metin, Özet görev, Fiziksel betimleyici
  - Code: [official](https://github.com/openai/lm-human-preferences)
  - Dataset: [TL;DR](https://www.tensorflow.org/datasets/catalog/reddit), [CNN/DM](https://github.com/abisee/cnn-dailymail)
- [Ödül modelleme yoluyla ölçeklenebilir temsilci hizalaması: bir araştırma yönü](https://arxiv.org/abs/1811.07871)
  - Jan Leike, David Krueger, Tom Everitt, Miljan Martic, Vishal Maini, Shane Legg
  - Anahtar Kelime: Temsilci hizalama sorunu, Etkileşimden ödül öğrenme, RL ile ödülü optimize etme, Yinelemeli ödül modelleme
  - Code: [official](https://github.com/rddy/ReQueST)
  - Env: Atari
- [Atari'de insan tercihlerinden ve gösterilerden öğrenmeyi ödüllendirin](https://arxiv.org/abs/1811.06521)
  - Borja Ibarz, Jan Leike, Tobias Pohlen, Geoffrey Irving, Shane Legg, Dario Amodei
  - Anahtar Kelime: Uzman demonstrasyon yörünge tercihleri, bilgisayar korsanlığı problemini ödüllendirir, insan etiketindeki gürültü
  - Code: [official](https://github.com/rddy/ReQueST)
  - Env: Atari
- [Deep TAMER: Yüksek Boyutlu Durum Uzaylarında Etkileşimli Ajan Şekillendirme](https://arxiv.org/abs/1709.10163)
  - Garrett Warnell, Nicholas Waytowich, Vernon Lawhern, Peter Stone
  - Anahtar Kelime: Yüksek boyut durumu, İnsan eğitmeninin girdilerinden yararlanın
  - Code: [third party](https://github.com/bharadwaj1098/Tamer)
  - Env: Atari
- [İnsan tercihlerinden derinlemesine pekiştirmeli öğrenme](https://arxiv.org/abs/1706.03741)
  - Paul Christiano, Jan Leike, Tom B. Brown, Miljan Martic, Shane Legg, Dario Amodei
  - Anahtar Kelime: Yörünge çiftleri arasında insan tercihlerinde tanımlanan hedefi keşfedin, segmentasyon, İnsan geri bildiriminden daha karmaşık bir şey öğrenin
  - Code: [official](https://github.com/mrahtz/learning-from-human-preferences)
  - Env: Atari, MuJoCo
- [Politikaya Bağlı İnsan Geri Bildiriminden Etkileşimli Öğrenme](https://arxiv.org/abs/1701.06049)
  - James MacGlashan, Mark K Ho, Robert Loftin, Bei Peng, Guan Wang, David Roberts, Matthew E. Taylor, Michael L. Littman
  - Anahtar Sözcük: Karar, insan geri bildiriminden çok mevcut politikadan etkilenir, Yerel bir optimuma yakınsayan politikaya bağlı geri bildirimden öğrenin
  
##Google Makale Türk
-[CHATGPT İLE ÜRETİLEN İÇERİKLERİN
ESER NİTELİĞİNİN 5846 SAYILI FİKİR VE
SANAT ESERLERİ KANUNU BAKIMINDAN
DEĞERLENDİRİLMESİ](https://www.researchgate.net/profile/Osman-Gucluturk/publication/367022218_ChatGPT_ile_Uretilen_Iceriklerin_Eser_Niteliginin_5846_sayili_Fikir_ve_Sanat_Eserleri_Kanunu_Bakimindan_Degerlendirilmesi/links/63be6bf7a03100368a6be52f/ChatGPT-ile-Ueretilen-Iceriklerin-Eser-Niteliginin-5846-sayili-Fikir-ve-Sanat-Eserleri-Kanunu-Bakimindan-Degerlendirilmesi.pdf)


-[JOURNAL OF TOURISM AND GASTRONOMY STUDIES](https://www.researchgate.net/profile/Emrullah-Erul/publication/369589050_JOURNAL_OF_TOURISM_AND_GASTRONOMY_STUDIES_ChatGPT_ile_Sohbetler_Turizmde_ChatGPT'nin_Onemi_Chats_with_ChatGPT_Importance_of_ChatGPT_in_Tourism/links/6423641292cfd54f84357cd6/JOURNAL-OF-TOURISM-AND-GASTRONOMY-STUDIES-ChatGPT-ile-Sohbetler-Turizmde-ChatGPTnin-Oenemi-Chats-with-ChatGPT-Importance-of-ChatGPT-in-Tourism.pdf)




## Kod tabanları
```
biçim:
- [başlık](kod tabanı bağlantısı) [bağlantılar]
  - yazar1, yazar2 ve yazar3...
  - anahtar kelime
  - deney ortamları, veri kümeleri veya görevler
```
- [PaLM + RLHF - Pytorch](https://github.com/lucidrains/PaLM-rlhf-pytorch)
  - Phil Wang, Yachine Zahidi, Ikko Eltociear Ashimine, Eric Alcaide
  - Anahtar Kelime: Transformatörler, PaLM mimarisi
  - Dataset: [enwik8](http://prize.hutter1.net/)
- [lm-insan-tercihleri](https://github.com/openai/lm-human-preferences)
  - Daniel M. Ziegler, Nisan Stiennon, Jeffrey Wu, Tom B. Brown, Alec Radford, Dario Amodei, Paul Christiano, Geoffrey Irving
  - Anahtar Sözcük: Dil öğrenmeyi ödüllendirme, Olumlu duygularla devam eden metin, Özet görev, Fiziksel betimleyici
  - Dataset: [TL;DR](https://www.tensorflow.org/datasets/catalog/reddit), [CNN/DM](https://github.com/abisee/cnn-dailymail)
- [takip-talimatları-insan-geri bildirimi](https://github.com/openai/following-instructions-human-feedback)
  - Long Ouyang, Jeff Wu, Xu Jiang, et al.
  - Anahtar Kelime: Büyük Dil Modeli, Dil Modelini İnsan Niyetiyle Hizala
  - Dataset: [TruthfulQA](https://github.com/sylinrl/TruthfulQA) [RealToxicityPrompts](https://allenai.org/data/real-toxicity-prompts)
- [Trafo Takviyeli Öğrenme (TRL)](https://github.com/lvwerra/trl)
  - Leandro von Werra, Younes Belkada, Lewis Tunstall, et al.
  - Anahtar Kelime: LLM'yi RL, PPO, Transformer ile eğitin
  - Task: [IMDB sentiment](https://www.imdb.com/interfaces/)
- [Distributed training](https://github.com/CarperAI/trlx)
  - Jonathan Tow, Leandro von Werra, et al.
  - Anahtar Kelime: Dağıtılmış eğitim çerçevesi, T5 tabanlı dil modelleri, LLM'yi RL, PPO, ILQL ile Tren
  - Görev: Sağlanan ödül işlevini veya ödül etiketli veri setini kullanarak LLM ile LLM'de ince ayar yapın
- [RL4LM'ler (Dil modellerinde insan tercihlerine göre ince ayar yapmak için modüler bir RL kitaplığı)](https://github.com/allenai/RL4LMs)
  - Rajkumar Ramamurthy, Prithviraj Ammanabrolu, Kianté,Brantley, Jack Hessel, Rafet Sifa, Christian Bauckhage, Hannaneh Hajishirzi, Yejin Choi
  - Anahtar Kelime: RL, Benchmark, Performant RL algoritması ile dil oluşturucuları optimize etme
  - Dataset: [IMDB](https://www.imdb.com/interfaces/), [CommonGen](https://inklab.usc.edu/CommonGen/), [CNN Daily Mail](https://github.com/abisee/cnn-dailymail), [ToTTo](https://github.com/google-research-datasets/ToTTo), [WMT-16 (en-de)](https://www.statmt.org/wmt16/it-translation-task.html), [NarrativeQA](https://github.com/deepmind/narrativeqa), [DailyDialog](http://yanran.li/dailydialog)
- [HH-RLHF](https://github.com/anthropics/hh-rlhf)
  - Ben Mann, Deep Ganguli
- Anahtar Kelime: İnsan tercihi veri seti, Red takım oluşturma verileri, makine yazımı
  - Görev: Yararlılık ve zararsızlık hakkında insan tercihi verileri için açık kaynaklı veri kümesi
- [LaMDA-rlhf-pytorch](https://github.com/conceptofmind/LaMDA-rlhf-pytorch)
  - Phil Wang
  - Anahtar Kelime: LaMDA, Dikkat Mekanizması
  - Görev: Google'ın PyTorch'taki LaMDA araştırma makalesinin açık kaynaklı eğitim öncesi uygulamas
- [TextRL](https://github.com/voidful/TextRL)
  - Eric Lam
  - Anahtar kelime: huggingface'in trafosu
  - Görev: Metin oluşturma
  - Env: PFRL, gym
- [minRLHF](https://github.com/thomfoster/minRLHF)
  - Thomfoster
  - Anahtar kelime: PPO, Minimal kitaplık
  - Görev: eğitim amaçlı
- [Stanford Human Preferences Dataset(SHP)](https://huggingface.co/datasets/stanfordnlp/SHP)
  - Ethayarajh, Kawin and Zhang, Heidi and Wang, Yizhong and Jurafsky, Dan
  - Anahtar Kelime: Doğal olarak oluşan ve insan tarafından yazılan veri seti, 18 farklı konu alanı
  - Görev: RLHF ödül modellerini eğitmek için kullanılması amaçlanmıştır
- [PromptSource](https://github.com/bigscience-workshop/promptsource)
  - Stephen H. Bach, Victor Sanh, Zheng-Xin Yong et al.
  - Anahtar Kelime: İstemli İngilizce veri kümeleri, Bir veri örneğini doğal dile eşleme
  - Görev: Doğal dil istemleri oluşturmak, paylaşmak ve kullanmak için araç seti
- [Structured Knowledge Grounding(SKG) Resources Collections](https://unifiedskg.com/)
  - Tianbao Xie, Chen Henry Wu, Peng Shi et al.
  - Anahtar Kelime: Yapılandırılmış Bilgi Temellendirmesi
  - Görev: Veri kümelerinin toplanması, yapılandırılmış bilgi temeli ile ilgilidir
- [The Flan koleksiyon](https://github.com/google-research/FLAN/tree/main/flan/v2)
  - Longpre Shayne, Hou Le, Vu Tu et al.
  - Görev: Koleksiyon, Flan 2021, P3, Super-Natural Instructions'tan veri kümelerini derler


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

Amacımız bu depoyu daha da iyi hale getirmek. Katkıda bulunmakla ilgileniyorsanız, katkıyla ilgili talimatlar için lütfen [BURAYA](CONTRIBUTING_TU.md) bakın.

## Lisans

Müthiş RLHF, Apache 2.0 lisansı altında yayınlandı.
[01Kevin01](https://github.com/01Kevin01)
