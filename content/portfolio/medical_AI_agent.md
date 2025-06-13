+++
image = "img/blog.png"
showonlyimage = true
date = "224-04-09T19:44:32+05:30"
title = "医療AIエージェント構築に向けた材料"
draft = false
weight = 3
+++

医療AIエージェントについて考察

<!--more-->

# 材料（国外の取り組みを参考に）
- [Med-R1](https://huggingface.co/yuxianglai117/Med-R1)
    - Qwen2-VL-2B をGRPOでファインチューニング
    - Qwen2-VL-72B超
- [OmniV-Med](https://arxiv.org/abs/2504.14692)
    - 各タスクのSOTAモデルに対し, あらゆるベンチで上回った
    - 1.5Bと7B
- [MedGemma](https://huggingface.co/collections/google/medgemma-release-680aade845f90bec6a3f60c4)
    - 4BのVLMと, 27BのLLM
    - 現状かなり有力なLLM
- [LingShu](https://arxiv.org/abs/2506.07044)
    - モデル, コードは未公開. 7B.
    - MedEvalKitという包括的ベンチマークでスコア更新
- [MedGemini](https://arxiv.org/pdf/2404.18416)
    - 現状最強の医療マルチモーダルモデル. closed.
    - 検索エンジンを活用したself-training（学習時）とuncertainty-guided search（推論時）の工夫.

# ツール
- [AgentIQ（NVIDIA）](https://developer.nvidia.com/agent-intelligence-toolkit)



# 個別タスクに対する取り組み
- [EHR]()
- [サマリ]()
- [SOAPノート](https://aclanthology.org/2025.cl4health-1.4.pdf#page10)