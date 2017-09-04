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

#### 9.HHpred ★
用于模板检测，对齐，3D建模，是具有帮助的互动网络服务器，地址：http://toolkit.tuebingen.mpg.de/hhpred，下载地址：ftp://ftp.tuebingen.mpg.de/pub/protevo/HHsearch

+ 简介：HHsearch是蛋白质序列搜索的开源软件程序，是免费的HH套件软件包的一部分。HHpred是一种免费的蛋白质功能和蛋白质结构预测服务器，基于HHsearch和HHblits，HH套件包中的另一个程序。 HHpred和HHsearch是蛋白质结构预测和远程相关序列检测中最受欢迎的方法之一，每个被引用超过500次。HHpred和HHsearch属于配置文件比较工具类，其中包括迄今为止最敏感的序列搜索方法。
+ 应用：HHpred和HHsearch的应用包括蛋白质结构预测，复杂结构预测，功能预测，域预测，域边界预测和蛋白质进化分类。在CASP7,8和9中，HHpred服务器已被列为最佳服务器，用于盲蛋白结构预测实验。在CASP9中，HHpredA，B和C分别在81个参与自动结构预测服务器中的第1位，第2位和第3位，在基于模板的建模中位列第6，第7，第8，所有147个目标上，而快于最好的20台服务器。在CASP8中，HHpred在所有目标上排名第七，在单一域蛋白亚组中排名第二，但仍高于顶级服务器的五十倍。

#### 10.Homology Modeling Professional for HyperChem
用于模板检测，对齐，二次结构预测，3D建模，从头循环建模，基于能量的侧链旋转异构体预测等，提供独立Windows可执行文件；地址：http://www.molfunction.com/software1.htm

+ 简介：HyperChem的同源性建模是最新的分子建模软件包，可以使用全面的量子化学计算和分子动力学模拟以及分子力学计算来进行大分子系统的分子建模，功能分析和模拟。程序包可用于在存在或不存在小分子，水分子，其他生物分子，金属原子和在真空或各种溶剂化条件下与模型共价结合的小分子的情况下进行蛋白质同源建模。该软件包还提供了几个建模，模拟和分析功能。蛋白质同源性建模只能使用三个模块程序来优化主链，侧链和整个分子系统的结构。由于这些模块程序可以自动运行，所以可以在几乎完全自动的条件下精确地执行同源建模。

#### 11.LOMETS
是本地Meta串线服务器，元服务器组合9个不同的程序。地址：http://zhanglab.ccmb.med.umich.edu/LOMETS/

+ 简介：LOMETS（Local Meta-Threading-Server）是蛋白质结构预测的在线Web服务。它通过从9个本地安装的线程程序（FFAS-3D，HHsearch，MUSTER，pGenTHREADER，PPAS，PRC，PROSPECT2，SP3和SPARKS-X）收集高得分的目标对模板对齐来生成3D模型。LOMETS的输出包括（参见说明性示例）：通过置信度分数从160个模型中选择的最佳10个串线模型；单个线程服务器的前10个目标模板对齐；空间C-α和侧链接触和距离图的预测；由共识约束指导的MODEMER建立的全长模型。

+ LOMETS包含于I-TASSER Suite

#### 12.MODELLER ★
满足空间限制，具有网络服务器和独立程序。服务器地址：http://salilab.org/modweb/ 下载地址：http://salilab.org/modeller/

+ 简介：MODELLER是用于同源建模以产生蛋白质三级结构和四级结构模型的计算机程序。它实现了一种来自蛋白质的核磁共振光谱（蛋白质NMR）的方法，称为空间约束的满足，通过该方法，使用一组几何标准来创建蛋白质中每个原子的位置的概率密度函数。该方法依赖于待建模的目标氨基酸序列与结构已被解决的模板蛋白之间的输入序列比对。该程序还包含蛋白质loop区域的从头结构预测的有限功能，即使在同源蛋白质中，这些区域通常也是高度可变的，因此难以通过同源建模进行预测。
+ 用于蛋白质三维结构的同源性或比较建模。用户提供要与已知相关结构建模的序列的对齐，MODELLER自动计算包含所有非氢原子的模型。MODELLER通过满足空间约束（3,4）来实现比较蛋白质结构建模，并且可以执行许多其他任务，包括蛋白质结构中循环的从头建模，针对灵活定义的目标函数优化各种蛋白质结构模型，蛋白质序列和/或结构的多重比对，聚类，序列数据库的搜索，蛋白质结构的比较等。MODELLER 可供大多数Unix / Linux系统，Windows和Mac下载。
+ Modeller最初是由旧金山加利福尼亚大学的Andrej Sali负责维护的。它运行在操作系统Unix，Linux，macOS和Windows上。它是免费的学术用途。图形用户界面（GUI）和商业版本由Accelrys分发。 ModWeb比较蛋白质结构模型Web服务器基于Modeller和其他自动蛋白质结构建模工具，可以将结果模型存入ModBase。由于Modeller的受欢迎程度，MODELLER提供了几款第三方GUI：1.EasyModeller是免费软件，是模板器最早的第三方GUI之一最新版本（EasyModeller 4.0）支持Linux和Windows操作系统；2.UCSF Chimera与Modeller有着简单的界面；3.PyMod是一款适用于PyMOL的免费开放源代码插件，具有全面的Modeller界面。它支持Linux，Windows和macOS。4.MaxMod是Windows上的MODELLER的独立GUI。

