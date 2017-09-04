## List of protein structure prediction software
## 蛋白结构预测软件列表（来自维基百科）

From Wikipedia：https://en.wikipedia.org/wiki/List_of_protein_structure_prediction_software

该列表主要总结了常用的蛋白结构预测软件，包括同源建模法（homology modeling）、蛋白串线法（protein threading）、从头预测法（ab initio methods）、二级结构预测、跨膜螺旋和信号肽预测。

### 亮点软件
蛋白结构预测是一个广泛的问题，大致包括 1)从相似蛋白的信息进行结构预测（同源建模或基于模板的建模）；2)没有任何相似蛋白知识的辅助进行结构预测（从头结构预测或自由建模）。对这些预测的软件可以完全自动化或者需要哦一定人为干预。

来自华盛顿大学贝克实验室的Robetta是CASP12中顶级的同源建模服务器，是2017年6月3日之前在连续自动化模型评估测试服务器中表现最佳的服务器，至少自2014年（CAMEO）CAMEO以来排名第一。Robetta是多种生物信息学工具的十步管道。Robetta的扩展里包括Foldit，其旨在调查人脑固有模式识别和拼图解决能力，以创建更成功的计算机蛋白质结构预测软件。

根据2006-2016 CASP实验（CASP7-12），I-TASSER是免费建模蛋白质结构预测的最佳服务器。独立的I-TASSER软件包可免费下载。

HHpred是2010年CASP9实验中基于模板的蛋白质结构预测的主要服务器。它的反应时间的中位数是几分钟，而不是其他高性能服务器的数天时间。HHpred通常用于远程同源性检测和基于同源性的功能预测。它采用免费的开源软件包HH套件，用于快速序列搜索，蛋白质串线和远程同源性检测。

DNASTAR中的NovaFold是基于I-TASSER的蛋白结构预测软件。它利用I-TASSER算法，结合了串线和从头折叠技术，构建了具有未知结构蛋白的准确且完整的3D原子模型。NovaFold是本地和基于云的软件。

根据2010年CASP9实验，RaptorX擅长对齐困难靶标。与其他服务器（包括使用一致和细化方法的服务器）相比，RaptorX可以为最困难的50个CASP9基于模板的建模目标生成明显更好的对齐。RaptorX服务器在服务器上可用。

MODELLER是一种流行的软件工具，用于通过使用从NMR光谱数据处理得到的方法满足空间约束来生成同源模型。所述ModWeb比较的蛋白质结构建模的网络服务器主要使用MODELLER用于自动比较建模。

TIP是STRUCTFAST模型的知识库和序列，结构和结合位点之间的预计算相似关系。

BBSP（构建块结构预测器）是一种利用基于混合模板的方法的程序，其基于片段相似性将片段构象与序列相关联并检测远距离的折叠相似性。此外，这种程序由二级结构预测算法协调，命名为HCAM，主要基于亲水谱分析，并包含在BBSP工具套件中。

MOE（分子操作环境）是蛋白质和小分子建模和药物开发应用的平台，包括同源建模，以及针对不同蛋白质和抗体家族的定制，基于知识的程序，如GPCRs，激酶等。分析模拟或实验结构，并使其适用于药物开发。

### 同源建模（Homology modeling）
维基链接：https://en.wikipedia.org/wiki/Homology_modeling

#### 1.RaptorX ★
用于远程同源检测、蛋白3D建模、结合位点预测，具有自动化网站服务器和本地程序。

+ 链接：http://raptorx.uchicago.edu/

