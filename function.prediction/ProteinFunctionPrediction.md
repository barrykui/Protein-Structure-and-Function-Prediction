## 蛋白质功能预测
来自维基百科：https://en.wikipedia.org/wiki/Protein_function_prediction

蛋白质功能预测（Protein Function Prediction）方法是生物信息学研究者将生物或生物化学作用分配给蛋白质的技术。这些蛋白质通常是基于基因组序列预测或数据研究不足的蛋白质。这些预测通常由数据密集型计算程序驱动。信息可能来自核酸序列同源性，基因表达谱，蛋白质结构域，出版物的文本挖掘，系统发育谱，表型谱和蛋白质-蛋白质相互作用。蛋白质功能是一个广泛的术语：蛋白质的作用范围从催化生化反应到信号转导，单个蛋白质可能在多个过程或细胞途径中起作用。

一般来说，功能可以被认为是“通过蛋白质发生的任何事物”。基因本体联盟（Gene Ontology Consortium）提供了一个有用的功能分类，基于明确定义术语的词典，分为三个主要类别：分子功能、生物过程和细胞成分。研究人员可以使用蛋白质名称或登录号查询该数据库，以根据计算或实验证据检索相关的基因本体（GO）术语或注释。

虽然诸如芯片分析，RNA干扰和酵母双杂交系统的技术可以用于蛋白质功能的实验证明，但测序技术的进步使得蛋白质可以被实验表征的速率比新的序列产生的速率远远要低。因此，新序列的注释主要是通过计算机方法的预测，因为这些类型的注释通常可以快速完成，并且许多基因或蛋白质可以一次完成。第一种这样的方法基于具有已知功能的同源蛋白（**基于同源性的功能预测**）来推断功能。基于内容和基于结构的方法的发展扩大了可以预测的信息，现在可以使用方法的组合来基于序列数据获得完整的细胞通路的描述。通过GO数据库使用的“证据代码”分析强调了基因功能的计算预测的重要性和普遍性：截至2010年，98％的注释列在代码IEA（从电子注释推断）的同时，只有0.6％基于实验证据。

### 1. 功能预测方法

#### 1.1 同源法 Homology-based methods
序列类似的蛋白质通常是同源的，因此具有相似的功能。因此，在新测序的基因组中的蛋白质通常使用其他基因组中相似蛋白质的序列进行注释。然而，密切相关的蛋白质并不总是具有相同的功能，例如，酵母Gal1和Gal3蛋白是具有非常不同功能的旁系同源物（73％同一性和92％相似性），Gal1是半乳糖激酶，Gal3是转录诱导物。“安全”功能预测没有严格的序列相似性阈值;许多几乎不可检测的序列相似性的蛋白质具有相同的功能，而其他（例如Gal1和Gal3）的蛋白质具有高度相似性，但具有不同的功能。

