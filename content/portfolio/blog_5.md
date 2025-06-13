+++
image = "img/blog.png"
showonlyimage = true
date = "2025-03-22T00:00:00+00:00"
title = "FGMコピュラが意外と使える話"
draft = true
weight = 999
+++

<!--more-->

[Risk aggregation with FGM copulas](https://www.sciencedirect.com/science/article/abs/pii/S0167668723000331)(IME)
- FGMコピュラは従属性の範囲も狭ければ裾従属性も無いのに, リスク評価に使える!?
- FGMコピュラの確率表現を導入.（stochastic representation）
    - Bernoulli marginal. Uniform copulaからランダムにインデックス（大きい方, 小さい方）を割り振る.

Marius Hofert先生による拡張が面白い.
[Index-mixed copula](https://arxiv.org/abs/2306.10663)
$$C(u) = E_I[\Pi_{k=1}^K C_k(u^{I_{:,k}};\theta_k) ]$$
Indexの分布$I$に関する期待値でmixtureを表現する. 従来のmixtureだけではなく, marginalもmixtureの要素に入れられる柔軟性.
Tailもbaseコピュラに由来するため, 作り出すことができる.