+ 简介：RaptorX是RAPTOR蛋白质结构预测系统的继承者。RAPTOR由滑铁卢大学徐金波博士和李明博士设计开发。RaptorX由位于芝加哥丰田技术研究所的徐金波教授领导的研究小组设计开发。RaptorX是用于非商业用途的蛋白质结构和功能预测的软件和Web服务器。RaptorX是蛋白质结构预测中最受欢迎的方法之一。像其他远程同源识别/蛋白质串线技术一样，当广泛使用的PSI-BLAST无效时，RaptorX能够产生可靠的蛋白质模型。然而，RaptorX也与基于谱的方法（例如，HHpred/HHsearch和Phyre/Phyre2）不同，因为RaptorX善于通过利用结构信息对没有大量序列同源物的蛋白质序列进行建模。RaptorX服务器的设计旨在确保对不熟悉蛋白结构预测方法的用户具有友好界面。
+ 使用方法：将蛋白质序列粘贴到RaptorX提交表单后，用户通常会等待几个小时（取决于序列长度）以进行预测。电子邮件将连同一个结果网页的链接发送给用户。RaptorX Server当前生成以下结果：3状态和8状态二级结构预测，序列模板对齐，3D结构预测，溶剂可及性预测，无序预测和结合位点预测。显示预测结果以支持肉眼检查。结果文件也可以下载。RaptorX服务器还产生一些置信度分数，表明预测的3D模型的质量（在没有相应天然结构的情况下）。例如，它为三维模型的全局质量产生P值，GDT（全局距离测试）和uGDT（非规范化GDT）用于三维模型的绝对全局质量和每个3D模型的每个位置的绝对局部质量的RMSD。
+ 应用和性能：RaptorX的应用包括蛋白质结构预测，功能预测，蛋白质序列-结构比对，蛋白质进化分类，引导定点突变和通过分子替代解决蛋白质晶体结构。在CASP9盲蛋白结构预测实验中，RaptorX在约80个自动结构预测服务器中排名第二。RaptorX还为50个最难的CASP9 TBM（基于模板的建模）目标生成了最佳对齐。在CASP 10中，RaptorX是15个最困难的CASP10 TBM目标中前10名人力/服务器组中唯一的服务器组。

#### 2. Biskit
将外部程序转换为自动化工作流程，如BLAST搜索、T-Coffee比对和MODELLER构建，链接：http://biskit.sf.net/

+ 简介：Biskit是由Python开发的开源软件包，该包辅助结构生物信息学和分子建模方面的研究。Biskit分为两个部分：1.用于操纵和分析大分子结构，蛋白质复合物和分子动力学轨迹的面向对象编程库；2. 建立一套解决具体任务的程序，例如通过同源建模自动预测蛋白质结构，或（通过灵活的蛋白质-蛋白质对接）来预测蛋白质复合物结构。Biskit库将许多计算委托给更专业的第三方程序，目前封装约15个外部应用程序，例如X-PLOR，Hex，T-Coffee，DSSP和MODELLER。最新版本2.4.3于2016年发布，项目正在积极发展。 Biskit最初是在巴斯德研究所开发的，名叫Biskit的是研究小组的名称：“生物信息学结构”。

#### 3. CABS
简化建模工具，是可下载的程序，链接：https://web.archive.org/web/20121009080857/http://www.biocomp.chem.uw.edu.pl/services.php

+ 简介：CABS是用于分子建模的多功能简化表示工具，包括：小蛋白的从头折叠，比较建模（特别是在差模板的情况下）和基于稀疏实验数据的结构预测。作为限制，可以使用实验约束，模板限制或理论上预测的约束（例如预测的侧链侧链接触）。该模型的描述可以在最近的出版物中找到。分子力场参数可以在这里查看：https://web.archive.org/web/20121009080857/http://biocomp.chem.uw.edu.pl/parameters_of_the_cabs_model.php。完整的包，包括CABS程序的Linux可执行文件，强制字段数据，示例输入和输出文件可以通过以下链接下载为tar.gz存档。
+ 下载：https://web.archive.org/web/20121009080857/http://biocomp.chem.uw.edu.pl/download.php?id=100


#### 4. CPHModel
片段装配，自动网络服务器，服务器地址：http://www.cbs.dtu.dk/services/CPHmodels/

+ 简介：CPHmodels 3.2是蛋白质同源建模服务器。模板识别基于由二级结构和暴露预测引导的轮廓-轮廓对准。CPHmodels-3.0是通过使用单一模板同源建模来预测蛋白质3D结构的网络服务器。服务器采用CPHmodels-2.0的评分功能和新颖的远程同源建模算法的混合。首先使用适用于密切同源性建模的快速CPHmodels-2.0概况文件评分函数对查询序列进行建模。新的计算代价高昂的远程同源建模算法只能在初始搜索中找到合适的PDB模板。 CPHmodels-3.0在CASP8比赛中被评为基准，并为94％的目标生产了模型（128个中有117个），74个被预测为高可靠性模型（117个中有87个）。当叠加到3D结构时这些平均RMSD为4.6？。其余26％的低可靠性模型（117个中的30个）可以叠加到真正的3D结构，平均RMSD为9.3？这些性能值将CPHmodels-3.0方法放置在高性能3D预测工具组中。除了它的准确性，该方法的重要特征之一是它的速度。对于大多数查询，服务器的响应时间少于20分钟。 Web服务器可从http://www.cbs.dtu.dk/services/CPHmodels/获取。