#### 13.MOE (Molecular Operating Environment)
用于模板识别，多个模板的使用以及其他环境的考虑（例如排除的配体体积），循环建模，侧链构象的旋转异构体文库，使用MM力场的放松，多平台支持（Windows, Linux, Mac），网站：http://www.chemcomp.com/

+ 简介：分子操作环境（MOE）是一个将可视化，建模和模拟以及方法开发整合在一起的药物开发软件平台。 MOE科学应用由生物学家，药物化学家和计算化学家在制药，生物技术和学术研究中使用。 MOE在Windows，Linux，Unix和MAC OS X上运行。MOE的主要应用领域包括基于结构的设计，基于片段的设计，药效团研发，药物化学应用，生物制剂应用，蛋白质和抗体建模，分子建模和模拟，化学信息学和QSAR。科学矢量语言（SVL）是MOE的内置命令，脚本和应用程序开发语言。

#### 14.Phyre and Phyre2 ★
用于远程模板检测，比对，3D建模，多模板，从头开始预测，提供Web服务器，自动更新折叠库，基因组搜索等设施，服务器地址：http://www.sbg.bio.ic.ac.uk/~phyre/

+ 简介：Phyre和Phyre2（Protein Homology/AnalogY Recognition Engine; pronounced as 'fire'）是蛋白质结构预测的基于网络的服务，可用于非商业用途。Phyre是引用超过1500次的最受欢迎的蛋白质结构预测方法，像其他远程同源识别技术（见蛋白质线程）一样，当其他广泛使用的方法（如PSI-BLAST）不能时，能够生成可靠的蛋白质模型。 Phyre2已经设计以确保用户对蛋白质结构预测方法的用户友好界面。

+ 2005年6月发布了第一个Phyre服务器，并使用基于每个蛋白质位置特定评分矩阵的配置文件对齐算法。Phyre2服务器于2011年2月公开发布，作为原始Phyre服务器的替代品，并为Phyre提供了额外的功能，Phyre是一个更高级的界面，完全更新的折叠库，并使用HHpred/HHsearch软件包进行同源检测和其他改进。
+ 用法：将蛋白质氨基酸序列粘贴到Phyre或Phyre2提交表单中，用户通常将在30分钟至几小时之间等待（取决于诸如序列长度，同源序列数目，插入和缺失的频率和长度等因素）预测完成。包含摘要信息和PDB格式的预测结构的电子邮件将连同到结果网页的链接一起发送给用户。 Phyre2结果屏幕分为三个主要部分，如下所述：二级结构和紊乱预测、结构域分析、详细模板信息和比对查看。
+ Phyre和Phyre2的应用包括蛋白质结构预测，功能预测，域预测，域边界预测，蛋白质进化分类，引导定点诱变和通过分子置换解决蛋白质晶体结构。在CASP 8盲蛋白结构预测实验中，Phyre_de_novo（Phyre2的前身）在71个自动结构预测服务器中排名第4。在CASP 9中，Phyre2在所有基于模板的建模（TBM）目标中排名第5，在79个参与服务器中的更难的TBM/FM（自由建模）中排名第2。

#### 15. Prime ★
基于物理的能量函数，提供图形界面、序列比对、二级结构预测、同源建模、蛋白精细化、环预测和侧链预测，网址：https://www.schrodinger.com/prime

