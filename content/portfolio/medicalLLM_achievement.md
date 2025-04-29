+++
image = "img/medicalllm.png"
showonlyimage = true
date = "224-04-09T19:44:32+05:30"
title = "医療LLM"
draft = false
weight = 3
+++

医療AI・医療LLMの研究開発：これまでの自身の取り組み

<!--more-->

---
[実績]
1. [EQUES | 経産省NEDO　GENIAC「薬学分野・製薬業務に特化したLLMの開発」](#anchor8)
1. [岡山大学AI研究会](#anchor7)  
1. [東大松尾研LLM講座](#anchor6)    
1. [覚醒プロジェクト | 7B パラメタの日本語医療LLMの作成, NeurIPS WS 2024](#anchor5)
1. [覚醒プロジェクト | 医療LLMのベンチマークの作成](#anchor4)  
1. [東大病院 | 70Bパラメタの日本語医療LLM開発](#anchor3)    
1. [東大病院 | OpenCALM(7B)・Llama2(70B)の日本語医療適応, NeurIPS WS 2023](#anchor2)  
1. [東大病院 | 心電図から心疾患や年齢予測を行うAIモデル, NeurIPS WS 2022](#anchor1)  
---

<a id="anchor0"></a>
#### 医療LLMやデータセットの一覧作成（随時更新）

```
主要なLLMリリースの最新ニュースをまとめた一覧表の公開. 主に性能が良いとされているものや将来性がありそうなモデルを取り上げている.
```

1. [JMedData4LLM:Curation of Japanese Medical Data Sources for LLM development](https://github.com/stardust-coder/jmed-data-for-llm)
1. [Awesome latest LLMs](https://github.com/stardust-coder/awesome-latest-LLM)
    - ページ後半に医療ドメイン特化について記載しています.
1. [SpeakerDeck「医療分野に特化したLLM　研究紹介」](https://speakerdeck.com/stardust11)


<a id="anchor8"></a>
#### （関連）経産省NEDO　GENIAC「薬学分野・製薬業務に特化したLLMの開発」
```
株式会社EQUESの事業として、国内初（世界でも事例わずか）の製薬領域に特化したLLMの開発に挑戦しました。本事業の一環で、特化モデルだけではなく、薬剤師国家試験・名寄せ・齟齬点検の３種類のベンチマークを独自に構築しました。成果の大部分はパブリックに公開し、GENIACコミュニティおよびライフサイエンス業界の発展に貢献していきます。本プロジェクトはNEDOの支援を受けています。
```

1. [学習済みモデル（huggingface）]()
1. 登壇
    - [NVIDIA ソブリンAIヘルスケアDay with Macnica](https://go.macnica.co.jp/Entry-CLV-RS-NV-20250417-Sovereign-AI-Healthcare-Day.html)
    - [TAI AMAJ #05 「医薬領域特化LLMの開発と実用」](https://lu.ma/mzxodxyl)
    - [GENIAC キックオフイベント](https://www.youtube.com/watch?v=aISmHo47mDY)

<a id="anchor7"></a>
#### 岡山大学AI研究会 招待講演
```
医療LLMの研究動向や自身の取り組みについて紹介させていただきました。
```
- [第13回岡山大学AI研究会 招待講演](https://www.cc.okayama-u.ac.jp/imelab/ouai/index.html)


<a id="anchor6"></a>
#### 東大松尾研LLM講座 医療LLM回 担当講師
```
医療LLM関連の研究について講義を行いました。
```
- [松尾研LLMコミュニティ【Paper & Hacks Vol.26】 医療LLMの研究紹介](https://matsuolab-community.connpass.com/event/336858/) [アーカイブ](https://youtu.be/a4U2iFg48SY)
- [東京大学松尾・岩澤研究室 大規模言語モデルDeepLearning応用講座 2024Fall 第１１回](https://weblab.t.u-tokyo.ac.jp/education/large-language-model/) 

<a id="anchor5"></a>
#### 7B パラメタの日本語医療LLMの作成

```
最新のベースモデルを利用し, 日本語医療テキストを用いた学習を施した7BパラメタLLMの作成.    
本取り組みは産総研「覚醒プロジェクト」の支援を受けています.
```

1. [論文：Development and bilingual evaluation of Japanese medical large language model within reasonably low computational resources](https://arxiv.org/pdf/2409.11783)


<a id="anchor4"></a>
#### 医療LLMのベンチマークの作成

```
医療LLMのベンチマーク評価プログラムとリーダーボードの作成. 日英対訳の医学質問応答の正答率を評価する目的. プロンプトで容易に出力や精度が変化したりすることもあり, フェアな評価手法については議論の余地が多分にあります. 
本取り組みは産総研「覚醒プロジェクト」の支援を受けています.
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
2023年の取り組み. 日本で初めてLLMの医療チューニングへの挑戦.
```

1. [学習済みモデル(huggingface)](https://huggingface.co/AIgroup-CVM-utokyohospital/llama2-jmedlora-3000)
1. [論文：JMedLoRA:Medical Domain Adaptation on Japanese Large Language Models using Instruction-tuning](https://arxiv.org/abs/2310.10083) 
1. [言語処理学会：JMedLoRA:Instruction-tuning による日本語大規模モデルの医療ドメイン適用](https://www.anlp.jp/proceedings/annual_meeting/2024/pdf_dir/P9-4.pdf)
1. [論文：Development and analysis of medical instruction-tuning for Japanese large language models](https://accscience.com/journal/AIH/articles/online_first/1381)




<a id="anchor1"></a>
#### 心電図から心疾患や年齢予測を行うAIモデル

```
12誘導心電図を入力とし症状の有無を判定する分類器の作成. 東大病院の患者約13万件の心電図データでMasked AutoEncoderの事前学習も実施しました. 今回, 左室収縮機能障害は心エコーにおけるEF値の低下と定義しています. このように, 心電図を入力, 心エコー所見を出力として学習することで, より手軽な心電図検査のみで症状有無の予測が可能となることを目指しています.
```

1. [Masked Autoencoder-Based Self-Supervised Learning for Electrocardiograms to Detect Left Ventricular Systolic Dysfunction](https://neurips.cc/media/PosterPDFs/NeurIPS%202022/60064.png?t=1669681561.7912426)
1. [Age prediction from coronary angiography using a deep neural network: Age as a potential label to extract prognosis-related imaging features](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0276928)





