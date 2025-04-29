+++
image = "img/blog.png"
showonlyimage = true
date = "2025-03-22T00:00:00+00:00"
title = "Repro Samples Methodとは"
draft = true
weight = 999
+++

<!--more-->


[FisherのFiducial Inference](https://en.wikipedia.org/wiki/Fiducial_inference)

Bayes + Frequent + Fiducial = BFF

漸近論を回避する枠組みが最近考えられている.


### 問題設定
以下のようなGenerativeなモデルからデータが生成されているとする。
$$Y = G(\theta, U)$$
$U$の分布は$\theta$にはよらない。$G$は既知の関数とする。

Realizationバージョンも考える。
$$Y^{obs} = G(\theta_0, u^{rel})$$
$u^{rel}$という$U$のrealizationが得られないので, 可能な限り近い$u^*$をプラグインすることを考える。

### 目標
- さまざまなパラメタやデータに対して、有意水準$\alpha$の信頼集合を$\theta$に対して構成する。

### Repro sample法
Repro sample $Y^*$を$u^*$からシミュレーションする。もし＄Y^{obs} = Y^*$ なら$\theta ~ \theta_0$が期待されるので$\theta$を候補集合の中に含めておく。このやり方だと候補集合 $\Gamma_\alpha$が
$$P(\theta_0 \in \Gamma_\alpha(Y)) \geq \alpha$$
を満たすことが保証される（Xie and Wang, 2024）。

$$P\{T(U,\theta) \in B_\alpha(\theta)} \geq \alpha, \forall \theta$$
なるマップ$T(u,\theta)$があるとする。
不確実性は$T(U,\theta)$を通して定量化される。