+ 简介：一个强大而创新的软件套装，用于精确进行蛋白质结构预测。1. 无与伦比的准确性：
Prime结合了改进的科学与新的方法和算法，以提供预测结构的最高精度。2.高级模拟：
Prime配体诱导的拟合分析在配体存在下改善活性位点的几何形状。诱导拟合建模模拟蛋白质靶标的灵活性，并确定不同配体化学型的替代结合模式。2.完全整合：Prime将同源建模和折叠识别纳入一个包装。比较建模用于产生准确的同源性模型进一步的基于结构的研究。线程和折叠识别技术用于在低序列或非序列身份的情况下创建用于早期结构调查或功能注释的骨干模型。3.易于使用的界面：Prime包括一个直观的逐步界面，通过为进程的每个阶段提供有用的默认设置，让新手用户完成结构预测的工作流程。同时，Prime允许专家用户指定和调整参数以优化预测的质量。Maestro界面提供了额外的结构和序列可视化和分析工具。

#### 16.ROBETTA  ★
用于同源建模和通过Ginzu域预测进行从头片段组装，提供网络服务器，地址：http://robetta.bakerlab.org/

+ 简介：Robetta提供了从头预测和蛋白质结构域的比较建模。没有可检测的PDB同源物的结构域用Rosetta从头方案进行建模。比较模型是使用HHSEARCH/HHpred，RaptorX和Sparks-X的本地安装版本检测和比对的模板PDB构建的。比对是集群的，使用RosettaCM协议生成比较模型。该程序是完全自动化的。 Robetta通过CAMEO（server11）不断评估。Robetta在盲目的基准测试实验CASP中被评估。Robetta使用由Rosetta Commons开发和维护的ROSETTA软件。 RCSB PDB更新后，星期三每周更新模板数据库。

+ 为防止不必要的使用，我们需要两个手动步骤进行全面的结构预测。第一步是提交您的域和模板检测的序列。第二步是继续使用3D模型。您一次只能选择一个域进行结构预测。第二步在计算上是昂贵的，所以如果需要，请继续这一步。您可以通过加入我们的分布式计算项目Rosetta@HOME来帮助增加这项服务的计算资源，并将其传播给朋友和同事。 
〜10分钟 - 数小时 进行域和模板检测。
〜1天 - 数周 用于高精度同源性模型（以高置信度检测的模板> 0.8且序列同一性> 40％）。
〜1个星期 - 几个月 困难目标。

#### 17.BHAGEERATH-H
从头折叠预测和同源法的结合，用于蛋白三级结构预测。网络服务器地址：http://www.scfbio-iitd.res.in/bhageerath/bhageerath_h.jsp

+ 简介：BHAGEERATH-H：蛋白质三级结构预测的同源异源混合网络服务器（2016年5月版）。“Bhageerath-H”接受氨基酸序列来预测5种候选结构。这里用户可以灵活地提供用于建模的参考PDB。方法已经在CASP12实验中进行了很多改进的版本。

+ Bhageerath：蛋白折叠的IIT Delhi途径。结合生物信息学工具和从头开始的方法，已经取得了相当大的进展，对于小蛋白质的三级结构预测来说，计算上是快速的。软件套件Bhageerath包括八个模块，可以独立运行或在管道中运行。与现有生物信息学工具的比较表明，本方法的性能令人满意和有用，特别是当数据库缺乏序列同系物时。 Alpha / Beta系统的初步工作取得了令人鼓舞的成果。目前，Bhageerathweb服务器对于具有两个二级结构（其间有一个环路）的系统的预期时间约为4-5分钟;而对于具有三个二级结构（其间有两个环路）的系统，在专用32处理器集群上为2-3小时。正在进行尝试将方法扩展到更大的系统，减少计算时间。

#### 18.Selvita Protein Modeling Platform（好像现在无法访问）
蛋白质建模工具包，提供免费演示，交互式Web服务器和独立程序，包括：BLAST搜索，CABS建模，3D线程，Psi-Pred二级结构预测，网站为http://www.selvita.com/selvita-protein-modeling-platform.html

+ 简介：SPMP 2.0为基于Web的界面中的蛋白质结构和交互建模提供了必要的工具，适用于初学者和专家用户的需求。
Selvita蛋白质建模平台基于CABS算法，由蛋白质结构建模领域世界知名专家Andrzej Kolinski教授创建 - 独特的CASP竞争技术（超过200个竞争对手的CASP6竞争中排名第一）新版本具有新的蛋白质-蛋白质/蛋白质肽对接模块，可用性增强和用户对发现结果的改进。 SPMP 2.0的主要特点包括：蛋白质-蛋白质/蛋白质-肽对接模块（前所未有的蛋白质主链柔性程度）。各种复杂程度的蛋白质结构预测（同源建模，折叠识别，从头折叠）；同源性使用单个或多个模板进行建模；BL​​AST序列比对和PSI-PRED二级结构预测；与现有方法相比，难以进行的同源建模和从头案例的优越预测能力；抗体抗原建模（循环建模与对接协议）的独特解决方案；与GROMACS集成 - 用于分子模拟的多功能和非常好的优化包；基于跨平台Web的GUI（仅需要启用Java的Web浏览器和Java运行时环境）；完全自动选择建模路由（或者：访问所有设置）SPMP是新手和大师的工具。；使用计算机模型结合使用稀疏实验数据（NMR）来提高模型精度的蛋白质结构预测的可能性。

