+++
date = "2016-11-05T21:05:33+05:30"
title = "Bookmark"
+++

### TO READ
* [Copula shrinkage and portfolio allocation in ultra-high dimensions](https://www.sciencedirect.com/science/article/abs/pii/S0165188922002123)
* [ダイナミック非対称t コピュラを用いた 新興国国債市場の相互依存構造に関する研究](https://www.jstage.jst.go.jp/article/jafee/17/0/17_45/_pdf)
- [Semiparametric copula-based analysis for treatment effects in the presence of treatment switching](https://onlinelibrary.wiley.com/doi/epdf/10.1002/sim.8585)
* [Yang and Barron, 1999](http://www.stat.yale.edu/~arb4/publications_files/Information-TheoreticDeterminationOfMinimaxRatesOfConvergenceAnnalsStatistics.pdf)
    - ノンパラ推定のminimaxレート導出


### コピュラ統計学
#### コピュラ一般
* [基本的な内容(IBIS 2009より)](https://ibisml.org/ibis2009/pdf-invited/yoshiba1.pdf)
* [極値での従属性および非対称性と信用ポートフォリオリスク(吉羽先生,2021)](https://www.jstage.jst.go.jp/article/jjssj/51/1/51_157/_pdf/-char/ja)
* [Bivariate distributions with ordered marginals](https://www.sciencedirect.com/science/article/pii/S0047259X19300831)
* [Relationship Between Kendall’s tau Correlation and Mutual Information](http://www.scielo.org.co/pdf/rce/v43n1/0120-1751-rce-43-01-3.pdf)
* [Copulae on products of compact Riemannian manifolds](https://www.sciencedirect.com/science/article/pii/S0047259X15001128)
* [Open Source Initiative for the Treatment of Uncertainties, Risks'N Statistics](https://openturns.github.io/openturns/latest/install.html)
* Parametric copula adjusted for non- and semiparametric regression, The Annals of Statistics(2022)
* On weak conditional convergence of bivariate Archimedean and Extreme Value copulas, and consequences to nonparametric estimation, Bernoulli(2021)
* Measuring dependence in the Wasserstein distance for Bayesian nonparametric models, The Annals of Statistics(2021)
* Inference for Archimax copulas, The Annals of Statistics(2020)
* Maximum entropy distribution of order statistics with given marginals, Bernoulli(2018)
* Vine copula approximation: a generic method for coping with conditional dependence, Stat Comput (2018) 28:219–237
* Stable feature selection using copula based mutual information, Pattern Recognition(2021)
* Portfolio optimization for inventory financing: Copula-based approaches, Computers & Operational Research (2021)
* COPOD: Copula-Based Outlier Detection, ICDM(2020)
* Computational Optimal Transport, Foundations and Trends in Machine Learning, 2019

#### 幾何
* [Permutation inference とbirkhoff polytope]()
    - バーコフ多面体 = チェス盤コピュラ全体
* [Geometry of Discrete Copula, Perrone 2019](https://arxiv.org/abs/1802.06969)

#### ベイズ
* [Bayesian Approaches to Copula Modelling](https://arxiv.org/abs/1112.4204)

#### Extreme Copula
* [A New Estimator for the Pickands Dependence Function](https://digitalcommons.wayne.edu/cgi/viewcontent.cgi?article=2108&context=jmasm)
* extreme copulaの密度関数 [link](https://ethz.ch/content/dam/ethz/special-interest/math/risklab-dam/documents/walter-saxer-preis/ma-doyon.pdf)
* [Kamnitui et al.](https://www.sciencedirect.com/science/article/pii/S0022247X18310035)
    - 緩和extreme copulaのうちτを固定した下で選べる範囲の解析 

#### コピュラエントロピーに関する研究 
* [Multivariate Normality Test with Copula Entropy](https://arxiv.org/pdf/2206.05956.pdf) 著者:[Jian Ma](https://scholar.google.com/citations?hl=en&user=gqCD4kwAAAAJ&view_op=list_works&sortby=pubdate)
* [copent: Estimating Copula Entropy and Transfer Entropy in R](https://arxiv.org/pdf/2005.14025.pdf)
     - copula entropyの推定手法. Transfer entropy. [Github](https://github.com/majianthu/copent)
* [Causal Domain Adaptation with Copula Entropy based Conditional Independence Test](https://arxiv.org/pdf/2202.13482.pdf)

<最小情報コピュラ>
* [Copulas with Maximum Entropy(Piantadosi et al.)](https://carma.edu.au/resources/jon/copulas.pdf)
    - チェスコピュラに対するエントロピー最大化
* [Maximum entropy distribution of order statistics with given marginals (Bernoulli 2018)](https://projecteuclid.org/journals/bernoulli/volume-24/issue-1/Maximum-entropy-distribution-of-order-statistics-with-given-marginals/10.3150/16-BEJ868.full)
     - 周辺分布を固定しエントロピー最大化. multidiagonalsの問題に帰着.
* [最小情報コピュラとその周辺]()
* [Copula Approximation, Durrlemann 2000]()
    - コピュラのBernstein近似とチェス盤近似. 裾従属性とpertubation.


#### 応用
* 情報検索
    - [Eickhoff et al. (ACM SIGIR 2013)](http://www-personal.umich.edu/~kevynct/pubs/sigir2013-eickhoff-copulas.pdf)
        - 軸の統合は線形結合よりコピュラの方が優秀
    - [Eickhoff et al. 2015](https://www.researchgate.net/publication/277940908_Modelling_Term_Dependence_with_Copulas)
        - コピュラを用いた検索モデルが高精度
    - [Komatsuda et al. 2016](https://db-event.jpn.org/deim2016/papers/124.pdf)
* 気象データ
    - Vrac et al. 
* 処置効果(Treatment effects)
    

#### コピュラとTotal Positivity
* [TP2 MTP2 提案論文](https://reader.elsevier.com/reader/sd/pii/0047259X80900652?token=90D2635E6FD9DA80EEF977F5C161BAEBA729553C81DB0368B6AB4F405D72F5D9F4F523DDBC111DF55797389E1D759B59&originRegion=us-east-1&originCreation=20220920131057)
* [TOTAL POSITIVITY IN MARKOV STRUCTURE 2016](https://arxiv.org/pdf/1510.01290.pdf)
* [Total positivity of copulas from a Markov kernel perspective](https://arxiv.org/pdf/2205.01914.pdf)
    - d-TP2 => MK-TP2 => TP2

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
* [FOURCASTNET(NVIDIA)](https://arxiv.org/pdf/2202.11214.pdf)
* [Adaptive Fourier Neural Operators: Efficient Token Mixers for Transformers(NVIDIA, ICLR2022)](https://arxiv.org/pdf/2111.13587.pdf) [Github](https://github.com/NVlabs/AFNO-transformer)
* [MP-PAWR](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/11914/1191416/Comparative-study-of-deep-neural-networks-for-very-short-term/10.1117/12.2601830.short?SSO=1) [著者](https://researchmap.jp/satoh-radarmeteo/published_papers)
    - [理研論文](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2021MS002823)

#### Matlantis
- [Matlantisに関する論文(PFN, Nature Communications)](https://matlantis.com/ja/cases#related)
    - 第一原理計算をせずに電子状態を予測するNeuralNetworkを学習



### その他
- [日本の統計学者](https://sites.google.com/site/shoutoyonekura/国内の統計学者リスト)
- [CMStatistics](https://twitter.com/intent/follow?original_referer=http%3A%2F%2Fwww.cmstatistics.org&ref_src=twsrc%5Etfw%7Ctwcamp%5Ebuttonembed%7Ctwterm%5Efollow%7Ctwgr%5ECFECMStatistics&screen_name=CFECMStatistics)
    - 統計学の国際会議, 12月開催
- [ISI WSC2023](https://www.isi2023.org/conferences/ottawa-2023/contributed-paperposter-sessions/#)
- [Joint Statistical Meeting](https://ww2.amstat.org/meetings/jsm/2023/)
    - 統計学の国際会議, 8月開催
- [WikiCFP](http://www.wikicfp.com/cfp/call?conference=statistics)
- [マスプロ](https://www.springer.com/journal/10107)
    - IF 3.06-4.26
- [EJOR](https://www.journals.elsevier.com/european-journal-of-operational-research)
    - IF 6.36
- [武田先生](https://www.u-tokyo.ac.jp/focus/ja/features/voices036.html)
- [金融情報学](https://www.ai-gakkai.or.jp/resource/my-bookmark/my-bookmark_vol37-no1/)
- [データサイエンスの魅力](https://engineer-lab.findy-code.io/jobs-in-statistics)
- [結局、統計学と機械学習は何が違うのか？](https://exploratory.io/note/kanaugust/2200910721280297)