#### 5. ESyPred3D
模板检测，对齐，3D建模，是自动网络服务器，地址：http://www.fundp.ac.be/urbm/bioinfo/esypred/

+ 简介：ESyPred3D是一种自动同源建模程序。该方法获益于使用**神经网络**的对准策略而增加的对准性能。通过组合，加权和筛选多个对齐程序的结果来获得对齐。最终的三维结构使用建模包MODELLER构建。
+ 执行同源建模的通常四个步骤：1.搜索模板（已知结构的相似序列），2.对齐查询和模板序列，3.使用最后一个对齐方式和模板的结构构建3D模型，4.评估最终的3D模型。
+ 模板选择：模板是通过在NCBI nr数据库中使用最多四个PSI-BLAST迭代找到的第一个PDB命中。 + 序列比对：使用共有对准方法对查询和模板序列进行比对。使用不同对齐程序在两组序列上构建不同的多重序列比对，包括查询和模板序列。共识方法是使用神经网络找到最佳对齐残差并使用死端消除算法分析所有可能的组合。
+ 模型生成和循环建模：最终的3D模型是使用MODELLER从目标模板对齐和模板的3D结构构建的。 MODELLER也用于构建缺失的循环。
+ 模型评估：使用PROCHECK程序评估最终模型。
+ 用法：ESyPred3D已经在EVA，CASP和CAFASP中进行了评估。ESyPred3D是一些元服务器的一部分：Meta-PP，Genetegrate和PredictProtein。 ESyPred3D网络服务器每月运行约2600项预测。

#### 6. FOLD-X
用于能量计算和蛋白质设计，是可下载的程序，下载链接：http://foldx.crg.es/

+ 简介：FoldX是一种使用经验力场的蛋白质设计算法。它可以确定点突变的能量效应以及蛋白质复合物（包括蛋白质-DNA）的相互作用能。 FoldX可以使用基于概率的旋转异构体库突变蛋白质和DNA侧链，同时探索周围侧链的替代构象。
+ YASARA的FoldX插件是用于在YASARA中访问和运行FoldX命令的软件包。FoldX是一种分子建模和蛋白质设计软件程序，用于计算接近实验值的能量差异。 FoldX可以最小化PDB结构，将一个或多个残基突变成新的残基，进行蛋白质稳定性分析，蛋白质-蛋白质相互作用能量分析等等。 FoldX广泛用于预测突变对蛋白质稳定性的影响或预测蛋白质-蛋白质结合的影响。 YASARA是一个分子图形，模型和模拟程序，最终使您很容易回答您的生物问题。 3D图形和直观的界面使它成为一个非常用户友好的蛋白质和核酸分析包。它也可以通过插件轻松扩展。 FoldX通常从没有图形的命令行运行。通过安装YASARA的FoldX插件，您可以在3D图形YASARA界面中轻触按钮，访问最重要的FoldX工具。您可以直接在屏幕上查看您的FoldX蛋白质分析结果。用于YASARA的FoldX，YASARA和FoldX插件都可用于Linux，MacOSX和Windows。
本网站是通过安装和使用YASARA的FoldX插件的指南。
玩的开心！
+ 应用：预测点突变或人类SNP对蛋白质稳定性或蛋白质复合物的影响；蛋白质设计以改善稳定性或修饰亲和力或特异性；同源性建模。
+ 主要特点：RepairPDB：蛋白质结构的能量最小化；BuildModel：使用预测的能量变化在计算机中进行诱变或同源建模;AnalyseComplex：相互作用能量计算；Stability：预测替代结构之间的自由能变化；AlaScan：使用预测的能量变化在计算机中对蛋白质结构的丙氨酸进行扫描；SequenceDetail：每个残基自由能分解成分离的能量项（氢键，范德华力，静电，...）
+ 用户界面：Native FoldX从命令行运行。已经开发了YASARA分子图形程序的FoldX插件，用于在图形环境中访问各种FoldX工具。例如，可以直接在屏幕上分析使用FoldX进行计算机突变或同源建模。链接：http://foldxyasara.switchlab.org/index.php/Main_Page