#### 1.2 序列基序法 Sequence motif-based methods
蛋白质结构域数据库，如Pfam（Protein Families Database）的发展使我们能够在查询序列中找到已知的域，为可能的功能提供证据。[dcGO网站](http://supfam.org/SUPERFAMILY/dcGO/)包含对各个结构域和结构超域的注释（即两个或多个连续域的组合），因此通过dcGO Predictor允许以更真实的方式进行功能预测。在蛋白质结构域内，称为“基序”的短签名与特定功能相关和基序数据库如[PROSITE](http://prosite.expasy.org/)（“蛋白质结构域，家族和功能位点数据库”）可以使用查询序列进行搜索。例如，基序可以用于预测蛋白质的亚细胞定位（在细胞中蛋白质在合成后进行输送）。短信号肽将某些蛋白质引导到特定位置，例如线粒体，并且存在用于预测蛋白质序列中这些信号的各种工具。例如，已经更新了几次SignalP。因此，可以预测蛋白质功能的方面，而不与其他全长同源蛋白质序列进行比较。

+ dcGO：dcGO是蛋白质结构域的综合本体数据库。作为本体资源，dcGO将开放生物医学本体从多种内容中集成，从功能信息如基因本体到其他酶和途径，从主要模型生物的表型信息到关于人类疾病和药物的信息。作为蛋白质域资源，dcGO包括对各个结构域域和结构超域（即两个或多个连续域的组合）的注释。dcGO背后有两个关键概念。第一个概念是用本体标记蛋白质结构域，例如用Gene Ontology进行标记。这就是为什么它被称为dcGO，以域为中心(domain-centric)的基因本体论。第二个概念是使用本体标记的蛋白质结构域来进行蛋白质功能预测。简单来说，第一个概念是关于如何创建dcGO资源，第二个概念是关于如何使用dcGO资源。最新dcGO的使用是从功能角度构建一个结构域网络，用于交叉本体比较，并结合生物树（sTOL）来提供功能和表型的系统发育背景。开源软件dcGOR是使用R编程语言开发的，以分析以域为中心的本体和注释。支持的分析包括：1.轻松访问广泛的本体及其以域为中心的注释;2.能够构建定制的本体和注释;3.基于域的富集分析和可视化;4.根据本体注释构建域（语义相似性）网络;5.使用随机游走算法估计联系（统计显着性）网络的显著性分析;6.高性能并行计算。积极发展的功能是：1.用于创建以结构域为中心的本体注释的算法和实现;2.输入蛋白质结构域的本体术语预测;3.使用最大似然/简约法重建祖先离散特性。

+ PROSITE：PROSITE是蛋白质数据库。它包括描述蛋白质家族，结构域和功能位点以及其中的氨基酸模式和谱。这些信息由瑞士生物信息学研究所的团队手工策划，并紧密地融入Swiss-Prot蛋白质注释中。PROSITE于1988年由Amos Bairoch创立。自2009年7月起，PROSITE，Swiss-Prot和Vital-IT团队的主管是Ioannis Xenarios。PROSITE的用途包括识别新发现的蛋白质的可能功能和已知蛋白质的分析已确定未确定的活性。经过充分研究的基因的性质可以迁移到生物相关的生物体，并且对于不同或不太了解的基因，可以从相似性预测生化功能。PROSITE提供蛋白质序列分析和基序检测的工具。它是ExPASy蛋白质组学分析服务器的一部分。数据库ProRule建立在PROSITE的域描述上。它提供有关功能或结构关键氨基酸的附加信息。这些规则包含有关生物有意义的残基的信息，如活性位点，底物-或辅因子-结合位点，翻译后修饰位点或二硫键，以帮助功能测定。这些可以根据PROSITE基序自动生成注释。

#### 1.3 结构法 Structure-based methods
因为蛋白质3D结构通常比其序列更加保守，结构相似性是两种或更多种蛋白质中类似功能的良好指标。目前已经开发了许多程序来筛选PDB中未知蛋白质结构，并报告类似的结构，例如，FATCAT，CE和DeepAlign。为了处理许多蛋白质序列没有解决结构的问题，还开发了一些功能预测服务器，如RaptorX，可以首先预测序列的3D模型，然后使用基于结构的方法根据预测的3D模型预测功能。在许多情况下，代替整个蛋白质结构，可以靶向表示活性位点或结合位点的特定基序的3D结构。由Mary Jo Ondrechen和学生开发的Structurally Aligned Local Sites of Activity（SALSA）方法利用单个氨基酸的计算化学性质来鉴定局部生物化学活性位点。已经开发了诸如[Catalytic Site Atlas](http://www.ebi.ac.uk/thornton-srv/databases/CSA/)的数据库，可以使用新的蛋白质序列来搜索以预测特定的功能位点。

#### 1.4 基于基因组内容的方法 Genomic context-based methods
蛋白质功能预测的许多新方法不是基于如上所述的序列或结构的比较，而是基于新型基因/蛋白质和已经具有注释的那些之间的一些类型的相关性。也称为系统发育学概况，这些基于基因组背景的方法是基于观察到两种或更多种在许多不同基因组中具有相同存在或不存在模式的蛋白质最可能具有功能性联系。而基于同源性的方法通常可用于鉴定蛋白质的分子功能，基于内容的方法可用于预测细胞功能或蛋白质作用的生物过程。例如，涉及相同信号转导途径的蛋白质可能共享所有物种的基因组背景。

+ 基因融合
当两个或更多个基因在一个生物体中编码两个或更多个蛋白质并且通过进化组合成为另一个生物体中的单个基因（或者基因裂变反之亦然）时，发生基因融合。例如，已经使用这个概念来搜索所有大肠杆菌蛋白质序列与其他基因组中的同源性，并发现超过6000对序列与另一个基因组中的单个蛋白质具有共享的同源性，表明每个对之间存在潜在的相互作用。因为每个蛋白质对中的两个序列是非同源的，所以不能使用基于同源性的方法来预测这些相互作用。

+ 共定位/共表达
在原核生物中，在基因组中位置上靠近在一起的基因通常通过进化保存在一起，并且倾向于编码相互作用或作为相同操纵子一部分的蛋白质。因此，染色体邻近也被称为基因相邻方法可用于预测蛋白质之间的功能相似性，至少在原核生物中。染色体接近度也被认为适用于选定真核生物基因组中的一些途径，进一步开发基因相邻方法对于研究真核生物中的蛋白质相互作用可能是有价值的。
涉及类似功能的基因也经常共转录，因此通常可以预测未评估的蛋白质与其共同表达的蛋白质具有相关功能。基于该方法开发的关联算法推定可用于分析大量的序列数据并鉴定具有与已知基因相似的表达模式的基因。通常，通过关联研究推定将一组候选基因（未知功能）与目标组（例如，已知与特定疾病相关的一组基因）进行比较，并且通过其候选可能性对候选基因进行排序目标群体基于数据。然而，根据最近的研究，有人提出这种分析存在一些问题。例如，由于许多蛋白质是多功能的，编码它们的基因可能属于几个目标群体。有人认为这样的基因更有可能通过关联研究推定被鉴定，因此预测不特定。随着RNA-seq数据的积累，能够估计可变剪接的同种型的表达谱，机器学习算法也被用于预测和鉴别异构体水平上的功能。这代表了功能预测的一个新兴研究领域，它将大规模异质基因组数据整合到推断异构体水平的功能。

#### 1.5 计算溶剂映射 Computational solvent mapping
![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Computational_solvent_mapping_of_AMA1_using_FTMAP.TIF/lossy-page1-750px-Computational_solvent_mapping_of_AMA1_using_FTMAP.TIF.jpg)

蛋白质功能预测中涉及的挑战之一是发现活性位点。某些活性部位未形成——基本上存在——直到蛋白质经历由小分子结合引起的构象变化。大多数蛋白质结构已经通过X射线晶体学确定，而这需要纯化的蛋白质晶体。因此，现有的结构模型通常是纯化的蛋白质，因此缺乏当蛋白质与小分子相互作用时产生的构象变化。

计算溶剂映射使用在蛋白质表面上计算“移动”的探针（有机小分子），搜索它们倾向于聚集的位点。通常应用多种不同的探针，目标是获得大量不同的蛋白质-探针构象。然后根据集群的平均自由能对所生成的集群进行排名。在计算地绘制多个探针之后，蛋白质的相对较多数量的簇形成的位点通常对应于蛋白质上的活性位点。

这种技术是1996年“湿实验室”工作的计算适应性。发现当蛋白质悬浮在不同溶剂中时，确定蛋白质的结构，然后将这些结构叠加在一起产生有机溶剂分子（即蛋白质悬浮在其中）通常聚集在蛋白质的活性位点。这项工作是为了实现在X射线晶体学产生的电子密度图中水分子是可见的。水分子与蛋白质相互作用，并且倾向于聚集在蛋白质的极性区域。这导致将纯化的蛋白质晶体浸入其它溶剂（例如乙醇，异丙醇等）中以确定这些分子簇聚在蛋白质上的想法。溶剂可以根据它们近似的方式来选择，也就是说，这种蛋白质可以与什么分子相互作用（例如，乙醇可以用于探测与氨基酸丝氨酸的相互作用，异丙醇是苏氨酸的探针等）。蛋白质晶体在每种溶剂中保持其三级结构是至关重要的。对于多种溶剂重复该过程，然后该数据可用于测定蛋白质上潜在的活性位点。十年后，这项技术发展成为Clodfelter等人的算法。

#### 1.6 基于网络的方法 Network-based methods
可以使用关联型算法推定来为给定的基因组或蛋白质组产生功能关联网络。这些网络作为一组基因中共享/相似功能的证据的表示，其中节点表示基因/蛋白质，并通过表示共享功能证据的边缘彼此链接。

+ 综合网络
基于不同数据源的几个网络可以组合成一个复合网络，然后可以通过预测算法来注释候选基因或蛋白质。例如，bioPIXIE系统的开发人员使用各种酿酒酵母基因组数据来生成该物种的复合功能网络。该资源允许表示生物过程的已知网络的可视化，以及这些网络的新组件的预测。已经开发了许多算法来基于几个数据源（例如基因组，蛋白质组学，蛋白质相互作用等）的整合来预测功能，并且对先前注释的基因的测试表明高水准的准确性。一些功能预测算法的缺点包括缺乏可访问性和分析所需的时间。近年来，开发了更快，更准确的算法，如[GeneMANIA](http://morrislab.med.utoronto.ca/prototype)（多关联网络集成算法），并在网络上公开，表明了功能预测的未来发展方向。
