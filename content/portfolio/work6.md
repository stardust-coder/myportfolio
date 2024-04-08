+++
image = "img/llama.png"
showonlyimage = true
date = "224-04-09T19:44:32+05:30"
title = "Medical AI"
draft = false
weight = 4
+++

東大病院の研究員として２年間・産総研「覚醒」研究代表者として半年  
取り組んだ医療AI・医療LLM
<!--more-->

[心電図から心疾患や年齢予測を行うAIモデル](#anchor1)  
[OpenCALM(7B)・Llama2(70B)の日本語医療適応](#anchor2)  
[70B（700億）パラメタの日本語医療LLM開発](#anchor3)    
[医療LLMのベンチマークの作成](#anchor4)  


---
---
---


<a id="anchor1"></a>
### 心電図から心疾患や年齢予測を行うAIモデル

```
12誘導心電図を入力とし症状の有無を判定する分類器の作成. 東大病院の患者約13万件の心電図データでMasked AutoEncoderの事前学習も実施しました. 今回, 左室収縮機能障害は心エコーにおけるEF値の低下と定義しています. このように, 心電図を入力, 心エコー所見を出力として学習することで, より手軽な心電図検査のみで症状有無の予測が可能となることを目指しています.
```

1. Shinnosuke Sawano, Satoshi Kodera, Hirotoshi Takeuchi, Issei Sukeda, Susumu Katsushika, and Issei Komuro :  
<u>**Masked Autoencoder-Based Self-Supervised Learning for Electrocardiograms to Detect Left Ventricular Systolic Dysfunction**</u>
    , NeurIPS Workshop on Learning from Time Series for Health, 2022. [✔︎poster](https://neurips.cc/media/PosterPDFs/NeurIPS%202022/60064.png?t=1669681561.7912426)

1. Shinnosuke Sawano, Satoshi Kodera, Masataka Sato, Susumu Katsushika, Issei Sukeda, ... , and Issei Komuro:  
<u>**Age prediction from coronary angiography using a deep neural network: Age as a potential label to extract prognosis-related imaging features**</u>
    , Plos one 17(10), 2022. [✔︎paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0276928)



<a id="anchor2"></a>
### OpenCALM(7B)・Llama2(70B)の日本語医療適応

```
日本で初めてLLMの医療チューニングにトライしました. 時代の流れが早く, 今となっては特に意味のない研究ですが...
```

**モデル**
* [日本語医療LLM JMedLoRA @ huggingface](https://huggingface.co/AIgroup-CVM-utokyohospital/llama2-jmedlora-3000)

**論文**
1. Issey Sukeda, Masahiro Suzuki, Hiroki Sakaji, and Satoshi Kodera:  
<u>**JMedLoRA:Medical Domain Adaptation on Japanese Large Language Models using Instruction-tuning**</u>
    , NeurIPS Workshop Deep Generative Models for Health, 2023.
    [✔︎arxiv](https://arxiv.org/abs/2310.10083) 

1. Issey Sukeda, Masahiro Suzuki, Hiroki Sakaji, Satoshi Kodera:
<u>**Development and analysis of medical instruction-tuning for Japanese large language models**</u>
, Artificial Intellignece for Health 2695, 2024. [✔︎paper](https://accscience.com/journal/AIH/articles/online_first/1381)


<a id="anchor3"></a>
### 70B（700億）パラメタの日本語医療LLM開発

```
東工大より日本語70BモデルであるSwallowがリリースされたので, 早速医療チューニングに使ってみました. 結果, 日本医師国家試験の正答率が50%近くまで伸びました. 一方で, GPT-4は8~9割正答できるという報告がありますし, まだまだ発展の余地しかない状況です.
```

1. Issey Sukeda, Risa Kishikawa, and Satoshi Kodera:  
<u>**70B-parameter large language models in Japanese medical question-answering**</u>
[✔︎arxiv]()

<a id="anchor4"></a>
### 医療LLMのベンチマークの作成

* [日本語医療モデル評価用ベンチマーク / Japanese Medical Language Model Evaluation Harness](https://github.com/stardust-coder/japanese-lm-med-harness)


