+++
image = "img/blog.png"
showonlyimage = true
date = "2025-02-18T00:00:00+00:00"
title = "コピュラ統計学について"
draft = true
weight = 999
+++

<!--more-->

**コピュラ統計学 (Copula statistics)**


---

### 最初に読むとよい. 

- Nelsen(2007)
- Joe(2014)
- [**Copulas: Tales and facts**](https://www.uio.no/studier/emner/matnat/math/STK9200/h21/mikosch2006_article_copulastalesandfacts.pdf)
- [Everything You Always Wanted to Know about Copula Modeling but Were Afraid to Ask](https://www.uni-muenster.de/Physik.TP/~lemm/seminarSS08/JHE-2007.pdf)(Genest)
- [リスク解析における接合関数（塚原2021）](https://www.jstage.jst.go.jp/article/jjssj/51/1/51_101/_pdf)
- [Copulas for finance(Durrleman, Roncalli)](http://www.thierry-roncalli.com/download/copula-survey.pdf)
- [Sklarの定理の証明](https://pdf.sciencedirectassets.com/271532/1-s2.0-S0893965913X00072/1-s2.0-S0893965913001183/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEBsaCXVzLWVhc3QtMSJHMEUCIQC6Mfml0oNuRmSLq%2BgSVvHb2BTIrwPqtSo1mCTsuvMHnQIgYxitVicV5RpG68eOGnV1796ig8g8bRBz0slvVLOqq1MqvAUI0%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAFGgwwNTkwMDM1NDY4NjUiDGDx2xmTnH4nN%2BMbtSqQBdH7WF9fVGhfhGsIm%2FC1uQa4U1PXUmeCsgSqn3vpS17SDzGJr5SXCqOro0jywl0jvQUycOuZswVoS%2B%2BKdaquzCVN4BLhBvuN0f5keTJzhaOGlszlxtzpzumesfnP9gStOiynhIPjsarwqF4oBjgXrzp2YYNb%2B9d%2FISPczuNv4o5OKNynaROtwEyiqDvN4F%2BImJyEXu%2BCmKz%2FL06UcdrEfMiziZTtYfKNYsqo1QSLzm%2BxbjQkhVHpOP4R3SiQeNzH7LCQwRw%2FCmLTU4Jg48bL2PFSjjSiYFwDjJFehTM6X7Sq3BKYsb4dsTY8hC9qxWBgpxH%2FDvHsA%2FwydnvAeAc7pjxsKUa1ty5r4CRZEYSytmelEP5HFZDSbLNS1IlREo1o7oFfZ7QS1xrFwh%2FApM4TTKgkpvefeZS%2BvKGcrHkQlxWDL9SMigm7sUn3LScyL9J8iWSkUnYQpvECNr%2F3s%2FGmyvNgXBTb0%2F2cEIdVzo6u2k8jHpR2FP5LcgHaZn6K%2FNlqqicY%2Forl54T6tdgmj3ugaFKEAz6eWF22e243RyAafWEFJAWJfvAANiMAOLWU0JLW714XW12KL18VaT4OjdlVKBJMQIuejbhmMxdN%2B7nqknf7jc16UhEhVcbSYzbd6Ebe%2BIQ0048VkncYQEJthiKmPh8GUUHaE3N%2F7OAchtuWINio3S5%2FqhEIeX2Ewt74E%2F8sst%2BWhW2xmtW3FAsIhzDBdxrhk7iVK1n9kTKFKkVEiGHHjzejswHI0OteVyNJhHEY65CZ5uF9xTHo5%2Bx9fx95pWoWHjDKl6QpQQuem%2B5cJsgKGj8HcFMf35ci61YmWIKEA%2F63hvd%2B%2FUDypFdG5XgCsDQdmCFws3kHwH7ws%2BgobU18MKTvjKcGOrEBZJPdBN53YW7tnf44lb4TMqo%2BpWRINcX6E3vw8gg%2FeKDaVb0eosTf2bNm2mNTFfRjws0ESmqNVWSg4YAkX7huKfUA7mDrhm0H%2BOq2dXxat0zuvRna5RviLrVlzkejg0jywuY6D7ZShrlve1jjCY1R9A8jUlCDxE3ergYCUzshM1k3S5MIcL45yEvMRk4RakiQ%2BeSa8P15dLbMoQ6S7vcXY8gO0Y35vOBCai%2B6RqJHth6X&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20230821T103439Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYTNMLF5EL%2F20230821%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=e324072db1536dde9cb71dde5a63f8618f66a5c8095a076b2cd40964842cff87&hash=a3b0ba30cb2c9a675dc21d65d0fea3eb006c2285fa452427667907a839770745&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S0893965913001183&tid=spdf-3230a61e-67d6-4a30-9bf9-725c73905272&sid=5497b4ea577a36464d6822f986286e67cc45gxrqa&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=1011570104555758580a&rr=7fa2398dcdf38072&cc=jp)

### コピュラ統計の重要なテーマ
- 金融データに多く見られる, ***上下非対称性・裾従属性(fat tail)・確率変動***を表現したい → 投資配分の決定
    - 近年は非対称tコピュラが注目されている
        - [Smith et al. (2012)](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=0f802c316ed7498a90c4ed28f8bd90987b3867d2)でベイズ推定. Sahu, Dey & Branco (2003)のskew t分布をもとに.
        - [Yoshiba(2018)](https://www.ism.ac.jp/editsec/resmemo/resmemo-file/resm1195.pdf)で最尤推定
        - ダイナミックへの拡張も Christoffersen et al. (2012)や夷藤・中村（2019）
    - 確率的コピュラ
        - 野澤・中村. 確率的ヴァインコピュラ
- ***系列相関***を含む時系列データを分析するための時系列モデル
    - コピュラ・マルコフ連鎖モデル
        - [Sun(2020)](https://link.springer.com/book/10.1007/978-981-15-4998-4), [Emura](https://www.jstage.jst.go.jp/article/jjssj/51/1/51_101/_pdf/-char/ja)
    - copula-GARCH, innovation項のcopulaの影響が不明 [参考](https://www.fs.hub.hit-u.ac.jp/inc/files/performance/masters-thesis/2011/finalp0929.pdf)
        - [Patton(2009)](https://ora.ox.ac.uk/objects/uuid:1957361c-cede-4252-aa2a-b3d59e8653cd/download_file?file_format=pdf&safe_filename=2007OMI10.pdf&type_of_work=Working+paper)
    - 高次元拡張. ARCHのときはfactor-basedやDCCで解決してきた.
- ***３次元以上***のモデル化（***多変量***）
    - 特にヴァインコピュラ、分解する際に現れる条件付き接合関数が条件付け変量に依存しないと想定される“簡単化の仮定” [**Pair-copula constructions of multivariate copulas**](https://mediatum.ub.tum.de/doc/1079253/651951.pdf)
        - アルキメデス型接合関数族ではクレイトン族のみがこの仮定を満たす. Gaussianやtも.
        - Hobæk Haff et al, St ̈ober et al. (2013)
    - mixed derivative measure of interaction function(Holland and Wang)
- よりよいリスク管理・軽量化（応用より）
    - 空間相関、降雨、災害、水害…
- empirical copula processの漸近理論
    - 現代的な経験過程の結果を用いたアプローチ
        - Weak convergence of empirical copula processes(Bernoulli)
        - Weak convergence of empirical copula processes indexed by functions(Bernoulli, 2017, Cornell)
- 機械学習・深層学習の応用

[コピュラの重要な課題 (2006時点で、バブルだった）]

- 多変量解析に対し、明確なメリットがない
    - 周辺分布とコピュラはある種つながっており、完全に分離するコピュラによる推定はバイアスを生む → どうしたらバイアス下げられる？
    - [接合関数モデルにおける統計的推測](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-005.pdf)
- コピュラ選択に対する正当性
    - 多くの応用研究での適用では「数学的性質がうれしい」、にとどまる
- 基準分布として
    - non-gaussianな実世界における, gaussian的存在になりたい. コピュラは関数クラスが広すぎる.
- 統計理論の発展
    - 推定における感度分析
    - フィッティングの良さをどうはかるか
    - コピュラへのフィットとデータへのフィットの差分
- 極値統計に無力
- 時系列モデリングに無力

### コピュラの推定

[セミパラ]

[セミパラメトリックコピュラモデルにおけるダイバージェンスの性質](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-025.pdf)

Rank likelihood

- [Hoff 2007](https://arxiv.org/pdf/math/0610413.pdf)でLAN（局所漸近正規性に関する条件）,
    - rank likelihoodに良い近似が存在すると嬉しい. Gaussian copulaに対しては正規分布…など
- Segers 2014でstructured Gaussianに対し, 有効推定量

Archimedeanに対するInversion of τ

- 典型的

Inversion of Beta [[Genest, 2013](http://www.numdam.org/item/JSFS_2013__154_1_5_0.pdf)]

- やってみたところイマイチだった

Maximum pseudo-likelihood (MPLE) [[Kojadinovic and Yan, 2010](https://econpapers.repec.org/article/eeeinsuma/v_3a47_3ay_3a2010_3ai_3a1_3ap_3a52-63.htm)]

- consistent, 時にefficient
- expected value of order statisticsを利用
- overestimate dependence especially for small weakly dependent samples
    - → 代わりにmedianかmodeを利用すると改善 [[Dias, 2022](https://arxiv.org/pdf/2208.01322.pdf)]

[分布のノンパラ推定]

Deheuvels (1979) multivariate empirical distribution on the marginal empirical distributions

Gijbels & Mielnicnuk (1990)

Fermanian (2005), goodness-of-fit test

[コピュラのノンパラ推定]

Fermanian & Scaillet (2003) コピュラを直接推定 , faster rate of convergence at n−1/2

[Chen and Huang 2007](https://www.songxichen.com/Uploads/Files/Publication/Chen-Huang-copula-07.pdf) コピュラを直接推定 

- Kernel estimator
- boundary biasが問題となる！

Autin et al.(2010) 

- nonlinear wavelet estimators, thresholding method, minimax on the spaces $\mathcal{B}_{2\infty}^s$

[Ghosh and Lu (2021)](https://arxiv.org/pdf/2112.10351.pdf) 経験ベイズを利用

Nonparametric estimation of copulas and copula densities by orthogonal projections [https://arxiv.org/pdf/2010.15351.pdf](https://arxiv.org/pdf/2010.15351.pdf%5C%5C%5C%5C)

- [Strong uniform convergence rates of the linear wavelet estimator of a multivariate copula density(2023)](https://arxiv.org/pdf/2303.05627.pdf)
    - optimal in a minimax sense over Besov balls for the supremum norm loss
    - Theorem 3.1

[裾従属係数のノンパラ推定]

[Ferreira 2013](https://www.ine.pt/revstat/pdf/rs130101.pdf)

[統計的学習への応用]

[Solving Estimating Equations With Copulas](https://arxiv.org/pdf/1801.10576.pdf)

### Information bounds

- Information bounds on Gaussian copulas [[Hoff 2014](https://arxiv.org/pdf/1110.3572.pdf)]

### Local Dependence

- Holland and Wang (1987)
    - joint = marginals + LDF (under mild conditions)
- Wang (1993)
    - “iterative replacement algorithm” ... method to determine joint from
    - marginals and LDF. & trivariate LDF.
- Molenberghs and Lesaffre (1997)
    - numerical extensions using non-linear integral equations.
- [Jones (1997)](https://www.sciencedirect.com/science/article/pii/S0047259X97917140?ref=pdf_download&fr=RR-2&rr=7ecbb60fca128a6c)
    - constant LDF θ leads to p(x1, x2) = a(x1; θ)b(x2; θ)ex1x2 . Plackett より優れた解釈可能性.
- Gupta(2004) : the vector failure + LDF determines the pdf.
- Gupta et al.(2010): FGM, AHM, elliptical copulas. TP2 との同値性.
- [Kurowicka and van Horssen (2015)](https://www.sciencedirect.com/science/article/pii/S0047259X14002863)
    - LDF of elliptical and archimedean copulas.
    - extension to higher dimensions (canonical Archimedean)
- Koutoumanou et al.(2017)
    - beta marginals
- [Copula-based local dependence framework](http://www.huangzaixin.com/papers/Manuscript.pdf)
    - その応用 https://arxiv.org/pdf/2003.04007.pdf
- [Nonparametric Universal Copula Modeling](https://arxiv.org/abs/1912.05503) (2019)
- [Towards a universal representation of statistical dependence](https://arxiv.org/abs/2302.08151)(2023)

### 群モデル

- [セミパラメトリックコピュラモデルにおけるダイバージェンスの性質](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-025.pdf)
- [塚原2020](https://www.ism.ac.jp/editsec/toukei/pdf/68-1-005.pdf)
- [不変確率モデル](https://www.ism.ac.jp/editsec/toukei/pdf/47-1-063.pdf)

### 最適輸送

- [WASSERSTEIN DISTANCE IN TERMS OF THE COMONOTONICITY COPULA](https://arxiv.org/pdf/2307.08402.pdf)
- measuring non-linear dependence
    - https://gmarti.gitlab.io/qfin/2020/06/25/copula-optimal-transport-dependence.html
    - https://arxiv.org/pdf/1610.09659.pdf

### Mutual Informationをcopula basedで推定する

- Physrev 2018 https://harveylab.hms.harvard.edu/pdf/safaai2018.pdf
- 2020 https://www.tandfonline.com/doi/abs/10.1080/03610926.2018.1563180?journalCode=lsta20
- AISTATS 2021 http://proceedings.mlr.press/v130/kom-samo21a/kom-samo21a.pdf
    - DoE Estimator https://github.com/karlstratos/doe
    - KXY https://github.com/kxytechnologies/kxy-python
- 2023 fastMI https://arxiv.org/pdf/2212.10268.pdf

- Copula Gaussian process https://github.com/NinelK/CopulaGP
- Information bottleneck https://proceedings.neurips.cc/paper_files/paper/2012/file/3cef96dcc9b8035d23f69e30bb19218a-Paper.pdf
- [**Relationship Between Kendall’s tau Correlation and Mutual Information**](http://www.scielo.org.co/pdf/rce/v43n1/0120-1751-rce-43-01-3.pdf)

### Transfer entropyを推定する

- https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwj-k-702cb_AhWbm1YBHZYiBrI4RhAWegQIAxAB&url=https%3A%2F%2Fwww.atlantis-press.com%2Farticle%2F25879098.pdf&usg=AOvVaw24e14PwkaJLPOtE7lHRwG-
- Granger causalityとの関連 https://arxiv.org/pdf/0910.4514.pdf
- http://www.er.ams.eng.osaka-u.ac.jp/Paper/2007/Sumioka07a.pdf
- https://arxiv.org/pdf/nlin/0001042.pdf

### 従属性一般

- [Some concepts of dependence](https://link.springer.com/content/pdf/10.1007/978-1-4614-1412-4_64.pdf) Lehmann(1966)
- [**Multivariate dependence concepts through copulas**](https://www.sciencedirect.com/science/article/pii/S0888613X15000523)
- X+Yの分布 https://arxiv.org/pdf/2107.00007.pdf
- 
- Total positivity
    - https://core.ac.uk/download/pdf/71544262.pdf
    - Fuchs 2023

### Entropy Copula関連

#### 最小情報コピュラ
- [最小情報従属モデリング](https://arxiv.org/pdf/2206.06792.pdf)
- [単調性](https://arxiv.org/pdf/1611.06714.pdf) Y. Tenzer and G. Elidan, On the monotonicity of the copula entropy
- https://www.sciencedirect.com/science/article/abs/pii/S0022169420309628
- [New copulas obtained by maximizing Tsallis or R ́enyi Entropies. 内容同じ？](https://hal.science/hal-00833323/document)https://hal.science/hal-00591062/document
    - [MaxEnt](http://djafari.free.fr/MaxEnt2010/slide/068.pdf)
        - tomographyとcopulaは等価 [link between](https://hal.science/hal-00509705/document)
- [tコピュラについて](https://core.ac.uk/download/pdf/234003915.pdf)
    - 期待値ベクトルと分散共分散行列が一定の分布の中で，タリス・エントロピーを最大にする分布は多変量 t 分布である(q-gaussianの極限)
    - Q. コピュラに限定した場合，最大分布は t コピュラになるのか

#### Tsallis分布やTsallisエントロピーについて
- [Tsalis分布と堆積モデル](https://www.notion.so/72b9dda2c7924487a5adde34c65b64c7?pvs=21)
- [Tsalisエントロピーとマルチフラクタル](https://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/1630-01.pdf)
- [Interaction function](https://reader.elsevier.com/reader/sd/pii/S0047259X14002863?token=4519FB9281CBAECA10DACDE791E3F65A7CAD988537FED06D2BB61E2E27DDEF05ACC3D6E55338EC2C33FC635AFD8BA3FF&originRegion=us-east-1&originCreation=20230404014415)
- **Development of a Maximum Entropy-Archimedean Copula-Based Bayesian Network Method for Streamflow Frequency Analysis—A Case Study of the Kaidu River Basin, China**
    - 応用研究、フレームワーク
- 読めないやつ
    - https://www.tandfonline.com/doi/abs/10.1080/03610918.2017.1387660

### コピュラの選択

- http://www.thierry-roncalli.com/download/copula-choice.pdf
- [CIC](https://biopen.bi.no/bi-xmlui/bitstream/handle/11250/226105/The%20copula%20information%20criteria%202014.pdf?sequence=5)
- [Baysean copula selection](https://d1wqtxts1xzle7.cloudfront.net/43927781/Bayesian_copula_selection20160320-19907-11r1q20-libre.pdf?1458502162=&response-content-disposition=inline%3B+filename%3DBayesian_copula_selection.pdf&Expires=1687534341&Signature=b59IEoocNqD1aC8uwJhNeK9sQ9GSNqupJjkYUrdsBM8C3IyEKxfwDm0iuX-TslHD-5D58yrJdSP8QWYc3~0YeDp1lkOKuX1ug7LPinqkPkpgWj9nLpavZuKEKHKKeUKIF4eDM4F4698ALIMTU3dJillu9Jov9iZg3dQuatevA2nJ0wRyjIDYKipe~9ooxzaLD2taJre72EMYstODmQPFvQGDcTX46WvpBzClEzOTJzuyeXMktGOck3wo-Mbz8JBMPS37K-NONd99DFbRN2WNxLKsYqTIhNxKeeujWYrd9QMIvBM0PZJCNHHAKwI77YvjCymC3iSsEGMjoysMAAtuyw__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)

### チェス版コピュラ

- 弱収束とチェス盤コピュラ https://www.sciencedirect.com/science/article/pii/S0047259X17301896
- **Testing Symmetry for Bivariate Copulas using Bernstein Polynomials**https://arxiv.org/pdf/2109.03694.pdf
- Empirical Bernstein copula. https://arxiv.org/pdf/2202.12787.pdf

### Archimedean Copula関連

- [Archimaxコピュラの推定](https://www.imstat.org/wp-content/uploads/2019/03/AOS1836.pdf)
- [多次元Archimedeanコピュラの推定](https://www.sciencedirect.com/science/article/pii/S0047259X12000607?ref=pdf_download&fr=RR-2&rr=7b297eb6fb0af699)
- [Sampling](https://www.uni-ulm.de/fileadmin/website_uni_ulm/mawi/forschung/PreprintServer/2007/preprintmariushofert.pdf)
- semiparametric Archimedean https://orbi.uliege.be/bitstream/2268/24473/1/VandenhendeLambert2005.pdf
- まとめスライド　[http://www.columbia.edu/~rf2283/Conference/2Models (1) Seagers.pdf](http://www.columbia.edu/~rf2283/Conference/2Models%20(1)%20Seagers.pdf)
- 

### Copula x DNN

- Deep archimedean copula https://arxiv.org/pdf/2012.03137.pdf
- Kammler https://arxiv.org/pdf/2301.08931.pdf
- Tactics https://arxiv.org/pdf/2202.03528.pdf
- **NN-Copula-CD: A Copula-Guided Interpretable Neural Network for Change Detection in Heterogeneous Remote Sensing Images** https://arxiv.org/pdf/2303.17448.pdf
- [Diffusion Copulas: Identification and Estimation](https://arxiv.org/pdf/2005.03513.pdf)
- [A copula-based method to build diffusion models with prescribed marginal and serial dependence](https://arxiv.org/pdf/1509.02319.pdf)
    - two diffusions are related by a monotone space-time transformation(STT) if and only if they share the same serial dependence
    - STTによってブラウン運動に変換. generatorの数でいくつかのクラス分類される.
- Copula GNN https://iclr.cc/virtual/2021/poster/2572 https://github.com/jiaqima/CopulaGNN
    - https://openreview.net/forum?id=XI-OJ5yyse
- ICLR 2018 [LEARNING SPARSE LATENT REPRESENTATIONS WITH THE DEEP COPULA INFORMATION BOTTLENECK](https://arxiv.org/pdf/1804.06216.pdf)
- **Copula Density Neural Estimation** https://arxiv.org/pdf/2211.15353.pdf

### ブラウン運動 x コピュラ

- https://www.sciencedirect.com/science/article/abs/pii/S0167715213001727
- https://arxiv.org/pdf/2004.10243.pdf

### サンプリング

- [local balanced proposal](https://math-info-4.slack.com/archives/D032VAJARBP/p1671669558921259)(Zanella2020)は[acceptanceが1となる](https://math-info-4.slack.com/archives/D032VAJARBP/p1672213692592949)が, proposalからのサンプルが簡単に取れない.
    - targetに似ていて, サンプルが簡単で, acceptance rateが上がる良い分布が必要？
    - exp(θ^T Hs(π)+Ht(π)) という形.
- 続編 [ICML2021](http://proceedings.mlr.press/v139/grathwohl21a/grathwohl21a.pdf) [ICLR2022](https://openreview.net/pdf?id=JSR-YDImK95) [離散HMC](https://arxiv.org/pdf/1705.08510.pdf#page123)
- [MCLMC](https://arxiv.org/pdf/2303.18221.pdf)

### 最適輸送

- https://arxiv.org/abs/2110.06798
    - Bedford2014より強い. L1収束まで言っている.
- 最適輸送ワークショップ
    - 最適輸送の情報幾何 https://link.springer.com/article/10.1007/s41884-023-00102-3
        - 量子化も考えられている
    - 量子コピュラ https://arxiv.org/pdf/1902.08460.pdf
    - 知識転移
        - ダイナミクスのダイナミクス. 忘却が発生
        - 内積で定義したタスク類似度ρが1/2以上なら汎化誤差が悪化する. なぜかはわからない.
        - 自然勾配法では逆行列の経験的な置き換えとかがうまくいっていたが理論とも整合
        - データセットの類似度と忘却の発生に相関があるという報告も
        - teacherとstudentのマッチングが同じ基底を持っていると汎化性能がよくなる
    - 拡散過程
        - 3Dレンダリングはまだできていない. 逆過程は本当の生成過程を再現しているわけではないから.
        - 条件付き生成, c1とc2を擬似的に独立だと思えばスコアが和になる. NNがいい感じに線型結合している. c1とc2が独立でない場合, 考える意味があるのかは不明.
        - 非平衡熱力学の行って帰ってくるパスに最適解では収束
        - textのencoderと画像モデルは別個.
        - メモリに乗らないところを, 区切って過程ごとにGPUに載せることができるようになったので, 1GPUで済んでいる
    - [NLPxOT](https://speakerdeck.com/eumesy/chatgpt-and-intro-of-ot-for-nlp?slide=46)
        - 最後に記載のある[GW距離](https://aclanthology.org/D18-1214.pdf)というのがshape spaceの定義に似ている.

### 時系列

- [カルマンフィルタと経済学](http://www2.econ.osaka-u.ac.jp/~tanizaki/class/kalman/kalman.pdf)
- [深層カルマンフィルタ](https://arxiv.org/pdf/1511.05121.pdf) [解説](https://deeplearning.jp/wp-content/uploads/2017/07/DL_hacks_20151225.pdf)
- Copula-based dynamic models for multivariate time series

### 金融応用分析

- 日銀
    - https://www.imes.boj.or.jp/research/papers/japanese/kk24-b2-3.pdf
    - https://www.imes.boj.or.jp/research/papers/japanese/kk29-3-4.pdf