#### 7.GeneSilico
用于共识模板搜索/片段装配，是网络服务器形式，服务器地址：http://www.genesilico.pl/meta/

+ 简介：GeneSilico是蛋白质结构预测的各种方法的门户。如果您提交单个蛋白质序列或多重序列比对（以下称为“目标”），则应获得以下预测：
1. 主要结构：由HmmPfam和HHSearchCDD识别的**结构域**
2. 二级结构：螺旋/延伸/其他构象（H/E/-）sspro4，cdm，psipred，fdm，jnet，prof，gor，spine，sable，pssfinder，sspred，sspal，nnssp，ssp，netSurfP，SOPRANO
3. 跨膜螺旋：Phobius，MEMSAT3，TMpred，HMMTOP，DAS，MINNOU，OCTOPUS，TMHMM2.0
4. 无序区域：DisEMBL，RONN，IUPRED，POODLE-L，GLOBPLOT，DISPROT（VSL2），PrDOS，DISOPRED2，Spritz，disPRO，Pdisorder，Spritz，iPDA，POODLE-S（计算共识是CASP8获奖方法）
5. 二硫键：DiANNA，DISULFIND，DBCP和DIpro2.0
6. 蛋白质中的核酸结合残基：BindN，BindN +，DISIS，DP-Bind，PPRInt和我们的RNA结合残基的meta预测因子（cons3best）。
7. Pcons共识服务器将评估FR对齐方式在多大程度上彼此一致，并且可以选择特定折叠
8. 从FR对齐，您可以自动生成粗略的三维模型（无变量循环）。您还可以选择属于特定折叠的对齐子集，并将其提交给我们的FRankenstein服务器，该服务器会将粗略模型拼接并重新组合，以生成一个可爱的小怪物蛋白质模型，希望类似于真实的结构。
9. 由我们的服务器生成的模型由COLORADO3D打分。使用RASMOL中的“color by temperature factor”选项来显示可能是正确的区域（蓝色）和可能是错误的区域（红色）。请记住，所有理论模型必须持保留态度- 即使是最信任的也应该被验证。

#### 8.Geno3D
满足空间限制，是自动网络服务器，地址：http://geno3d-pbil.ibcp.fr/

+ 简介：Geno3D服务器的目的是使所有生物化学家和生物学家能够访问自动蛋白质建模Web服务器来生成蛋白质3D模型。该服务器可用，希望它将是有用的，整个服务器的质量和性能的风险是与你在一起。结果只是一个模型，必须仔细考虑，它不是一个实验3D结构！Geno3D中使用的策略是通过空间约束（距离和二面体）满意度的比较蛋白质结构建模。Geno3D最常用于同源性或比较蛋白质结构建模：用户提供序列进行建模（查询），其被使用PSI-BLAST方法针对来自PDB的蛋白质序列数据库问题（默认情况下为所有条目）;用户选择PDB条目作为分子建模的模板; 对于每个模板，Geno3D服务器计算二级结构预测，显示二级结构中的协议百分比，从查询序列模板重新分配信息。在选择多模板的情况下，还会显示碳alpha模板之间的rmsd（均方根偏差）.

#### 9.HHpred
用于模板检测，对齐，3D建模，是具有帮助的互动网络服务器，地址：http://toolkit.tuebingen.mpg.de/hhpred

+ 简介：HHsearch是蛋白质序列搜索的开源软件程序，是免费的HH套件软件包的一部分。HHpred是一种免费的蛋白质功能和蛋白质结构预测服务器，基于HHsearch和HHblits，HH套件包中的另一个程序。 HHpred和HHsearch是蛋白质结构预测和远程相关序列检测中最受欢迎的方法之一，每个被引用超过500次。HHpred和HHsearch属于配置文件比较工具类，其中包括迄今为止最敏感的序列搜索方法。
+ 应用：HHpred和HHsearch的应用包括蛋白质结构预测，复杂结构预测，功能预测，域预测，域边界预测和蛋白质进化分类。在CASP7,8和9中，HHpred服务器已被列为最佳服务器，用于盲蛋白结构预测实验。在CASP9中，HHpredA，B和C分别在81个参与自动结构预测服务器中的第1位，第2位和第3位，在基于模板的建模中位列第6，第7，第8，所有147个目标上，而快于最好的20台服务器。在CASP8中，HHpred在所有目标上排名第七，在单一域蛋白亚组中排名第二，但仍高于顶级服务器的五十倍。