#### 18.STRUCTUROPEDIA
MODELLER的网络界面，提供单体或多聚体形式的蛋白质与肽和DNA复合物的同源性建模，以及将突变和翻译后修饰（PTM）引入蛋白质结构中，网络服务地址：http://structuropedia.org/

#### 19.SWISS-MODEL ★
局部相似度/片段装配，提供自动网络服务器（基于ProModII），地址：http://swissmodel.expasy.org/。

+ 简介：SWISS-MODEL是一种完全自动化的蛋白质结构同源建模服务器，可通过ExPASy Web服务器或程序DeepView（Swiss Pdb-Viewer）访问。该服务器的目的是使蛋白质建模可以在世界各地的所有生物化学家和分子生物学家访问。

+ 帮助：SWISS-MODEL是一种基于网络的综合服务，致力于蛋白质结构同源建模。它引导用户构建不同复杂程度的蛋白质同源模型。构建同源模型包括四个主要步骤：（i）识别结构模板，（ii）目标序列和模板结构的比对，（iii）模型构建和（iv）模型质量评估。这些步骤需要专门的软件并集成最新的蛋白质序列和结构数据库。可以交互地重复上述步骤中的每一个，直到达到满意的建模结果。根据建模任务的难度，提供了三种不同类型的建模模式，其用户干预量有所不同：自动化模式，对齐模式和项目模式。

#### 20.TIP-STRUCTFAST
自动比较建模，提供网络服务器，地址：http://www.eidogen.com/structfast.php

+ 简介：STRUCTFAST是Eidogen-Sertanty的专有和正在申请专利的蛋白质结构确定算法。 STRUCTFAST是最好的比较建模算法，如2004年12月的CASP6蛋白质结构测定实验所证实的。对于比较建模目标，STRUCTFAST优于其他47台自动化服务器和124个手工建模团队中（5个例外）。

#### 21.WHAT IF
位置特定旋转异构体，提供独立程序和web界面，网址：https://web.archive.org/web/20130618170139/http://swift.cmbi.kun.nl/whatif/
http://swift.cmbi.ru.nl/servers/html/index.html

+ 简介：WHAT IF主页是一个多功能的分子建模包，专门从事蛋白质和其环境中的分子，如水，配体，核酸等。

#### 22.Yasara
模板检测，比对，建模包括配体和低聚物，模型片段的杂交，提供图形界面或文本模式（集群），地址：http://www.yasara.org/

+ 简介：YASARA是一款多功能分子模拟商业软件，可用于分子结构可视化，结构分析，分子动力学模拟，分子对接，同源模建，NMR数据预测蛋白质结构等。YASARA是分子可视化，建模和动力学的计算机程序。有很多科学用途，如大量的科学文章提到的软件。YASARA的免费版本非常适合生物信息学教育。有一系列免费的生物信息学课程，使用这个软件。YASARA是自1993年以来开发的Windows，Linux，Mac OS X和Android的分子图形，模拟和仿真程序，最终使您很容易回答您的问题。通过直观的用户界面，逼真的图形和支持经济实惠的快门眼镜，自动立体显示器和输入设备，YASARA创造了与“人造现实”的新水平的互动，让您专注于您的目标，并忘记了程序。 YASARA由PVL（便携式矢量语言）提供支持，PVL（便携式矢量语言）是提供高于传统软件的性能方法的新开发框架。 PVL允许您可视化甚至最大的蛋白质，并在标准PC上实现真正的交互式实时模拟，并使用GPU（见基准测试）。您可以推拉分子，并使用动态模型，而不是静态图片。扎根于学术界，YASARA介绍的所有方法都在同行评议的期刊中有所描述。您可以免费获得初始阶段“YASARA View”，而较高阶段（YASARA Model，YASARA Dynamics，YASARA Structure）需要许可费用，可以在未来保证新的开发，更新和支持，而不需要临时授权。

### 蛋白串线（折叠识别,Threading/fold recognition）
维基链接：https://en.wikipedia.org/wiki/Protein_threading

