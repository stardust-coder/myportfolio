+++
image = "img/blog.png"
showonlyimage = true
date = "2025-02-18T00:00:00+00:00"
title = "コピュラ統計学について"
draft = false
weight = 999
+++

<!--more-->

**コピュラ統計学 (Copula statistics)という分野の概観**

---

対象：コピュラに関する分野をざっくり知りたい方、コピュラを学び始めた方

※ 本稿は分野やキーワードの概観が主旨なので、コピュラについてや研究内容の解説は含まれません。


## 概観

### 最初に読むと良いもの
- [**Copulas: Tales and facts**](https://www.uio.no/studier/emner/matnat/math/STK9200/h21/mikosch2006_article_copulastalesandfacts.pdf) (Thomas Mikosch, 2006)


### 教科書
- [An introduction to copulas](https://mistis.inrialpes.fr/docs/Nelsen_2006.pdf), Nelsen(2007)
- [Dependence Modeling with Copulas](https://www.taylorfrancis.com/books/mono/10.1201/b17116/dependence-modeling-copulas-harry-joe) , Joe(2014)
- [Everything You Always Wanted to Know about Copula Modeling but Were Afraid to Ask](https://www.uni-muenster.de/Physik.TP/~lemm/seminarSS08/JHE-2007.pdf) (Genest)


### コピュラ統計の重要なテーマ 5選
- 特に金融データに多く見られる**上下非対称性・裾従属性(fat tail)・確率変動**を表現したい → 投資配分の決定などに役立てる
    - 近年は非対称tコピュラが注目されている
        - [Smith et al. (2012)](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=0f802c316ed7498a90c4ed28f8bd90987b3867d2)でベイズ推定.
        - [Yoshiba(2018)](https://www.ism.ac.jp/editsec/resmemo/resmemo-file/resm1195.pdf)で最尤推定.
        - [Christoffersen et al. (2012)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1573345)でダイナミカルモデル.
        - [非対称 t 接合関数の性質と統計的推定方法(吉羽2019)](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-045.pdf)

- ***系列相関***を含む時系列データを分析するための時系列モデル
    - コピュラ・マルコフ連鎖モデル
        - [Sun(2020)](https://link.springer.com/book/10.1007/978-981-15-4998-4)
    - copula-GARCH
        - innovation項のcopulaの影響が不明 [参考](https://www.fs.hub.hit-u.ac.jp/inc/files/performance/masters-thesis/2011/finalp0929.pdf)
        - [Patton(2009)](https://ora.ox.ac.uk/objects/uuid:1957361c-cede-4252-aa2a-b3d59e8653cd/download_file?file_format=pdf&safe_filename=2007OMI10.pdf&type_of_work=Working+paper)
    - 高次元拡張
        - ARCHのときはfactor-basedやDCCで解決してきた部分.
- ***３次元以上***のモデル化
    - Vine コピュラ
        - 分解する際に現れる条件付き接合関数が条件付け変量に依存しないと想定される“簡単化の仮定”について [**Pair-copula constructions of multivariate copulas**](https://mediatum.ub.tum.de/doc/1079253/651951.pdf)
            - アルキメデス型接合関数族ではクレイトン族のみがこの仮定を満たす. Gaussianやtも.
- empirical copula process（経験コピュラ過程）の漸近理論
    - 現代的な経験過程の結果を用いたアプローチ
        - [Weak convergence of empirical copula processes(Fermanian et al., 2004)](https://projecteuclid.org/journals/bernoulli/volume-10/issue-5/Weak-convergence-of-empirical-copula-processes/10.3150/bj/1099579158.full)
        - [Weak convergence of empirical copula processes indexed by functions (Radulovic et al., 2017)](https://projecteuclid.org/journals/bernoulli/volume-23/issue-4B/Weak-convergence-of-empirical-copula-processes-indexed-by-functions/10.3150/16-BEJ849.full)
- 機械学習・深層学習と関連した応用
    - コピュラ自体をNNで表現する系
        - [Deep archimedean copula](https://arxiv.org/pdf/2012.03137.pdf)
        - [Copula Density Neural Estimation](https://arxiv.org/pdf/2211.15353.pdf)
    - コピュラを組み込んだアーキテクチャで機械学習する系
        - Transformer系
            - [TACTIS](https://arxiv.org/abs/2202.03528), [TACTIS-2](https://openreview.net/forum?id=xtOydkE1Ku) など
        - Diffusion系
            - [Diffusion Copulas: Identification and Estimation](https://arxiv.org/pdf/2005.03513.pdf)
            - [A copula-based method to build diffusion models with prescribed marginal and serial dependence](https://arxiv.org/pdf/1509.02319.pdf)
        - その他
            - [NN-Copula-CD: A Copula-Guided Interpretable Neural Network for Change Detection in Heterogeneous Remote Sensing Images](https://arxiv.org/pdf/2303.17448.pdf)
            - [Copula GNN](https://iclr.cc/virtual/2021/poster/2572) 
            - [LEARNING SPARSE LATENT REPRESENTATIONS WITH THE DEEP COPULA INFORMATION BOTTLENECK](https://arxiv.org/pdf/1804.06216.pdf)


### コピュラの重要なLimitation

- 多変量解析に対し、明確なメリットがない
    - 周辺分布とコピュラはある種つながっており、完全に分離するコピュラによる推定はバイアスを生む → どうしたらバイアス下げられる？ 
- コピュラ選択に対する正当性
    - 多くの応用研究での適用では「数理的性質がうれしい」、にとどまる
- 基準分布としての曖昧さ
    - non-gaussianな実世界における, gaussian的存在になりたい. コピュラは関数クラスが広すぎる. [Mikosch, 2006]
- 統計理論の発展
    - 推定における感度分析
    - フィッティングの良さをどう測れば良いのか
    - コピュラへのフィットとデータへのフィットの差分
- 極値統計に無力
- 時系列モデリングに無力

### コピュラの推定手法の研究

#### パラメトリックモデル
- Archimedean copulaに対するInversion of Kendall's $\tau$, MLE, MMEなどが一般的.
    - (例) [Some Results on Point Estimation of the Association Parameter of a Bivariate Frank Copula](https://www.tandfonline.com/doi/full/10.1080/03610918.2025.2545611?src=exp-la)

#### セミパラコピュラモデル：周辺分布をノンパラ、コピュラをパラメトリックに推定
- [セミパラメトリックコピュラモデルにおけるダイバージェンスの性質(Sei and Matsumoto)](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-025.pdf)
- [Hoff et al. (2007)](https://arxiv.org/pdf/math/0610413.pdf)でLAN（局所漸近正規性に関する条件）に関する研究
    - 「Gaussian copulaに対しては正規分布」などの, rank likelihoodに対して良い近似が存在すると嬉しい.
- Information bounds on Gaussian copulas [[Hoff 2014](https://arxiv.org/pdf/1110.3572.pdf)]
- [Segers et al.(2014)]()でstructured Gaussianに対し, 有効推定量を構成することに成功.
- Maximum pseudo-likelihood (MPLE) [[Kojadinovic and Yan, 2010](https://econpapers.repec.org/article/eeeinsuma/v_3a47_3ay_3a2010_3ai_3a1_3ap_3a52-63.htm)]
    - consistent, 時にefficient
    - expected value of order statisticsを利用
    - overestimate dependence especially for small weakly dependent samples
        - → 代わりにmedianかmodeを利用すると改善 [[Dias, 2022](https://arxiv.org/pdf/2208.01322.pdf)]

#### ノンパラ推定
- [Fermanian & Scaillet (2003)](https://scaillet.ch/pdfs/copula.pdf)
    - faster rate of convergence at $n^{−1/2}$
- [Chen and Huang (2007)](https://www.songxichen.com/Uploads/Files/Publication/Chen-Huang-copula-07.pdf) 
    - Kernel estimator
    - boundary biasが問題となる
- [Autin et al.(2010)](https://www.i2m.univ-amu.fr/perso/florent.autin/Copulas.pdf)
    - nonlinear wavelet estimators, thresholding method, minimax on the spaces $\mathcal{B}_{2\infty}^s$

- [Ghosh and Lu (2021)](https://arxiv.org/pdf/2112.10351.pdf) 
    - 経験ベイズを利用

- [Nonparametric estimation of copulas and copula densities by orthogonal projections](https://arxiv.org/pdf/2010.15351.pdf%5C%5C%5C%5C)

- [Strong uniform convergence rates of the linear wavelet estimator of a multivariate copula density(2023)](https://arxiv.org/pdf/2303.05627.pdf)
    - optimal in a minimax sense over Besov balls for the supremum norm loss
    - see Theorem 3.1


### 金融応用
- 日銀からの文献 [1](https://www.imes.boj.or.jp/research/papers/japanese/kk24-b2-3.pdf) [2](https://www.imes.boj.or.jp/research/papers/japanese/kk29-3-4.pdf)
- [Copulas for finance(Durrleman, Roncalli)](http://www.thierry-roncalli.com/download/copula-survey.pdf)


### コピュラの理論

- [Sklarの定理の証明](https://pdf.sciencedirectassets.com/271532/1-s2.0-S0893965913X00072/1-s2.0-S0893965913001183/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEBsaCXVzLWVhc3QtMSJHMEUCIQC6Mfml0oNuRmSLq%2BgSVvHb2BTIrwPqtSo1mCTsuvMHnQIgYxitVicV5RpG68eOGnV1796ig8g8bRBz0slvVLOqq1MqvAUI0%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAFGgwwNTkwMDM1NDY4NjUiDGDx2xmTnH4nN%2BMbtSqQBdH7WF9fVGhfhGsIm%2FC1uQa4U1PXUmeCsgSqn3vpS17SDzGJr5SXCqOro0jywl0jvQUycOuZswVoS%2B%2BKdaquzCVN4BLhBvuN0f5keTJzhaOGlszlxtzpzumesfnP9gStOiynhIPjsarwqF4oBjgXrzp2YYNb%2B9d%2FISPczuNv4o5OKNynaROtwEyiqDvN4F%2BImJyEXu%2BCmKz%2FL06UcdrEfMiziZTtYfKNYsqo1QSLzm%2BxbjQkhVHpOP4R3SiQeNzH7LCQwRw%2FCmLTU4Jg48bL2PFSjjSiYFwDjJFehTM6X7Sq3BKYsb4dsTY8hC9qxWBgpxH%2FDvHsA%2FwydnvAeAc7pjxsKUa1ty5r4CRZEYSytmelEP5HFZDSbLNS1IlREo1o7oFfZ7QS1xrFwh%2FApM4TTKgkpvefeZS%2BvKGcrHkQlxWDL9SMigm7sUn3LScyL9J8iWSkUnYQpvECNr%2F3s%2FGmyvNgXBTb0%2F2cEIdVzo6u2k8jHpR2FP5LcgHaZn6K%2FNlqqicY%2Forl54T6tdgmj3ugaFKEAz6eWF22e243RyAafWEFJAWJfvAANiMAOLWU0JLW714XW12KL18VaT4OjdlVKBJMQIuejbhmMxdN%2B7nqknf7jc16UhEhVcbSYzbd6Ebe%2BIQ0048VkncYQEJthiKmPh8GUUHaE3N%2F7OAchtuWINio3S5%2FqhEIeX2Ewt74E%2F8sst%2BWhW2xmtW3FAsIhzDBdxrhk7iVK1n9kTKFKkVEiGHHjzejswHI0OteVyNJhHEY65CZ5uF9xTHo5%2Bx9fx95pWoWHjDKl6QpQQuem%2B5cJsgKGj8HcFMf35ci61YmWIKEA%2F63hvd%2B%2FUDypFdG5XgCsDQdmCFws3kHwH7ws%2BgobU18MKTvjKcGOrEBZJPdBN53YW7tnf44lb4TMqo%2BpWRINcX6E3vw8gg%2FeKDaVb0eosTf2bNm2mNTFfRjws0ESmqNVWSg4YAkX7huKfUA7mDrhm0H%2BOq2dXxat0zuvRna5RviLrVlzkejg0jywuY6D7ZShrlve1jjCY1R9A8jUlCDxE3ergYCUzshM1k3S5MIcL45yEvMRk4RakiQ%2BeSa8P15dLbMoQ6S7vcXY8gO0Y35vOBCai%2B6RqJHth6X&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20230821T103439Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYTNMLF5EL%2F20230821%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=e324072db1536dde9cb71dde5a63f8618f66a5c8095a076b2cd40964842cff87&hash=a3b0ba30cb2c9a675dc21d65d0fea3eb006c2285fa452427667907a839770745&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S0893965913001183&tid=spdf-3230a61e-67d6-4a30-9bf9-725c73905272&sid=5497b4ea577a36464d6822f986286e67cc45gxrqa&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=1011570104555758580a&rr=7fa2398dcdf38072&cc=jp)
- [接合関数モデルにおける統計的推測（塚原2020）](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-005.pdf)
- [リスク解析における接合関数（塚原2021）](https://www.jstage.jst.go.jp/article/jjssj/51/1/51_101/_pdf)

---

## コピュラに関するキーワード

### 裾従属性・裾従属係数

- 裾従属係数のノンパラ推定
    - [Ferreira 2013](https://www.ine.pt/revstat/pdf/rs130101.pdf)

### コピュラのモデル選択

実用上毎度直面する問題だが、あまり研究は豊富ではない。

- [Which copula is the right one?](http://www.thierry-roncalli.com/download/copula-choice.pdf)
- [Copula Information Criteria](https://biopen.bi.no/bi-xmlui/bitstream/handle/11250/226105/The%20copula%20information%20criteria%202014.pdf?sequence=5)
- [Bayesian copula selection](https://d1wqtxts1xzle7.cloudfront.net/43927781/Bayesian_copula_selection20160320-19907-11r1q20-libre.pdf?1458502162=&response-content-disposition=inline%3B+filename%3DBayesian_copula_selection.pdf&Expires=1687534341&Signature=b59IEoocNqD1aC8uwJhNeK9sQ9GSNqupJjkYUrdsBM8C3IyEKxfwDm0iuX-TslHD-5D58yrJdSP8QWYc3~0YeDp1lkOKuX1ug7LPinqkPkpgWj9nLpavZuKEKHKKeUKIF4eDM4F4698ALIMTU3dJillu9Jov9iZg3dQuatevA2nJ0wRyjIDYKipe~9ooxzaLD2taJre72EMYstODmQPFvQGDcTX46WvpBzClEzOTJzuyeXMktGOck3wo-Mbz8JBMPS37K-NONd99DFbRN2WNxLKsYqTIhNxKeeujWYrd9QMIvBM0PZJCNHHAKwI77YvjCymC3iSsEGMjoysMAAtuyw__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)




### チェス版コピュラ・Bernsteinコピュラ
コピュラの代表的な離散近似の仕方です。

- [弱収束とチェス盤コピュラ](https://www.sciencedirect.com/science/article/pii/S0047259X17301896)
- [Testing Symmetry for Bivariate Copulas using Bernstein Polynomials](https://arxiv.org/pdf/2109.03694.pdf)
- [Empirical Bernstein copula](https://arxiv.org/pdf/2202.12787.pdf)

### Archimedean Copula関連

Aruchimedeanコピュラは、一番シンプルで扱いやすい形式をしているコピュラのクラス（族）です。
- [Archimaxコピュラの推定](https://www.imstat.org/wp-content/uploads/2019/03/AOS1836.pdf)
- [多次元Archimedeanコピュラの推定](https://www.sciencedirect.com/science/article/pii/S0047259X12000607?ref=pdf_download&fr=RR-2&rr=7b297eb6fb0af699)
- [Sampling from Archimedean copulas](https://www.uni-ulm.de/fileadmin/website_uni_ulm/mawi/forschung/PreprintServer/2007/preprintmariushofert.pdf)
- [Semiparametric Archimedean Copula](https://orbi.uliege.be/bitstream/2268/24473/1/VandenhendeLambert2005.pdf)


--- 


## 隣接テーマ

以下は間接的な関わりがある関連テーマ.

### Local Dependence（局所従属性）

- [Holland and Wang (1987)](https://www.semanticscholar.org/paper/Dependence-function-for-continuous-bivariate-Holland-Wang/a1d6e1d028ceee0b94fd2ac4cbacc7e69793d08f)
- [Kurowicka and van Horssen (2015)](https://www.sciencedirect.com/science/article/pii/S0047259X14002863)
    - LDF of elliptical and archimedean copulas.
    - extension to higher dimensions (canonical Archimedean)
- [Copula-based local dependence framework](http://www.huangzaixin.com/papers/Manuscript.pdf)
    - その応用論文：https://arxiv.org/pdf/2003.04007.pdf


### 最適輸送

最適輸送とコピュラは実は密接に関わりがある。

- [WASSERSTEIN DISTANCE IN TERMS OF THE COMONOTONICITY COPULA](https://arxiv.org/pdf/2307.08402.pdf)
- [Optimal transportで非線形な従属性を測る話](https://arxiv.org/pdf/1610.09659.pdf)

### 相互情報量

相互情報量と負のコピュラエントロピーは等しいことが知られている。[Ma, 2011]

- [Physrev (2018)](https://harveylab.hms.harvard.edu/pdf/safaai2018.pdf)
- [Non-parametric estimation of copula based mutual information](https://www.tandfonline.com/doi/abs/10.1080/03610926.2018.1563180?journalCode=lsta20)
- [Inductive Mutual Information Estimation(AISTATS 2021)](http://proceedings.mlr.press/v130/kom-samo21a/kom-samo21a.pdf)
    - DoE Estimator https://github.com/karlstratos/doe
    - KXY https://github.com/kxytechnologies/kxy-python
- [fastMI (2023)](https://arxiv.org/pdf/2212.10268.pdf)
- [Copula Gaussian process](https://github.com/NinelK/CopulaGP)
- [Relationship Between Kendall’s tau Correlation and Mutual Information](http://www.scielo.org.co/pdf/rce/v43n1/0120-1751-rce-43-01-3.pdf)


### その他従属性一般の話題
- [Some concepts of dependence](https://link.springer.com/content/pdf/10.1007/978-1-4614-1412-4_64.pdf), Lehmann(1966)
- [Multivariate dependence concepts through copulas](https://www.sciencedirect.com/science/article/pii/S0888613X15000523)
- [X+Yの分布](https://arxiv.org/pdf/2107.00007.pdf)
- Total positivity, [Fuchs et al., 2023](https://arxiv.org/abs/2205.01914)
- [Chatterjee correlation](https://arxiv.org/abs/1909.10140)