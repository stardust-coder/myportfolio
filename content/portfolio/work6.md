+++
image = "img/llama.png"
showonlyimage = true
date = "224-04-09T19:44:32+05:30"
title = "Medical AI"
draft = false
weight = 4
+++

医療AI・医療LLMの研究開発

<!--more-->

<!-- ---
1. [7B パラメタの日本語医療LLMの作成](#anchor5)
1. [医療LLMのベンチマークの作成](#anchor4)  
1. [70Bパラメタの日本語医療LLM開発](#anchor3)    
1. [OpenCALM(7B)・Llama2(70B)の日本語医療適応](#anchor2)  
1. [心電図から心疾患や年齢予測を行うAIモデル](#anchor1)  
--- -->

<a id="anchor0"></a>
#### 医療LLMやデータセットの一覧作成（随時更新）

```
主要なLLMリリースの最新ニュースをまとめた一覧表. 主に性能が良いとされているものや将来性がありそうなモデルを取り上げている.
```

1. [JMedData4LLM:Curation of Japanese Medical Data Sources for LLM development](https://github.com/stardust-coder/jmed-data-for-llm)
1. [Awesome latest LLMs](https://github.com/stardust-coder/awesome-latest-LLM)
    - ページ後半に医療ドメインについて記載.


<a id="anchor5"></a>
#### 7B パラメタの日本語医療LLMの作成

```
最新のベースモデルを利用し, 日本語医療テキストを用いた学習を施した7BパラメタLLMの作成.    
本取り組みは産総研「覚醒プロジェクト」の支援を受けています.
```

1. [論文：Development and bilingual evaluation of Japanese medical large language model within reasonably low computational resources (Coming soon...)]()
1. [学習済みモデル(huggingface, 現在非公開)](https://huggingface.co/stardust-coder/jmedllm-7b-v1)


<a id="anchor4"></a>
#### 医療LLMのベンチマークの作成

```
医療LLMのベンチマーク評価プログラムとリーダーボードの作成. 日英対訳の医学質問応答の正答率を評価する目的.　　
プロンプトで容易に出力や精度が変化したりすることもあり, フェアな評価手法については悩ましい.
```
論点  
・Q&Aの５択問題を解かせるので良いのか.  国家試験でいいのか.  
・Q&Aの５択問題の正解率を評価するにはどうするのが良いか. ← 最近はhuggingface等を通して統一的になりつつある.

1. [医療LLM評価用ベンチマーク / Japanese Medical Language Model Evaluation Harness](https://github.com/stardust-coder/japanese-lm-med-harness)
    - 特徴１：推論にvllmを利用し高速化を図る
    - 特徴２：プロンプトテンプレートをオプションで指定できる
    - 特徴３：回答と正答のゲシュタルト距離をもとに選択肢を１つ選んだと"みなす"


<a id="anchor3"></a>
#### 70B パラメタの日本語医療LLM開発

```
東工大よりリリースされた日本語70BモデルであるSwallowの医療チューニング. 結果, 日本医師国家試験の正答率が50%近くまで到達. 一方で, GPT-4は8~9割正答できるという報告があり, まだまだ発展の余地しかない状況.
```

1. [学習済みモデル(huggingface)](https://huggingface.co/AIgroup-CVM-utokyohospital/MedSwallow-70b)
1. [論文：70B-parameter large language models in Japanese medical question-answering](https://arxiv.org/abs/2406.14882)



<a id="anchor2"></a>
#### OpenCALM(7B)・Llama2(70B)の日本語医療適応

```
日本で初めてLLMの医療チューニングへの挑戦.
```

1. [学習済みモデル(huggingface)](https://huggingface.co/AIgroup-CVM-utokyohospital/llama2-jmedlora-3000)
1. [論文：JMedLoRA:Medical Domain Adaptation on Japanese Large Language Models using Instruction-tuning](https://arxiv.org/abs/2310.10083) 
1. [論文：Development and analysis of medical instruction-tuning for Japanese large language models](https://accscience.com/journal/AIH/articles/online_first/1381)




<a id="anchor1"></a>
#### 心電図から心疾患や年齢予測を行うAIモデル

```
12誘導心電図を入力とし症状の有無を判定する分類器の作成. 東大病院の患者約13万件の心電図データでMasked AutoEncoderの事前学習も実施しました. 今回, 左室収縮機能障害は心エコーにおけるEF値の低下と定義しています. このように, 心電図を入力, 心エコー所見を出力として学習することで, より手軽な心電図検査のみで症状有無の予測が可能となることを目指しています.
```

1. [Masked Autoencoder-Based Self-Supervised Learning for Electrocardiograms to Detect Left Ventricular Systolic Dysfunction](https://neurips.cc/media/PosterPDFs/NeurIPS%202022/60064.png?t=1669681561.7912426)
1. [Age prediction from coronary angiography using a deep neural network: Age as a potential label to extract prognosis-related imaging features](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0276928)