#### 1.RaptorX ★
远程模板检测、单模板和多模板串线、与旧程序RAPTOR完全不同且远远优于它；提供网络服务器和自动更新的折叠库，网址：http://raptorx.uchicago.edu/

+ 简介：见同源建模中的RaptorX条目。

#### 2.FALCON@home
单模板和多模板串线，基于志愿者计算的高吞吐量服务器，提供网络服务器，地址：http://protein.ict.ac.cn/FALCON

简介：FALCON @ home拥有超过20,000名志愿者CPU的计算能力，每天可处理超过1,000种蛋白质。FALCON @ home将查询蛋白质与保守区域比对，而不是直接使用全长模板。 这有助于避免基于高度可变区域的模糊对齐，从而改善远程同源识别。FALCON @ home易于使用。根据对准质量对鉴定的同源模板进行分类，并使用JMOL直观地可视化预测结构。

#### 3.HHpred
模板检测、比对和3D建模，提供交互式网络服务器，网址：https://toolkit.tuebingen.mpg.de/#/tools/hhpred
 + 简介：见同源建模中的HHpred条目。

 #### 4.NovaFold
 串线与从头预测折叠的结合，商业蛋白质结构预测应用，网址：http://www.dnastar.com/t-products-NovaFold.aspx
 
 + 简介：DNASTAR NovaFold是基于I-TASSER的蛋白质结构预测软件，该软件是密歇根大学张扬教授实验室开发的屡获殊荣的软件包。NovaFold利用由张教授开发的I-TASSER算法，结合了线程和从头式折叠技术，构建了具有先前未知结构的准确，完整的3D原子模型。使用NovaFold的蛋白质结构预测的混合方法来产生任何大小分子的高精度模型。该方法首先通过将它们与模板库进行比较来识别结构片段，然后将这些和不匹配的片段并入最终结构；预测配体结合位点和蛋白质功能；通过支持结构和序列比对来评估NovaFold预测质量。

 #### 5.I-TASSER ★
 从头折叠预测与串线法的结合，蛋白结构和功能预测，网址：http://zhanglab.ccmb.med.umich.edu/I-TASSER/，下载地址:http://zhanglab.ccmb.med.umich.edu/I-TASSER/download

 + 简介：I-TASSER（Iterative Threading ASSEmbly Refinement，迭代串线组装细化）是蛋白质结构和功能预测的分层方法。它首先通过多线程方法LOMETS从PDB中识别结构模板， 通过迭代模板片段组装模拟构建全长原子模型。然后通过蛋白质功能数据库BioLiP对3D模型进行串线导出目标的功能洞察。I-TASSER（作为“张服务器”）被列为近期全社会CASP7-12中蛋白质结构预测的第一服务器。在CASP9中也被列为最佳功能预测。服务器正在积极开发中，目标是使用最先进的算法提供最准确的结构和功能预测。 I-TASSER Suite是一套独立的计算机程序，用于高分辨率蛋白质结构预测，细化和基于结构的功能注释。

 #### 6. mGenTHREADER/GenTHREADER
 序列谱和二级结构预测，提供网络服务器，地址：http://bioinf.cs.ucl.ac.uk/psipred/，也可以下载本地软件

 #### 7. MUSTER
 谱-谱比对，提供网络服务器（http://zhanglab.ccmb.med.umich.edu/MUSTER）和软件下载（包含于I-TASSER Suite 5.1）

 + 简介：MUSTER (MUlti-Sources ThreadER)是一种新的蛋白质串线算法，用于从PDB库中识别模板结构。它通过将序列谱-谱对齐与多个结构信息组合来生成序列-模板比对。 MUSTER服务器的输出包括：1.前五名模板蛋白质和查询模板比对；2.MODELLER构建的全长模型。

#### 8.Phyre and Phyre2
见同源建模中Phyre and Phyre2部分的介绍。

#### 9.Selvita Protein Modeling Platform
见同源建模中的Selvita Protein Modeling Platform部分的介绍。

#### 10.SUPERFAMILY
隐马尔可夫模型，提供网络服务器和单机版程序，网站：http://supfam.org/SUPERFAMILY/

+ 简介：SUPERFAMILY是所有蛋白质和基因组的结构和功能注释数据库，其注释是基于隐藏的Markov模型的集合，其代表SCOP 超家族层级的结构蛋白质结构域 。一个超家族将具有进化关系的域组合在一起。通过从隐马尔可夫模型中扫描超过2,478个完全测序的基因组的蛋白质序列产生注释 。对于每种蛋白质，您可以：1.提交SCOP分类序列；2.查看域组织，序列比对和蛋白质序列细节。对于每个基因组，您可以：1.检查超家族分配，系统发育树，域组织列表和网络；2.检查基因组内超过和低于代表的超家族。对于每个超家族，您可以：1.检查SCOP分类，功能注释，基因本体注释，InterPro抽象和基因组分配；2.探索跨越生命树的超家族的分类分布。

