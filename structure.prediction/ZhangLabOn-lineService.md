## 张实验室在线服务系统
来自：https://zhanglab.ccmb.med.umich.edu/services/

====================================================

+ [在线服务](https://zhanglab.ccmb.med.umich.edu/services/#Server) - 折叠、对接、设计和结构域等，其中一些可以下载；
+ [生物信息学工具](https://zhanglab.ccmb.med.umich.edu/services/#Tool) - 比对、成像和聚类等，所有都可以下载；
+ [数据库](https://zhanglab.ccmb.med.umich.edu/services/#Database) - 配体、GPCR、基因组、decoy、potential和CASP等，所有都可以下载。

### I.蛋白质结构和功能预测服务（折叠，串线，潜能，接触，扭转，对接等）

#### 1. I-TASSER ONLINE 蛋白结构与功能预测
链接：http://zhanglab.ccmb.med.umich.edu/I-TASSER

简介：I-TASSER服务器是蛋白质结构和功能预测的互联网服务。模型是基于LOMETS的多线程对齐和迭代TASSER模拟构建的。 I-TASSER（作为“张服务器”）在最近的CASP7和CASP8实验中被评为第1号服务器。服务器正在积极开发，目标是使用最先进的算法提供准确的结构和功能预测。

参考文献：

+ Ambrish Roy, Alper Kucukural, Yang Zhang. I-TASSER: a unified platform for automated protein structure and function prediction. Nature Protocols, vol 5, 725-738 (2010). 
+ Yang Zhang. I-TASSER server for protein 3D structure prediction. BMC Bioinformatics, vol 9, 40 (2008). (download the PDF file).

#### 2. QUARK ONLINE 从头蛋白结构预测
链接：http://zhanglab.ccmb.med.umich.edu/QUARK

+ 简介：QUARK是一种用于蛋白质折叠和蛋白质结构从头预测的计算机算法，其目的是从氨基酸序列构建正确的蛋白质3D模型。 QUARK模型通过在原子级知识型力场的指导下通过“复制-交换蒙特卡罗”模拟从小碎片（1-20个残基）构建。QUARK在CASP9的自由建模（FM）中排名第一。由于在QUARK仿真中没有使用全局模板信息，所以服务器适用于没有同源模板的蛋白质。

+ 参考文献：D. Xu, Y. Zhang, Ab initio protein structure assembly using continuous structure fragments and optimized knowledge-based force field. Proteins, 2012, 80: 1715-1735 

#### 3. LOMETS 蛋白折叠识别
链接：http://zhanglab.ccmb.med.umich.edu/LOMETS

+ 简介：LOMETS（Local Meta-Threading-Server）是本地安装的蛋白质结构预测的元服务器。它通过从9个本地安装的线程程序（FUGUE，HHsearch，PAINT，PPA-I，PPA-II，PROSPECT2，SAM-T02，SPARKS，SP3）中收集一致的目标对模板对齐来生成3D模型。

参考文献：

+ S. Wu, Y. Zhang. LOMETS: A local meta-threading-server for protein structure prediction. Nucleic Acids Research 2007; 35: 3375-3382

#### 4. COACH 蛋白-配体结合位点预测
链接：http://zhanglab.ccmb.med.umich.edu/COACH

+ 简介：COACH是蛋白质-配体结合位点预测的元服务器方法。从目标蛋白质的给定结构开始，COACH将使用两种比较方法TM-SITE和S-SITE生成补体配体结合位点预测，TM-SITE和S-SITE通过亚结构和结合特异性序列比对比较从BioLiP数据库识别配体结合模板。这些预测将与其他方法（包括COFACTOR，FINDSITE和ConCavity）的结果相结合，以产生最终的配体结合位点预测。用户还可以输入一级序列，其中I-TASSER将用于首先生成3D模型，然后将其馈送进入COACH管道进行配体结合位点预测。

参考文献：

+ Jianyi Yang, Ambrish Roy, and Yang Zhang. Protein-ligand binding site recognition using complementary binding-specific substructure comparison and sequence profile alignment, Bioinformatics, 29:2588-2595 (2013). 

#### 5.COFACTOR 基于结构的功能预测
链接：http://zhanglab.ccmb.med.umich.edu/COFACTOR

+ 简介：COFACTOR是一种基于蛋白质3D结构的蛋白质分子生物学功能注释自动化方法。当用户提供目标蛋白的结构模型时，COFACTOR将通过全局和局部结构比较将目标蛋白与三种综合蛋白质功能库中的已知蛋白质（模板）进行匹配。功能洞察，包括配体结合位点，基因本体术语和酶分类，然后从最高置信度得分（C评分）的最佳模板蛋白质获取而来。在社区范围的CASP9实验中，COFACTOR算法被列为配体结合位点预测的最佳方法。

参考文献：

+ Ambrish Roy, Jianyi Yang, and Yang Zhang. COFACTOR: An accurate comparative algorithm for structure-based protein function annotation. Nucleic Acids Research, 40:W471-W477 (2012)
+ Ambrish Roy, Yang Zhang. Recognizing protein-ligand binding sites by global structural alignment and local geometry refinement. Structure, 20: 987-997 (2012)

#### 6.MUSTER - Multi-source Protein Structure Threader
链接：http://zhanglab.ccmb.med.umich.edu/MUSTER

+ 简介：MUSTER（MUlti-Sources Threader）是一种新的蛋白质串线算法，用于从PDB库中识别模板结构。它通过将序列谱-谱比对与多个结构信息组合来生成序列-模板比对。

参考文献：
+ S. Wu, Y. Zhang. MUSTER: Improving protein sequence profile-profile alignments by using multiple sources of structure information. Proteins: Structure, Function, and Bioinformatics 2008; 72: 547-556.

#### 7.SEGMER
链接：http://zhanglab.ccmb.med.umich.edu/SEGMER

+ 简介：SEGMER是一种分段串线算法，用于从蛋白质数据库（PDB）库中识别子结构基序。它首先将靶序列分成由2-4个连续或非连续的二级结构元件（α-螺旋，β-链）组成的区段。然后将序列片段串过PDB以鉴定保守的亚结构。它通常识别比全链串线法更好的保守结构基序，特别是当PDB中没有类似的全局折叠时。

参考文献：
+ S. Wu, Y. Zhang. SEGMER:identifying protein sub-structural similarity by segmental threading. Structure, vol 18, 858-867 (2010). 

#### 8.FG-MD(Fragment-Guided MD simulation)
链接：http://zhanglab.ccmb.med.umich.edu/FG-MD

+ 简介：FG-MD是基于分子动力学（MD）的高分辨率蛋白质结构细化算法。给定初始蛋白质或蛋白质复合物3D模型（C-α或全原子），FG-MD首先通过结构校准程序TM-align从PDB识别类似的片段。然后使用从碎片提取的空间约束来指导分子动力学模拟。一般来说，FG-MD旨在改进更接近原生结构的初始模型。它还通过消除空间冲突并改善扭转角和氢键网络来改善结构的局部几何形状。

参考文献：

+ Jian Zhang, Yu Liang, Yang Zhang. Atomic-Level Protein Structure Refinement Using Fragment-Guided Molecular Dynamics Conformation Sampling. Structure, 19: 1784-1795, 2011

#### 9.ModRefiner 高分辨率蛋白结构精修
链接：http://zhanglab.ccmb.med.umich.edu/ModRefiner

+ 引言：ModRefiner是一种用于原子级，高分辨率蛋白质结构细化的算法。它可以从C-alpha跟踪，主链模型或全原子模型开始。在结构细化模拟期间，侧链和骨架原子都是完全柔性的，其中构象搜索由物理学和基于知识的力场的复合物引导。 ModRefiner有一个选项，允许分配第二个结构，这将被用作驱动细化模拟的参考。ModRefiner的一个目标是将最初的起始模型绘制到更靠近其自然状态。它也能显着改善局部结构的物理质量。

参考文献：

+ Dong Xu and Yang Zhang. Improving Physical Realism and Structural Accuracy of Protein Models by a Two-step Atomic-level Energy Minimization, Biophysical Journal, vol 101, 2525-2534 (2011)

#### 10.REMO 从C-α最早到全原子模型
链接：http://zhanglab.ccmb.med.umich.edu/REMO

+ 简介：REMO是通过优化骨架氢键网络，从C-α轨迹构建蛋白质原子结构的新算法。

参考文献：

+ Yunqi Li and Yang Zhang. REMO: A new protocol to refine full atomic protein models from C-alpha traces by optimizing hydrogen-bonding networks. Proteins, 2009, 76: 665-676.

#### 11.SPRing ON-LINE 蛋白质复杂结构的精确模板识别
链接：http://zhanglab.ccmb.med.umich.edu/spring

+ 简介：SPRING是蛋白质-蛋白质结构预测的基于模板的算法。它首先通过PDB库中的一条链蛋白质复合物，并从原始寡聚体条目中检索出结合片段。与另一个链相关联的复杂模型从预先计算的查找表中推导出来，其中由SPRING得分选出的最佳取向是由串线Z分数，界面接触和单体到二聚体模板。

参考文献：

+ Aysam Guerler, Brandon Govindarajoo and Yang Zhang. Mapping monomeric threading to protein-protein structure prediction, Journal of Chemical Information and Modeling 2013, 53: 717-725.

#### 12.COTH ON-LINE
链接：http://zhanglab.ccmb.med.umich.edu/COTH

+ 简介：COTH（CO-THreader）是一种多链蛋白串线算法，用于鉴定和重组来自三级和复杂结构文库的蛋白质复合物结构。它首先通过序列谱文件对齐生成复杂的查询模板对齐，序列谱比对由BSpred的结合位点从头预测协助。然后通过结构叠加将来自三级模板文库的单体结构合并到复合体框架中。

参考文献：

+ S Mukherjee, Y Zhang Protein-protein complex structure prediction by multimeric threading and template recombination. Structure, vol 19, 955-966 (2011) 

#### 13.BSpred
链接：http://zhanglab.ccmb.med.umich.edu/BSpred

+ 简介：BSpred是一种基于神经网络的算法，用于预测来自氨基酸序列的蛋白质的结合位点。该算法对基于序列的特征进行了广泛的训练，包括蛋白质序列分布，二级结构预测和氨基酸的疏水性量表。

参考文献：S Mukherjee, Y Zhang Protein-protein complex structure prediction by multimeric threading and template recombination. Structure, vol 19, 955-966 (2011)

#### 14.SVMSEQ 蛋白接触预测
链接：http://zhanglab.ccmb.med.umich.edu/SVMSEQ

简介：SVMSEQ是使用支持向量机进行蛋白质残留接触预测的新算法。

参考文献：S. Wu, Y. Zhang. A comprehensive assessment of sequence-based and template-based methods for protein contact prediction. Bioinformatics, vol 24, 924-931 (2008).

#### 15.ANGLOR
链接：http://zhanglab.ccmb.med.umich.edu/ANGLOR

简介：ANGLOR是一种基于机器学习的算法，用于从头开始预测蛋白质主链扭转角。对于给定的氨基酸序列，通过神经网络训练和支持向量机的组合来预测每个残差的实际值主干扭转角（phi和psi）。

参考文献：S. Wu, Y. Zhang. ANGLOR: A Composite Machine-Learning Algorithm for Protein Backbone Torsion Angle Prediction. PLoS ONE 2008; 3: e3400.

#### 16.BSP-SLIM ONLINE 预测结构的低分辨率对接
链接：http://zhanglab.ccmb.med.umich.edu/BSP-SLIM

简介：BSP-SLIM是低分辨率蛋白质结构的盲目分子对接方法。该方法首先通过结构匹配目标与模板全息结构来鉴定推定的配体结合位点。然后通过配体和结合中心的负像之间的局部形状和化学特征互补构建配体-蛋白质对接构象。

参考文献：Hui Sun Lee and Yang Zhang. BSP-SLIM: A blind low-resolution ligand-protein docking approach using theoretically predicted protein structures, Proteins, 2012, 80:93-110

#### 17.SAXSTER SAXS辅助的蛋白折叠识别
链接：http://zhanglab.ccmb.med.umich.edu/SAXSTER/

简介：SAXSTER是一种将小角度X射线散射（SAXS）数据和串线相结合的新算法，用于高分辨率蛋白质结构测定。给定一个查询序列，SAXSTER首先使用PDB库中的MUSTER串线程序生成一个模板对齐列表。然后，SAXS数据将用于基于SAXS配置文件匹配来优化最佳模板对齐，最终用于全长原子蛋白结构构建。

参考文献：M. dos Reis, R. Aparicio and Y. Zhang. Improving protein template recognition by using small angle X-ray scattering profiles. Biophysical Journal, vol 101, 2770-2781 (2011)

#### 18.ThreaDom ON-LINE 多重串线比对预测蛋白结构域边界
链接：http://zhanglab.ccmb.med.umich.edu/ThreaDom/

介绍：ThreaDom是蛋白质结构域边界预测的基于模板的算法。给定蛋白质序列，ThreaDom首先通过PDB文库对目标进行线性化，以鉴定具有相似结构折叠的蛋白质模板。然后基于目标和模板结构之间的多重序列比对来分配域边界，其中将每个预测分配置信度得分，该预测结合了来自模板结构、终端和内部间隙和插入的信息。ThreaDom旨在预测连续和不连续结构域域。

参考文献：Z Xue, D Xu, Y Wang, Y Zhang. ThreaDom: Assigning protein domain boundary using multiple threading alignments. Bioinformatics, 29: i247-i256, 2013.

#### 19.ThreaDomEx 预测蛋白结构域边界并检测不连续结构域
链接：http://zhanglab.ccmb.med.umich.edu/ThreaDomEx/

简介：ThreaDomEx是一种新版本的基于模板的结构域预测程序，扩展自ThreaDom。与ThreaDom程序相比，ThreaDomEx的主要新功能包括：（1）支持不连续域预测;（2）它允许手动干预域预测。

参考文献：Yan Wang, Jian Wang, Ruiming Li, Qiang Shi, Zhidong Xue, Yang Zhang. ThreaDomEx: a unified platform for predicting continuous and discontinuous protein domains by multiple-threading and segment assembly. Nucleic Acids Research, 45: W400-W407, (2017).

#### 20. EvoDesign On-line
链接：http://zhanglab.ccmb.med.umich.edu/EvoDesign/

简介：EvoDesign是基于进化谱的从头蛋白质设计方法。从目标蛋白质结构的支架开始，EvoDesign首先通过TM-align识别与PDB文库相似的蛋白质家族。然后从用于引导氨基酸序列空间的构象搜索的蛋白质模板构建结构特征，其中通过基于单序列的溶剂化，扭转角和二级结构预测来容纳的物理化学填充物。最终设计的序列通过聚类在设计模拟期间生成的所有序列诱饵来获得。

参考文献：Pralay Mitra, David Shultis and Yang Zhang. EvoDesign: de novo protein design based on structural and evolutionary profiles. Nucleic Acids Research, W273-W280, 2013.

#### 21.GPCR-I-TASSER GPCR的结构建模
链接：http://zhanglab.ccmb.med.umich.edu/GPCR-I-TASSER/

简介：GPCR-I-TASSER是专为预测G蛋白偶联受体的3D结构而设计的在线服务器系统。目标序列首先通过LOMETS的PDB libary进行线程，以搜索推定的模板。如果识别同源模板，则使用基于模板的片段组装过程来构建全长模型。在没有同源模板的情况下，使用从头开始的TM-螺旋折叠程序从头开始组装7-TM-螺旋束，随后GPCR-I-TASSER结构重组模拟辅助来自GPCR-RD。最终的结构模型通过片段指导的分子动力学（FG-MD）模拟在原子级进行改进。

参考文献：Jian Zhang, Jianyi Yang, Richard Jang, Yang Zhang. GPCR-I-TASSER: A hybrid approach to G protein-coupled receptor structure modeling and the application to the human genome. Structure, 23: 1538-1549 (2015).

#### 22.BindProf
链接：http://zhanglab.ccmb.med.umich.edu/BindProf/

简介：BindProf是一种用于预测界面残基突变时蛋白质-蛋白质结合相互作用的自由能变化（ΔΔG）的方法。虽然BindProf采用多尺度方法，该方法使用不同层次结构的分辨率的多源信息。BindProf的独特特征是从类似的蛋白质-蛋白质相互作用的多个结构校正而衍生的接口结构谱得分的夹杂。

参考文献：Jeffrey R. Brender, Yang Zhang. Predicting the Effect of Mutations on Protein-Protein Binding Interactions through Structure-Based Interface Profiles. PLOS Computational Biology, 11: e1004494 (2015).

#### 23.ResQ ONLINE 残基特异性质量和B因子的估计
链接：http://zhanglab.ccmb.med.umich.edu/ResQ/

简介：ResQ是基于模型模拟的局部变化和同源比对的不确定性来估计蛋白质结构预测中B因子和残基质量的方法。给定蛋白质结构模型，ResQ通过串线和结构比对技术从PDB识别一组同源和/或类似的模板。然后通过支持向量回归导出残差级建模误差，从最佳同源蛋白质的实验记录中推导出每个残基的B因子。

参考文献：Jianyi Yang, Yan Wang, Yang Zhang. ResQ: An approach to unified estimation of B-factor and residue-specific error in protein structure prediction. Journal of Molecular Biology, 428: 693-701 (2016).

#### 24.IonCom 离子配体结合位点预测
链接：http://zhanglab.ccmb.med.umich.edu/IonCom//

简介：IonCom是小配体（包括金属和酸根离子）结合位点预测的配体特异性方法。从查询蛋白质的给定序列或结构出发，IonCom执行复合结合位点预测，结合了从头训练和基于模板的转移。为了提高特异性和敏感性，本文重点研究了十三个最重要的小配体分子的结合位点预测，包括九种金属离子（Zn++，Cu+，Fe+，Fe++，Ca++，Mg++，Mn++，Na+，K+）和四种酸根离子CO3--，NO2-，SO4--，PO4---）。

参考文献：Xiuzhen Hu, Qiwen Dong, Jianyi Yang, Yang Zhang. Recognizing metal and acid radical ion binding sites by integrating ab initio modeling with template-based transferals. Boinformatics, 32: 3260-3269 (2016).

#### 25.STRUM 突变稳定性改变预测
链接：http://zhanglab.ccmb.med.umich.edu/STRUM/

简介：STRUM是一种用于预测蛋白质分子在单点nsSNP突变时的折叠稳定性变化（ΔΔG）的方法。STRUM采用梯度增强回归方程来训练不同级别的序列和结构特性上的各种特征上的吉布斯自由能变化。STRUM的独特特征是序列谱与蛋白质结构预测的低分辨率结构模型的结合，有助于提高该方法的稳健性和准确性，使其适用于各种蛋白质序列，包括没有实验结构的蛋白质序列。

参考文献：Lijun Quan, Qiang Lv, Yang Zhang. STRUM: Structure-based stability change prediction upon single-point mutation, Boinformatics, 32: 2936-46 (2016).

### II. 生物信息学工具（结构比对，序列比对，3D可视化，表面和聚类等）

#### 1.TM-score 蛋白结构的相似度
链接：http://zhanglab.ccmb.med.umich.edu/TM-score

简介：TM-score是计算两种蛋白质结构拓扑相似度的算法。它可以用于定量获取相对于天然的蛋白质结构预测的质量。由于TM-score衡量紧密匹配比远距离匹配更强，所以与常用的均方根偏差（RMSD）相比，TM-score对结构的全局拓扑结构更为敏感。

参考文献：Y. Zhang, J. Skolnick, Scoring function for automated assessment of protein structure template quality. Proteins, 2004 57: 702-710

#### 2.TM-align 快速精确的结构比对
链接：http://zhanglab.ccmb.med.umich.edu/TM-align

简介：TM-align是一种用于使用动态规划和TM-score旋转矩阵快速准确的蛋白质结构比对的计算机算法。每个比较将报告两种蛋白质之间的最佳比对以及TM-score。

参考文献：Y. Zhang, J. Skolnick, TM-align: A protein structure alignment algorithm based on TM-score. Nucleic Acids Research, 2005 33: 2302-2309

#### 3.MM-align 蛋白复杂结构比对
链接：http://zhanglab.ccmb.med.umich.edu/MM-align

简介：MM-align旨在使用基于TM-score旋转矩阵的动态规划的启发式迭代，结构上比对多聚体蛋白复合物。每个复合物中的多重链首先以各种可能的顺序连接，然后同时以交联链对准阻止进行比对。界面结构上的比对可以通过MM-align通过界面特定的加权因子来加强。据报道TM-score用于评估两种配合物的结构相似性。

参考文献：S. Mukherjee, Y. Zhang, MM-align: a quick algorithm for aligning multiple-chain protein complex structures using iterative dynamic programming. Nucleic Acids Research 2009; 37: e83

#### 4.NW-align
链接：http://zhanglab.ccmb.med.umich.edu/NW-align

简介：NW-align是基于标准Needleman-Wunsch动态规划算法的蛋白质序列比对的简单稳健的比对程序。突变基因来自BLOSUM62，间隙开放罚分=-11，间隙延伸罚分=-1。该程序的源代码可以在NW-align网站的底部下载，可以轻松修改为不同目的。

#### 5.EDTSurf
链接：http://zhanglab.ccmb.med.umich.edu/EDTSurf

简介：EDTSurf是一个用于构建大分子三角化表面的开源程序。它可以产生范德华表面，溶剂可及表面和分子表面（溶剂排除表面）的三个主要大分子表面，并且识别大分子内的空穴。

参考文献：Dong Xu, Yang Zhang (2009) Generating Triangulated Macromolecular Surfaces by Euclidean Distance Transform. PLoS ONE 4(12): e8140

#### 6.MVP
链接：http://zhanglab.ccmb.med.umich.edu/MVP

简介：MVP（Macromolecular Visualization and Processing）是大分子结构及其衍生信息可视化的便捷工具。它支持PDB格式和EM密度图，并具有许多绘图样式和颜色模式。它包含许多方便的特征，包括三角形表面的计算，深度，主轴和估计蛋白质结构的二级结构等。

参考文献：Dong Xu, Yang Zhang (2009) Generating Triangulated Macromolecular Surfaces by Euclidean Distance Transform. PLoS ONE 4(12): e8140. 

#### 7.MVP-Fit 
链接：http://zhanglab.ccmb.med.umich.edu/MVP-Fit

简介：MVP-Fit是将多个单体结构结合并适应EM密度图的工具。虽然大多数当前的工具只能实现对刚体对接和装配，但MVP-Fit具有将单体结构灵活移动和停靠在EM密度图中的优点，同时保持各个结构模型的物理和几何约束。

参考文献：Dong Xu, Yang Zhang, MVP-Fit: A Convenient Tool for Flexible Fitting of Protein Domain Structures with Cryo-Electron Microscopy Density Map. 

#### 8. SPICKER 近天然模型筛选
链接：http://zhanglab.ccmb.med.umich.edu/SPICKER

简介：SPICKER是一种聚类算法，用于从蛋白质结构诱饵池中识别近天然模型。集群由结构诱饵的成对RMSD度量定义。

参考文献：Y. Zhang, J. Skolnick, SPICKER: Approach to clustering protein structures for near-native model selection, Journal of Computational Chemistry, 2004 25: 865-871.

#### 9. HAAD 氢原子添加
链接：http://zhanglab.ccmb.med.umich.edu/HAAD

简介：HAAD是从蛋白质重原子结构构建氢原子的计算机算法。氢原子通过最小化原子重叠和促进氢键而加入。

参考文献：Yunqi Li, Roy Ambrish and Yang Zhang, HAAD: A Quick Algorithm for Accurate Prediction of Hydrogen Atoms in Protein Structures, PLoS One, 2009 4: e6701

#### 10.PSSpred
链接：http://zhanglab.ccmb.med.umich.edu/PSSpred

简介：PSSpred是一种用于准确蛋白质二级结构预测的多重神经训练算法。该程序可以免费下载。

#### 11.3DROBOT 蛋白结构诱饵生成器
链接：http://zhanglab.ccmb.med.umich.edu/3DRobot/

简介：3DRobot是一个程序，用于自动生成多样化、包装好的蛋白质结构诱饵。给定一个本地结构作为输入，3DRobot从PDB库识别不同的结构支架。然后进行无约束的片段重组模拟以构建不同的全长模型。最后的诱饵通过两步迭代能量最小化程序在原子级进一步改进，以改善结构的氢结合网络和空间重叠。3DRobot旨在提供高质量的蛋白质结构诱饵，用于设计和培养蛋白质折叠力场和折叠模拟方法。

参考文献：Haiyou Deng, Ya Jia, Yang Zhang. 3DRobot: Automated Generation of Diverse and Well-packed Protein Structure Decoys. Boinformatics, 32: 378-87 (2016).

#### 12.I-TASSER-MR
链接：http://zhanglab.ccmb.med.umich.edu/I-TASSER-MR/

简介：I-TASSER-MR是通过结合I-TASSER和分子置换（MR）来确定蛋白质结构的管道。从氨基酸序列和X射线衍射数据开始，首先通过迭代穿线组件细化模拟（I-TASSER）构建3D模型。然后通过逐步截断不可靠的建模区域的迭代编辑程序，通过分子置换确定X射线衍射的相位信息。最后，使用Phenix.autobuild程序构建原子模型。

参考文献：
+ Y. Wang, J. Virtanen, Z. Xue, J. J. G. Tesmer and Y. Zhang. Using iterative fragment assembly and progressive sequence truncation to facilitate phasing and crystal structure determination of distantly related proteins. Acta Cryst. (2016). D72, 616-628
+ Yan Wang, Jouko Virtanen, Zhidong Xue, Yang Zhang. I-TASSER-MR: automated molecular replacement for distant-homology proteins using iterative fragment assembly and progressive sequence truncation. Nucleic Acids Research, 45: W429-W434 (2017).

#### 13.NeBcon 蛋白接触图的精确预测
链接：http://zhanglab.ccmb.med.umich.edu/NeBcon/

介绍：NeBcon（基于神经网络和贝叶斯分类器的接触预测）是基于序列的蛋白质接触图预测的分层算法。它首先使用朴素贝叶斯分类器定理来计算八个机器学习和共同演化的接触产生程序（SVMSEQ，BETACON，SVMcon，PSICOV，CCMpred，FreeContact，MetaPSICOV和STRUCTCH）的后验概率。最后的接触图由神经网络机器创建，训练具有二级结构，溶剂可及性和多序列比对的香农熵的内在结构特征的后验概率分数。

参考文献：Baoji He, S. M. Mortuza, Yanting Wang, Hong-Bin Shen, Yang Zhang. NeBcon: Protein contact map prediction using neural network training coupled with naïve Bayes classifiers. Bioinformatics, : doi: 10.1093/bioinformatics/btx164 (2017).

### III. 数据库和电位

#### 1.BioLiP 配体-蛋白结合数据库
链接：http://zhanglab.ccmb.med.umich.edu/BioLiP

简介：BioLiP是一个手工策划的数据库，用于高质量，生物相关的配体-蛋白结合相互作用。数据主要从蛋白质数据库（PDB）收集，从文献和其他特定数据库挖掘的生物学见解，然后进行计算和手动验证。

参考文献：Jianyi Yang, Ambrish Roy, and Yang Zhang. BioLiP: a semi-manually curated database for biologically relevant ligand-protein interactions, Nucleic Acids Research, 41:D1096-D1103, 2013.

#### 2.Genome-Wide Structure & Function Modeling for E. coli
链接：http://zhanglab.ccmb.med.umich.edu/Ecoli

简介：这是一个关于大肠杆菌细菌整个基因组蛋白质结构、功能和相互作用网络建模的数据库。序列的3D结构由I-TASSER和QUARK生成，并由Spring模拟的相互关系的结构。

参考文献：
+ Dong Xu, Yang Zhang. Ab Initio Structure Prediction for Escherichia coli: Towards Genome-wide Protein Structure Modeling and Fold Assignment. Scientific Reports, 3: 1895 (2013).
+ Aysam Guerler, Elisa Warner and Yang Zhang. Genome-wide prediction and structural modeling of protein-protein interactions in Escherichia coli. 2013, submitted.

#### 3.GLASS
链接：http://zhanglab.ccmb.med.umich.edu/GLASS

简介：GLASS（GPCR-Ligand Association）数据库是经过实验验证的GPCR-配体相互作用的手动储存库。随着相关的GPCR和化学信息，从文献和公共数据库中提取GPCR-配体关联数据并将其整合到GLASS中。

参考文献：WK Chan, H Zhang, J Yang, JR Brender, Y Zhang. GLASS: A comprehensive database for experimentally-validated GPCR-ligand associations. Bioinformatics, 31: 3035-3042 (2015).

#### 4.GPCR-HGmod
链接：http://zhanglab.ccmb.med.umich.edu/GPCR-HGmod

简介：GPCR-HGmod是通过GPCR-I-TASSER方法产生的人类基因组中所有G蛋白偶联受体（GPCR）的3D结构模型的数据库。由于模型对模板库的敏感性，如果解决了新的GPCR实验结构，数据库将每六个月更新一次。

参考文献：Jian Zhang, Jianyi Yang, Richard Jang, Yang Zhang GPCR-I-TASSER: A hybrid approach to G protein-coupled receptor structure modeling and the application to the human genome. Structure, 23: 1538-1549 (2015). 

#### 5.GCPR-RD
链接：http://zhanglab.ccmb.med.umich.edu/GPCR-RD

简介：GPCR-RD是从文献和实验报告中系统收集的G蛋白偶联受体（GPCRs）的实验性约束的基础数据库。它包含数千个空间约束从诱变，二硫化物映射距离，电子冷冻显微镜和FTIR实验。数据可以方便地用于协助GPCR结构预测和功能注释。

参考文献：J Zhang, Y Zhang, GPCRRD: G protein-coupled receptor spatial restraint database for 3-D structure modeling and function annotation Bioinformatics, 2010,26(23):3004-3005.

#### 6.GPCR-EXP
链接：http://zhanglab.ccmb.med.umich.edu/GPCR-EXP

简介：GPCR-EXP是手工策划的数据库，包含已经解决的所有G蛋白偶联受体。数据库每周更新一次。每个条目包含与GPCR相关的PDB ID，分辨率，发布日期，生物名称和文献的信息。

参考文献：Jianyi Yang and Yang Zhang. GPCR-EXP: a manually curated database for experimentally solved GPCR structures, 2014

#### 7.TM-Fold ONLINE
链接：http://zhanglab.ccmb.med.umich.edu/TM-fold

简介：TM-fold是一种在线服务器，用于估计属于同一家族的两种蛋白质结构的后验可能性。对于给定的一对蛋白质结构，该服务器是通过结构比对算法计算结构相似性，并报告属于同一SCOP/CATH折叠系列的结构的后验概率。

参考文献：J Xu, Y Zhang, How significant is a protein structure similarity with TM-score=0.5? Bioinformatics, 2010, doi:10.1093

#### 8.Protein Structure Decoys
链接：http://zhanglab.ccmb.med.umich.edu/decoys

简介：此数据集包含由ab initio I-TASSER模拟生成的两组结构诱饵。第一组包含I-TASSER对56种小蛋白质的原始诱饵。第二组包括相同的56个蛋白质的非冗余结构诱饵，其中模型通过快速分子动力学模拟而改进。

参考文献：
+ Sitao Wu, Jeffrey Skolnick, Yang Zhang: Ab initio modeling of small proteins by iterative TASSER simulations. BMC Biology 2007, 5: 17.
+ J Zhang and Y Zhang, A Distance-Dependent Atomic Potential Derived from Random-Walk Ideal Chain Reference State for Protein Fold Selection and Structure Prediction. PLoS One, vol 5, e15386 (2010).

#### 9.potential I-TASSER Force Field
链接：http://zhanglab.ccmb.med.umich.edu/potential

简介：I-TASSER使用的交互参数和知识型力场。

参考文献：
+ Yang Zhang, Andrzej Kolinski, Jeffrey Skolnick. Touchstone II: A new approach to ab initio protein Structure Prediction. Biophysical Journal, vol 85, 1145 (2003). 

+ Sitao Wu, Jeffrey Skolnick, Yang Zhang. Ab initio modeling of small proteins by iterative TASSER simulations BMC Biology, vol 5, 17 (2007).

#### 10.RW potential
链接：http://zhanglab.ccmb.med.umich.edu/RW

介绍：RW是蛋白质结构建模和结构诱饵识别的距离相关原子势。它是使用理想的随机游动链作为参考状态的1383个高分辨率PDB结构计算的。

参考文献：J Zhang and Y Zhang, A Distance-Dependent Atomic Potential Derived from Random-Walk Ideal Chain Reference State for Protein Fold Selection and Structure Prediction. PLoS One, vol 5, e15386 (2010)

#### 11.HPSF
链接：http://zhanglab.ccmb.med.umich.edu/HPSF

简介：HPSF（人类蛋白质组学结构和功能）是人类蛋白质组“缺失蛋白质”的结构和功能注释数据库。首先从neXtProt数据库中提取尚未在蛋白质级验证的缺失的蛋白质。然后，结构折叠模拟由I-TASSER生成，所有同源模板从串线库中排除。最后，每个蛋白质的功能分析由基于结构的功能注释工具COFACTOR提供。

参考文献：Qiwen Dong, Rajasree Menon, Gilbert S. Omenn, Yang Zhang. Structural Bioinformatics Inspection of neXtProt PE5 Proteins in the Human Proteome. Journal of Proteome Research, 14: 3750-3761 (2015) 

#### 12.An automated assessment of protein structure predictions for CASP Experiment
链接：
+ http://zhanglab.ccmb.med.umich.edu/casp7
+ http://zhanglab.ccmb.med.umich.edu/casp8
+ http://zhanglab.ccmb.med.umich.edu/casp9
+ http://zhanglab.ccmb.med.umich.edu/casp10
+ http://zhanglab.ccmb.med.umich.edu/casp11
