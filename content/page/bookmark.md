+++
date = "2016-11-05T21:05:33+05:30"
title = "Bookmark"
+++

### TO READ
* [Copula shrinkage and portfolio allocation in ultra-high dimensions](https://www.sciencedirect.com/science/article/abs/pii/S0165188922002123)
- [Semiparametric copula-based analysis for treatment effects in the presence of treatment switching](https://onlinelibrary.wiley.com/doi/epdf/10.1002/sim.8585)
* [Yang and Barron, 1999](http://www.stat.yale.edu/~arb4/publications_files/Information-TheoreticDeterminationOfMinimaxRatesOfConvergenceAnnalsStatistics.pdf)
    - ノンパラ推定のminimaxレート導出
* [column generation](https://arxiv.org/pdf/2103.12624.pdf)
    - 列生成の
* Copula-Based Markov Models for Time Series: Parametric Inference and Process Control

### コピュラ統計学
#### コピュラ一般
* [基本的な内容(IBIS 2009より)](https://ibisml.org/ibis2009/pdf-invited/yoshiba1.pdf)
* [塚原先生](https://www.jstage.jst.go.jp/article/jjssj/51/1/51_101/_pdf)
    - おすすめ.
* [Bivariate distributions with ordered marginals](https://www.sciencedirect.com/science/article/pii/S0047259X19300831)
* [Copulae on products of compact Riemannian manifolds](https://www.sciencedirect.com/science/article/pii/S0047259X15001128)
* [Parametric copula adjusted for non- and semiparametric regression](https://projecteuclid.org/journals/annals-of-statistics/volume-50/issue-2/Parametric-copula-adjusted-for-non--and-semiparametric-regression/10.1214/21-AOS2126.short), The Annals of Statistics(2022)
* [Measuring dependence in the Wasserstein distance for Bayesian nonparametric models](https://projecteuclid.org/journals/annals-of-statistics/volume-49/issue-5/Measuring-dependence-in-the-Wasserstein-distance-for-Bayesian-nonparametric-models/10.1214/21-AOS2065.short), The Annals of Statistics(2021)
* Vine copula approximation: a generic method for coping with conditional dependence, Stat Comput (2018) 28:219–237


#### コピュラの幾何学
* [Permutation inference とbirkhoff polytope]()
    - バーコフ多面体 = チェス盤コピュラ全体
* [Geometry of Discrete Copula, Perrone 2019](https://arxiv.org/abs/1802.06969)
    - ウルトラモジュラコピュラ

#### Bayesianコピュラ
* [Bayesian Approaches to Copula Modelling](https://arxiv.org/abs/1112.4204)
* [MCMC for copula](http://proceedings.mlr.press/v5/silva09a/silva09a.pdf)

#### Extreme Copula（極値コピュラ）
* [A New Estimator for the Pickands Dependence Function](https://digitalcommons.wayne.edu/cgi/viewcontent.cgi?article=2108&context=jmasm)
* extreme copulaの密度関数 [link](https://ethz.ch/content/dam/ethz/special-interest/math/risklab-dam/documents/walter-saxer-preis/ma-doyon.pdf)
* [Kamnitui et al.](https://www.sciencedirect.com/science/article/pii/S0022247X18310035)
    - 緩和extreme copulaのうちτを固定した下で選べる範囲の解析 
* On weak conditional convergence of bivariate Archimedean and Extreme Value copulas, and consequences to nonparametric estimation, Bernoulli(2021)


#### コピュラエントロピーに関する研究 
* [Multivariate Normality Test with Copula Entropy](https://arxiv.org/pdf/2206.05956.pdf) 著者:[Jian Ma](https://scholar.google.com/citations?hl=en&user=gqCD4kwAAAAJ&view_op=list_works&sortby=pubdate)
* [copent: Estimating Copula Entropy and Transfer Entropy in R](https://arxiv.org/pdf/2005.14025.pdf)
     - copula entropyの推定手法. Transfer entropy. [Github](https://github.com/majianthu/copent)
* [Causal Domain Adaptation with Copula Entropy based Conditional Independence Test](https://arxiv.org/pdf/2202.13482.pdf)
* Maximum entropy distribution of order statistics with given marginals, Bernoulli(2018)


#### 最小情報コピュラ関連
* [Copulas with Maximum Entropy(Piantadosi et al.)](https://carma.edu.au/resources/jon/copulas.pdf)
    - チェス盤コピュラに対するエントロピー最大化
* [Maximum entropy distribution of order statistics with given marginals (Bernoulli 2018)](https://projecteuclid.org/journals/bernoulli/volume-24/issue-1/Maximum-entropy-distribution-of-order-statistics-with-given-marginals/10.3150/16-BEJ868.full)
     - 周辺分布を固定しエントロピー最大化. multidiagonalsの問題に帰着.
* [最小情報コピュラとその周辺]()
* [Copula Approximation, Durrleman 2000]()
    - コピュラのBernstein近似とチェス盤近似. 裾従属性とpertubation.


#### コピュラ×機械学習
* [概観](https://pluto.huji.ac.il/~galelidan/papers/CopulaMLSurvey.pdf)
    - まとまっていて理解しやすい
* Inference for Archimax copulas, The Annals of Statistics(2020)
    - 続編 Inference and sampling for Archimax copulas

#### 応用
* 金融
    - [ダイナミック非対称$t$コピュラを用いた 新興国国債市場の相互依存構造に関する研究](https://www.jstage.jst.go.jp/article/jafee/17/0/17_45/_pdf)
    - [確率的依存構造をもつコピュラモデル](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-087.pdf)
    - [極値での従属性および非対称性と信用ポートフォリオリスク(吉羽先生,2021)](https://www.jstage.jst.go.jp/article/jjssj/51/1/51_157/_pdf/-char/ja)

* 情報検索
    - [Eickhoff et al. (ACM SIGIR 2013)](http://www-personal.umich.edu/~kevynct/pubs/sigir2013-eickhoff-copulas.pdf)
        - 軸の統合は線形結合よりコピュラの方が優秀
    - [Eickhoff et al. 2015](https://www.researchgate.net/publication/277940908_Modelling_Term_Dependence_with_Copulas)
        - コピュラを用いた検索モデルが高精度
    - [Komatsuda et al. 2016](https://db-event.jpn.org/deim2016/papers/124.pdf)

* 気象データ
    - Vrac et al. 
* 処置効果(Treatment effects)
* Stable feature selection using copula based mutual information (Pattern Recognition 2021)
* Portfolio optimization for inventory financing: Copula-based approaches, (Computers & Operational Research 2021)
* COPOD: Copula-Based Outlier Detection, (ICDM 2020)

#### コピュラとTotal Positivity
* [TP2 MTP2 提案論文](https://reader.elsevier.com/reader/sd/pii/0047259X80900652?token=90D2635E6FD9DA80EEF977F5C161BAEBA729553C81DB0368B6AB4F405D72F5D9F4F523DDBC111DF55797389E1D759B59&originRegion=us-east-1&originCreation=20220920131057)
* [TOTAL POSITIVITY IN MARKOV STRUCTURE 2016](https://arxiv.org/pdf/1510.01290.pdf)
* [Total positivity of copulas from a Markov kernel perspective](https://arxiv.org/pdf/2205.01914.pdf)
    - d-TP2 => MK-TP2 => TP2

##### 行列のTotal Positivity一般
* [Total positivity of recursive matrices](https://arxiv.org/pdf/1601.05645.pdf)
* [The logarithmic method and the solution to the TP2-completion problem](https://scholarworks.wm.edu/cgi/viewcontent.cgi?article=3357&context=etd)
* [Some properties of TP matrices](https://reader.elsevier.com/reader/sd/pii/0024379576900768?token=84BA6EE2C3FA46FD3D07418AB4C032CC21FDBF005A0D4E4B7E9792913BB69541FE9ECEB5C20CBE243C436609CB2E71DE&originRegion=us-east-1&originCreation=20221128121736)
    - TP行列はTPとTPへのLU分解可能.
* [On totally positive matrices and geometric incidences](https://www.cs.bgu.ac.il/~shakhar/my_papers/TP.pdf)
    - repeated 2 × 2 minors in a special class of n × n TP-matrices

#### コピュラと順位相関と相互情報量
- [On the size of the class of bivariate extreme-value copulas with a fixed value of Spearman's rho or Kendall's tau](https://www.sciencedirect.com/science/article/pii/S0022247X18310035)
    - pickand functionが取れる形の広さを評価.
- [On the exact region determined by Kendall’s tau and Spearman’s rho](https://arxiv.org/pdf/1502.04620.pdf)
    - 従来知られていたtau vs rhoの可動域をstrictに評価.
- [Estimating Mutual Information](https://arxiv.org/pdf/cond-mat/0305641.pdf)
    - 相互情報量推定の一般的な話.
- [上記相互情報量推定に使われたライブラリ](https://github.com/karlstratos/doe)
- [Inductive Mutual Information Estimation](https://arxiv.org/pdf/2102.13182.pdf)
    - 最大エントロピー原理に基づいて相互情報量推定. 
- [On Variational Bounds of Mutual Information](https://arxiv.org/pdf/1905.06922.pdf)
* [Relationship Between Kendall’s tau Correlation and Mutual Information](http://www.scielo.org.co/pdf/rce/v43n1/0120-1751-rce-43-01-3.pdf)

#### コピュラの実装
* [PyCop](https://github.com/maximenc/pycop)
* [Open Source Initiative for the Treatment of Uncertainties, Risks'N Statistics](https://openturns.github.io/openturns/latest/install.html)


### マルコフ基底・代数統計
* [青木先生&竹村先生のGrobner School 2012](http://www.math.kobe-u.ac.jp/crest-c/cs-2012/2012-02-22-aoki-takemura.pdf)
    - 相似検定, 対数線形モデル
* [原先生のIBISML2010](https://ibisml.org/ibis2010/session/ibis2010hara.pdf)
    - 正確検定, 部分マルコフ基底
* [分割表の列挙とランダム生成](https://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/1289-6.pdf)
    - 整数計画問題
* [分割表の一致率検定とFisher の正確確率法](https://core.ac.uk/download/pdf/228569891.pdf)
* [多項ロジットモデルの適合度検定のためのマルコフ基底の計算](https://www.i.u-tokyo.ac.jp/edu/course/mi/master/2018/a/hamada.pdf)

### 最適輸送理論
* [THE SINKHORN-KNOPP ALGORITHM: CONVERGENCE AND APPLICATIONS](https://strathprints.strath.ac.uk/19685/1/skapp.pdf)
* [Quantitative Stability of Regularized Optimal Transport and Convergence of Sinkhorn’s Algorithm](https://arxiv.org/pdf/2110.06798.pdf)


### 機械学習
#### Transformer関連
* [Unveiling Transformers with LEGO](https://www.youtube.com/watch?v=brmidghOP6c) [論文](https://arxiv.org/abs/2206.04301)
    - Transformersの定性的理解をLEGO(方程式(変数&演算子)をテキストとして入力し, 解く)というタスクを通して行う. 
* [Transformerについてのまとめ論文(DeepMind)](https://arxiv.org/pdf/2207.09238.pdf)

#### 因果推論・因果探索
* 因果探索 [電通の人のブログ](https://note.com/dd_techblog/n/nc8302f55c775)

#### 気象予測
* [Nature論文](https://www.nature.com/articles/s41586-021-03854-z.pdf)
    - GANで雲を予想. なぜNature?
* [ForecastNet(NVIDIA)](https://arxiv.org/pdf/2202.11214.pdf)
* [Adaptive Fourier Neural Operators: Efficient Token Mixers for Transformers(NVIDIA, ICLR2022)](https://arxiv.org/pdf/2111.13587.pdf) [Github](https://github.com/NVlabs/AFNO-transformer)
* [MP-PAWR](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/11914/1191416/Comparative-study-of-deep-neural-networks-for-very-short-term/10.1117/12.2601830.short?SSO=1) [著者](https://researchmap.jp/satoh-radarmeteo/published_papers)
    - [理研論文](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2021MS002823)

### 離散変数のサンプリング
- Hamming Sampler (2015)
- Informed Proposal for Local MCMC
    - PIPというefficientなproposalをdiscrete spaceに対して提案. ざっくりacceptance rateが1になる.
- Gibbs with Gradient (ICML2021)
- Path Auxiliary Sampler (ICLR2022)
- [Langevin Monte Carloの実装](https://github.com/abdulfatir/langevin-monte-carlo)
- [exchange algorithm sampling](https://statweb.stanford.edu/~cgates/PERSI/papers/sturm98.pdf)


### 学会・雑誌・研究者
- [日本の統計学者](https://sites.google.com/site/shoutoyonekura/国内の統計学者リスト)
- [オックスフォード大学の関連組織](https://www.oxford-man.ox.ac.uk/research-overview/)
- [CMStatistics](https://twitter.com/intent/follow?original_referer=http%3A%2F%2Fwww.cmstatistics.org&ref_src=twsrc%5Etfw%7Ctwcamp%5Ebuttonembed%7Ctwterm%5Efollow%7Ctwgr%5ECFECMStatistics&screen_name=CFECMStatistics)
    - 統計学の国際会議, 12月開催
- [ISI WSC2023](https://www.isi2023.org/conferences/ottawa-2023/contributed-paperposter-sessions/#)
    - 統計学の国際会議, 12月締切, 7月開催
- [Joint Statistical Meeting](https://ww2.amstat.org/meetings/jsm/2023/)
    - 統計学の国際会議, 2月締切, 8月開催
- [応用数理学会](https://jsiam.org/union2023)
    - 1月締切
- [WikiCFP](http://www.wikicfp.com/cfp/call?conference=statistics)
- [マスプロ](https://www.springer.com/journal/10107)
- [EJOR](https://www.journals.elsevier.com/european-journal-of-operational-research)
- [先生](https://www.u-tokyo.ac.jp/focus/ja/features/voices036.html)
- [CWTS Journal Indicators](https://www.journalindicators.com/indicators)

### その他
- [金融情報学ブックマーク（和泉先生）](https://www.ai-gakkai.or.jp/resource/my-bookmark/my-bookmark_vol37-no1/)
- [データサイエンスの魅力](https://engineer-lab.findy-code.io/jobs-in-statistics)
- [結局、統計学と機械学習は何が違うのか？](https://exploratory.io/note/kanaugust/2200910721280297)