#### 11.SPARKS-X
根据序列谱和结构谱通过折叠识别进行3D建模，提供网络服务器，http://sparks-lab.org/yueyang/server/SPARKS-X/

+ 简介：努力通过改变对准评分功能并结合使用改进的二级结构预测，主干扭转角和溶剂可及表面积的SPINE-X技术来进一步改进称为SPARKS的单一方法折叠识别技术。结果：使用SALIGN基准测试对称精度的新方法SPARKS-X，用于折叠识别的Lindahl和SCOP基准测试，以及用于结构预测的CASP 9盲测试。该方法与几种最先进的技术（如HHPRED和BoostThreader）相比较。结果表明，SPARKS-X是最佳单方法识别技术之一。我们还注意到，在模型构建中并入多个模板和细化可能会进一步改进SPARKS-X。

#### 12.BBSP - Building Blocks Structure Predictor
基于混合模板，提供免费的应用和数据库，网址：http://acbrc.org/，下载链接：http://www.acbrc.org/tools.html

### 从头结构预测（Ab initio structure prediction）
维基链接：https://en.wikipedia.org/wiki/De_novo_protein_structure_prediction

#### 1.EVfold
由蛋白质家族相关突变计算出的进化耦合，用于预测单独序列的3D结构，并预测功能残基的偶联强度。预测球状蛋白和跨膜蛋白，提供网络服务器，网址：http://evfold.org/

+ 简介：EVfold使用进化变异来计算蛋白质家族中一组共同进化的残基对，使用称为最大熵的全局方法，正式类似于部分相关性。使用EVcouplings-mfDCA（平均场直接耦合分析）或更准确地使用EVcouplings-PLM快速计算EC。所得到的残基对表示蛋白质之间的相互作用网络，并且在蛋白质的进化轨迹期间反映位置对的共同进化。 EC用作展开蛋白质的距离约束，然后使用距离几何和模拟退火进行折叠。 EVfold处理球状蛋白和跨膜蛋白，目前针对各个领域进行了优化。1.输入蛋白质序列。2.可选地，提供自己的多序列比对。对于α-螺旋跨膜蛋白，您还可以提供自己的拓扑预测。3.获取残差对的EC分数，个别残差的EC强度和高级对的联系图。4.探索一组排名预测的3D结构模型

#### 2.FALCON
通过迭代精化二面角分布来预测蛋白质结构的位置特定隐马尔可夫模型，提供网络服务器，网址：http://protein.ict.ac.cn/FALCON

#### 3. QUARK ★
蒙特卡罗片段装配，用于蛋白建模的在线服务器，地址：http://zhanglab.ccmb.med.umich.edu/QUARK/

+ 简介：QUARK是一种用于从头蛋白质折叠和蛋白质结构预测的计算机算法，其目的是从氨基酸序列构建正确的蛋白质3D模型。 QUARK模型通过在原子级知识型力场的指导下的复制交换蒙特卡罗模拟从小碎片（1-20个残留长）构建。 QUARK在CASP9和CASP10实验中被评为自由建模（FM）中的第一服务器。由于在QUARK仿真中没有使用全局模板信息，所以服务器适用于没有同源模板的蛋白质。

#### 4.NovaFold
见串线法中NovaFold的描述

#### 5.I-TASSER
见串线法中I-TASSER的描述

#### 6.Selvita Protein Modeling Platform
见同源建模和串线法中Selvita Protein Modeling Platform的描述

#### 7.ROBETTA
见同源建模ROBETTA的描述

#### 8.Rosetta@home	
ROBETTA算法的分布式实现，可下载程序：http://boinc.bakerlab.org/rosetta/

#### 9.CABS
见同源建模中CABS的描述

#### 10.CABS-FOLD
从头建模服务，也可以使用替代模板（一致性建模），提供网络服务器，地址：http://biocomp.chem.uw.edu.pl/CABSfold/

+ 简介：用于从头和基于共识的蛋白质结构预测。CABS-fold使用蛋白质结构预测的有效模拟程序：以从头方式（仅从氨基酸序列），由用户提供的模板（一致性建模）和/或用户提供的距离约束（例如从稀疏实验数据）。 Web服务器输出是产生构象的粗粒度轨迹，其全原子分辨率的Jmol表示和预测模型（以及随附的分析）。通常，输出在2-12小时内生成。