#### 10.Homology Modeling Professional for HyperChem
用于模板检测，对齐，二次结构预测，3D建模，从头循环建模，基于能量的侧链旋转异构体预测等，提供独立Windows可执行文件；地址：http://www.molfunction.com/software1.htm

+ 简介：HyperChem的同源性建模是最新的分子建模软件包，可以使用全面的量子化学计算和分子动力学模拟以及分子力学计算来进行大分子系统的分子建模，功能分析和模拟。程序包可用于在存在或不存在小分子，水分子，其他生物分子，金属原子和在真空或各种溶剂化条件下与模型共价结合的小分子的情况下进行蛋白质同源建模。该软件包还提供了几个建模，模拟和分析功能。蛋白质同源性建模只能使用三个模块程序来优化主链，侧链和整个分子系统的结构。由于这些模块程序可以自动运行，所以可以在几乎完全自动的条件下精确地执行同源建模。

#### 11.LOMETS
是本地Meta串线服务器，元服务器组合9个不同的程序。地址：http://zhanglab.ccmb.med.umich.edu/LOMETS/

+ 简介：LOMETS（Local Meta-Threading-Server）是蛋白质结构预测的在线Web服务。它通过从9个本地安装的线程程序（FFAS-3D，HHsearch，MUSTER，pGenTHREADER，PPAS，PRC，PROSPECT2，SP3和SPARKS-X）收集高得分的目标对模板对齐来生成3D模型。LOMETS的输出包括（参见说明性示例）：通过置信度分数从160个模型中选择的最佳10个串线模型；单个线程服务器的前10个目标模板对齐；空间C-α和侧链接触和距离图的预测；由共识约束指导的MODEMER建立的全长模型。

+ LOMETS包含于I-TASSER Suite

#### 12.MODELLER
满足空间限制，具有网络服务器和独立程序。服务器地址：http://salilab.org/modweb/ 下载地址：http://salilab.org/modeller/

+ 简介：MODELLER是用于同源建模以产生蛋白质三级结构和四级结构模型的计算机程序。它实现了一种来自蛋白质的核磁共振光谱（蛋白质NMR）的方法，称为空间约束的满足，通过该方法，使用一组几何标准来创建蛋白质中每个原子的位置的概率密度函数。该方法依赖于待建模的目标氨基酸序列与结构已被解决的模板蛋白之间的输入序列比对。该程序还包含蛋白质loop区域的从头结构预测的有限功能，即使在同源蛋白质中，这些区域通常也是高度可变的，因此难以通过同源建模进行预测。
+ 用于蛋白质三维结构的同源性或比较建模。用户提供要与已知相关结构建模的序列的对齐，MODELLER自动计算包含所有非氢原子的模型。MODELLER通过满足空间约束（3,4）来实现比较蛋白质结构建模，并且可以执行许多其他任务，包括蛋白质结构中循环的从头建模，针对灵活定义的目标函数优化各种蛋白质结构模型，蛋白质序列和/或结构的多重比对，聚类，序列数据库的搜索，蛋白质结构的比较等。MODELLER 可供大多数Unix / Linux系统，Windows和Mac下载。
+ Modeller最初是由旧金山加利福尼亚大学的Andrej Sali负责维护的。它运行在操作系统Unix，Linux，macOS和Windows上。它是免费的学术用途。图形用户界面（GUI）和商业版本由Accelrys分发。 ModWeb比较蛋白质结构模型Web服务器基于Modeller和其他自动蛋白质结构建模工具，可以将结果模型存入ModBase。由于Modeller的受欢迎程度，MODELLER提供了几款第三方GUI：1.EasyModeller是免费软件，是模板器最早的第三方GUI之一最新版本（EasyModeller 4.0）支持Linux和Windows操作系统；2.UCSF Chimera与Modeller有着简单的界面；3.PyMod是一款适用于PyMOL的免费开放源代码插件，具有全面的Modeller界面。它支持Linux，Windows和macOS。4.MaxMod是Windows上的MODELLER的独立GUI。