#### 11.Bhageerath
用于在原子级建模和预测蛋白质结构的计算协议，提供网络服务器，地址：http://www.scfbio-iitd.res.in/bhageerath/index.jsp

+ 简介：BHAGEERATH：基于能量的蛋白质结构预测服务器。“Bhageerath”的现有版本接受氨基酸序列和二级结构信息，以预测本机的5种候选结构。预期在最终结构中存在至少一种天然类似结构（RMSD <7，无端环）。该服务器已经在80个小球状蛋白上得到验证。

#### 12.Abalone
分子动力学折叠，提供下载程序（商业）。

+ 简介：Abalone是一种通用的分子动力学和分子图形程序，用于在显式（柔性SPC水模型）或隐式水模型中的周期性边界条件下模拟生物分子。主要设计用于模拟AMBER力场中的蛋白质折叠和DNA配体复合物。

#### 13.PEP-FOLD
从头方法，基于HMM结构字符表，肽结构预测服务器，地址：http://bioserv.rpbs.univ-paris-diderot.fr/PEP-FOLD/

+ 简介：PEP-FOLD是从氨基酸序列预测肽结构的新方法。该方法基于结构字母SA字母来描述四个连续残差的构象，将预测的SA字母序列与贪婪算法和粗粒度力场耦合。PEP-FOLD3：在5至50个氨基酸的溶液中更快速地开放线性肽，可以进行初步的肽蛋白相互作用研究。未对二硫键进行优化或用户指定的约束。将此服务用于此类受限肽。 PEP-FOLD最新进化改进了高达36个氨基酸的线性肽的性能 - 最佳模型，NMR结构的平均RMSd为2.1 A，也允许用户指定的约束，如二硫键和残基间接近点。

### 二级结构预测
维基链接：https://en.wikipedia.org/wiki/List_of_protein_secondary_structure_prediction_programs
https://en.wikipedia.org/wiki/Protein_structure_prediction#Secondary_structure

#### 1.SPIDER2 ★
通过迭代深层神经网络（DNN）对蛋白质结构特征（包括二级结构，局部骨架角度和可接近表面积（ASA））的最全面和准确的预测，提供网络服务器和下载软件，网址为http://sparks-lab.org/server/SPIDER2/

#### 2.s2D
在一个统一的框架中预测障碍和二级结构。在基于溶液的NMR数据上训练，提供网络服务器和下载软件，网址为http://www-mvsoftware.ch.cam.ac.uk/index.php/s2D

#### 3.RaptorX-SS8
使用PSI-BLAST曲线的条件神经场预测3态和8态二级结构，提供网络服务器和下载软件，网址分别为http://raptorx.uchicago.edu/ 和 http://ttic.uchicago.edu/~jinbo/software.htm

#### 4.NetSurfP
基于谱的神经网络，NetSurfP服务器预测氨基酸序列中氨基酸的表面可及性和二级结构，提供网络服务器和下载软件，地址为http://www.cbs.dtu.dk/services/NetSurfP/

#### 5.GOR
基于信息理论/ 贝叶斯推理，提供网络服务器，地址为http://abs.cit.nih.gov/gor/

#### 6.Jpred
神经网络分配，提供网络服务器，http://www.compbio.dundee.ac.uk/~www-jpred/

#### 7.Meta-PP
对其他服务器的一致预测（整合了多个网站服务），提供网络服务器，http://www.cs.bgu.ac.il/~dfischer/predictprotein/submit_meta.html

#### 8.PREDATOR
基于知识的数据库比较，提供网络服务器，网址为：http://bioweb.pasteur.fr/seqanal/interfaces/predator-simple.html

#### 9.PredictProtein
基于谱的神经网络，提供网络服务器，网址为：http://www.predictprotein.org/

+ 简介：PredictProtein通过预测相关蛋白质的二级结构和返回家族开始。溶剂可及性和跨膜螺旋预测随后不久就适用。在PredictProtein已经运行的二十年中，我们已经大大扩展了结构注释的广度，例如增加了非规则二级结构和本质无序区域的预测，二硫桥和残留间接触，最后还包括跨 - 膜β桶结构。我们还增加了预测蛋白质功能的重要资源，例如协助亚细胞定位（LocTree，LocTree2，NLSpred）的注释，识别蛋白质 - 蛋白质相互作用位点（ISIS）和蛋白质 - DNA结合位点（DISIS＆SomeNA）很快就发布）。我们已经添加了一些简单的工具来预测酶活性（不幸的是，这种方法在纽约到慕尼黑的转变中没有生存），并通过序列同源性（MetaStudent）推断GeneOntology数字。另一个主要的补充是预测氨基酸变化对蛋白质功能（SNAP和SNAP2）的影响以及直接对蛋白质结构（在制备中）的作用。

#### 10.PSIPRED
两个前馈神经网络对从PSI-BLAST获得的输出进行分析，提供网络服务器，网址为：http://bioinf.cs.ucl.ac.uk/psipred/
，该网站还整合了其他一些网站的服务。
+ 简介：基于PSI-blast的二级结构PREDiction（PSIPRED）是一种用于研究蛋白质结构的方法。在其算法中使用人工神经网络 机器学习方法。它是一个服务器端程序，具有一个网站作为前端界面，可以从一级序列中预测蛋白质的二级结构（β表，α螺旋和线圈）。PSIPRED可作为Web服务和软件使用。该软件作为源代码分发，在技术上被授权为专有软件。它允许修改，但通过禁止软件的利润分配及其结果来实施免费软件规定。预测方法或算法分为三个阶段：生成序列谱，预测初始二级结构，以及过滤预测结构。

#### 11.SOPMA
多重对齐的自优化预测方法（基于最近邻法），提供网络服务器，网站为：https://npsa-prabi.ibcp.fr/NPSA/npsa_sopma.html

#### 12.Homology Modeling Professional for HyperChem
在蛋白质中观察到的氨基酸残基的频率分析，商业软件，网址为：http://www.molfunction.com/bioinformatics.htm

#### 13.SymPred
一种改进的基于字典的方法，其捕获一组蛋白质中的局部序列相似性，提供网络服务器，网址为：http://bio-cluster.iis.sinica.edu.tw/SymPred/

#### 14.YASSPP
使用PSI-BLAST配置文件的基于SVM的级联预测器，提供网络服务器，网址为：http://yasspp.cs.umn.edu/

#### 15.PSSpred
来自PSI-BLAST谱的多个反向传播 神经网络预测器，提供网络服务器和可下载程序，网址为：http://zhanglab.ccmb.med.umich.edu/PSSpred/

+ 简介：PSSpred（Protein Secondary Structure PREDiction）可以准确预测蛋白质二级结构的简单的神经网络的训练算法。它首先使用PSI-BLAST收集多个序列比对。然后根据Rumelhart误差反向传播方法，分别使用Henikoff权重的氨基酸频率和对数奇数数据来训练二级结构。最终二级结构预测结果是来自不同轮廓数据和参数的7种神经网络预测因子的组合。该程序可在本页面底部免费下载。

#### 16.HCAM
通过检测物理化学模式进行Hidropathy聚类辅助方法，提供可下载软件和数据库，网址为：http://www.acbrc.org/tools.html

#### 17.Frag1D
使用基于谱文件的片段匹配来预测二次结构和形状字符串（二面角的离散状态），提供可下载软件和数据库，网址为：http://frag1d.bioshu.se/

### 跨膜螺旋预测
维基链接：https://en.wikipedia.org/w/index.php?title=Transmembrane_helix_prediction&action=edit&redlink=1

#### 1.HMMTOP
基于隐马尔可夫模型，提供网络服务器和单机程序，网址为：http://www.enzim.hu/hmmtop/

#### 2.MEMSAT
基于神经网络和支持向量机，提供网络服务器和单机程序，网址为：http://bioinf.cs.ucl.ac.uk/psipred

#### 3.PHDhtm in PredictProtein
基于多对齐的神经网络系统，提供网络服务器和单机程序，网址为：http://www.predictprotein.org/

#### 4.Phobius
同源性支持预测，提供网络服务器和单机程序，网址为：http://phobius.sbc.su.se/

#### 5.TMHMM
基于隐马尔可夫模型，提供网络服务器和单机程序，网址为：http://www.cbs.dtu.dk/services/TMHMM/

#### 6.CCTOP
基于一致/隐马尔科夫模型，提供网络服务器和单机程序，网址为：http://cctop.enzim.ttk.mta.hu/

#### 7.SVMTop2
基于支持向量机，提供网络服务器，网址为：https://web.archive.org/web/20120502035214/http://bio-cluster.iis.sinica.edu.tw/SVMtop2/Submit.html

### 信号肽预测

#### SignalP
基于人工神经网络和隐马尔科夫模型，提供网络服务器和单机程序，网址为：http://www.cbs.dtu.dk/services/SignalP/
