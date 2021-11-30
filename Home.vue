<!--:” 是指令 “v-bind”的缩写，“@”是指令“v-on”的缩写；-->
<template>
    <el-container style="border: 5px solid #eee" ref="homePage">
        <el-aside width="280px" style="background-color: rgb(238, 241, 246)" v-show="toggle">
            <el-menu efault-active="0"
                     class="el-menu-vertical-demo"
                     :collapse="isCollapse"
            >
                <el-submenu-item index="1">
                    <el-submenu index="1">
                        <template #title><i class="el-icon-message"></i>1 项目信息</template>
                        <el-menu-item index="1-1"><a @click='goAnchor("page-1")'>1.1 项目简介</a></el-menu-item>
                        <el-menu-item index="1-2"><a @click='goAnchor("page-2")'>1.2 分析方案</a></el-menu-item>
                        <el-menu-item index="1-3"><a @click='goAnchor("page-3")'>1.3 差异表达分析</a></el-menu-item>
                        <el-menu-item index="1-4"><a @click='goAnchor("page-4")'>1.4 PCA主成分分析图（Figure）</a>
                        </el-menu-item>
                        <el-menu-item index="1-5"><a @click='goAnchor("page-5")'>1.5 PCA主成分分析表（Table）</a></el-menu-item>
                        <el-menu-item index="1-6"><a @click='goAnchor("page-6")'>1.6 火山图（Figure）</a></el-menu-item>
                        <el-menu-item index="1-7"><a @click='goAnchor("page-7")'>1.7 热 图（Figure）</a></el-menu-item>

                    </el-submenu>
                </el-submenu-item>

                <el-submenu-item index="2">
                    <el-submenu index="2">
                        <template #title>
                            <i class="el-icon-message"></i>2 功能富集分析
                        </template>
                        <el-submenu index="2-1">
                            <template #title>2.1 GO富集分析</template>
                            <el-menu-item index="2-1-1"><a @click='goAnchor("page-8")'>2.1.1 GO富集分析表</a></el-menu-item>
                            <el-menu-item index="2-1-2"><a @click='goAnchor("page-9")'>2.1.2 GO富集分析柱状图</a></el-menu-item>
                            <el-menu-item index="2-1-3"><a @click='goAnchor("page-213")'>2.1.3 GO富集分析气泡图</a></el-menu-item>
                            <el-menu-item index="2-1-4"><a @click='goAnchor("page-214")'>2.1.4 GO富集分析网络图</a></el-menu-item>
                        </el-submenu>
                        <el-submenu index="2-2">
                            <template #title>2.2 KEGG富集分析</template>
                            <el-menu-item index="2-2-1"><a @click='goAnchor("page-221")'>2.2.1 KEGG富集分析表</a></el-menu-item>
                            <el-menu-item index="2-2-2"><a @click='goAnchor("page-222")'>2.2.2 KEGG富集分析柱状图</a></el-menu-item>
                            <el-menu-item index="2-2-3"><a @click='goAnchor("page-223")'>2.2.3 KEGG富集分析气泡图</a></el-menu-item>
                            <el-menu-item index="2-2-4"><a @click='goAnchor("page-224")'>2.2.4 KEGG富集分析网络图</a></el-menu-item>
                            <el-menu-item index="2-2-5"><a @click='goAnchor("page-225")'>2.2.5 KEGG富集分析通路图</a></el-menu-item>
                        </el-submenu>
                        <el-submenu index="2-3">
                            <template #title>2.3 GSEA富集分析</template>
                            <el-menu-item index="2-3-1"><a @click='goAnchor("page-231")'>2.3.1 GSEA富集分析表</a></el-menu-item>
                            <el-menu-item index="2-3-2"><a @click='goAnchor("page-232")'>2.3.2 GSEA富集分析图</a></el-menu-item>
                        </el-submenu>
                    </el-submenu>
                </el-submenu-item>

                <el-submenu-item index="3">
                    <el-submenu index="3">
                        <template #title><i class="el-icon-message"></i>3 互作网络分析</template>
                        <el-menu-item index="3-1"><a @click='goAnchor("page-31")'>3.1 蛋白互作网络表</a></el-menu-item>
                        <el-menu-item index="3-2"><a @click='goAnchor("page-32")'>3.2 蛋白互作网络图</a></el-menu-item>
                    </el-submenu>
                </el-submenu-item>

                <el-submenu-item index="4">
                    <el-submenu index="4">
                        <template #title><i class="el-icon-message"></i>4 附录</template>
                        <el-menu-item index="4-1"><a @click='goAnchor("page-41")'>4.1 参考文献</a></el-menu-item>
                        <el-menu-item index="4-2"><a @click='goAnchor("page-42")'>4.2 软件与方法说明</a></el-menu-item>
                        <el-menu-item index="4-3"><a @click='goAnchor("page-43")'>4.3 结果目录</a></el-menu-item>
                    </el-submenu>
                </el-submenu-item>
            </el-menu>
        </el-aside>

<!--        ======================================================================================================================================================-->

        <el-container>
            <!--            <el-header>header</el-header>-->
            <el-main>
                <div>
                    <scroll-container>
                        <scroll-page id="page-1" class="s-page">
                            <h2><b>1 项目信息</b></h2>
                            <h3>1.1 项目简介</h3>
                            <div class="contentOne">
                                <div class="contA"><p>
                                    本报告为解螺旋真核转录组标准项目结题报告。本项目使用DNBSEQ平台一共测了12个样品，每个样品平均产出7.64G数据。样品比对基因组的平均比对率为 93.61%
                                    ，比对基因集的平均比对率为63.13% ；一共检测到17441个基因。</p></div>
                                <div class="contB" id="contB">
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-2" class="s-page">
                            <h2>1.2 分析方案</h2>
                            <div class="contentOne">
                                <div class="contA">本项目共20个样本。下表为转录组测序分析结果统计表:</div>
                                <br/>
                                <div class="contB"><h5>表1样品分析结果统计表</h5>
                                    <table01></table01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-3" class="s-page">
                            <h2>1.3 差异表达分析（Table）</h2>
                            <div class="contentOne">
                                <div class="contA">
                                    下表为基因差异表达分析结果统计表:
                                </div>
                                <br/>
                                <div class="contB"><h5>表2 差异表达分析结果统计表</h5>
                                    <table01></table01>
                                </div>
                                <br/>
                                <p>分析结果统计下载链接：</p>
                                <h6>分析结果统计信息</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-4" class="s-page">
                            <h2>1.4 PCA主成分分析图（Figure）</h2>
                            <div class="contentOne">
                                <div class="contA">
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;主成分分析（Principal Component
                                    Analysis，PCA）是将多个变量通过降维为少数几个相互独立的变量（即主成分），
                                    同时尽可能多地保留原始数据信息的一种多元统计分析方法。在转录组的分析中，
                                    PCA将样本所包含的大量基因表达量信息降维为少数几个互相无关的主成分，
                                    以进行样本间的比较，方便找出离群样品、判别相似性高的样品簇等。
                                    <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;说明： 图中不同颜色代表不同 group
                                        中的样本，样本间相似度越高则在图中越聚集，反之样本间相似度越低则空间距离越远。</p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <figure01></figure01>
                                    <h5>图1 PCA主成分分析图</h5></div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-5" class="s-page">
                            <h2>1.5 PCA主成分分析表（Table）</h2>
                            <div class="contentOne">
                                <div class="contA">

                                </div>
                                <br/>
                                <div class="contB"><h5>1.5 PCA主成分分析表（Table）</h5>
                                    <table01></table01>
                                </div>
                                <br/>
                                <div>

                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-6" class="s-page">
                            <h2>1.6 火山图（Figure）</h2>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        火山图可以直观反映差异表达基因的整体分布情况。以log2(foldchange）为横坐标，-log10(P.adj）为纵坐标，对差异表达分析中所有的基因进行火山图绘制。

                                        作图软件：R (3.6.3版本) (统计分析与可视化)；

                                        R包：主要为 ggplot2 (用于可视化)；

                                        图中参数：LogFC > 1 & 图中的p值 0.05；</p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <figure02></figure02>
                                    <h5>图2 差异表达基因火山图</h5>
                                </div>
                                <br/>
                                <p>分析结果统计下载链接：</p>
                                <h6>分析结果统计信息</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-7" class="s-page">
                            <h2>1.7 热 图（Figure）</h2>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        聚类分析往往用于反映不同实验条件下样本差异表达基因的变化模式。功能相关的基因在相同条件下通常具有相似的表达模式，例如被共同的转录因子调控的基因，或其产物构成同一个蛋白复合体的基因，或参与相同生物学过程的基因。我们利用R包，对差异表达基因和不同样本/实验条件进行层次聚类分析，同时利用K-means算法将差异基因分成若干个表达模式相近的集合，同一个集合中的基因在相同的条件下具有相似的表达变化趋势。</p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <figure17></figure17>
                                    <h5>图3 差异基因聚类图</h5>
                                    注：根据差异表达基因在每个样品里的表达量（FPKM值），取以2为底的对数后，计算欧氏距离，再利用系统聚类法（Hierarchical Cluster），最终得到样品的整体聚类结果。在图中，行为基因，列为样品，基因在不同样品中的表达量是否有差异可以通过热图颜色的变化体现。
                                </div>
                                <br/>
                                <p>分析结果统计下载链接：</p>
                                <h6>分析结果统计信息</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-8" class="s-page">
                            <h2><b>2 功能富集分析</b></h2>
                            <h3>2.1 GO富集分析</h3>
                            Gene ontology（基因本体论，GO）是一个国际标准化的基因功能分类体系，提供了一套动态更新的标准词汇表来全面描述生物体中基因核基因产物的属性。GO总共有三个本体（ontology），分别描述基因的分子功能（molecular function）、细胞成分（cellular component）、生物学过程（biological process）。GO的基本单位是term（词条、节点），每个term都对应一个属性。GO功能显著性富集分析，首先把所有显著性差异表达基因向Gene ontology数据库的各term映射，计算每个term的基因数目，然后应用超几何检验，找出与整个基因组背景相比，在显著性差异表达基因中显著富集的GO条目。通过GO功能显著性富集分析能确定差异表达基因行使的主要生物学功能。
                            <h4>2.1.1 GO富集分析表（Table）</h4>

                        </scroll-page>

                        <scroll-page id="page-9" class="s-page">
                            <h4>2.1.2 GO富集分析柱状图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        为了直观的展示差异表达基因集合的GO统计结果，可以根据上表统计结果，绘制柱状图，结果如下：</p>                                </div>
                                <br/>
                                <div class="contB">
                                    <figure212></figure212>
                                    <h5>图4 差异表达基因的GO统计柱状图</h5>
                                    注：横坐标为GO Term，左纵坐标为基因数目所占百分比，右纵坐标为基因数目。此图展示的是在显著上调或显著下调表达基因在二级GO Term的富集情况。                                </div>
                                <br/>
                                <p>分析结果统计下载链接：</p>
                                <h6>分析结果统计信息</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-213" class="s-page">
                            <h4>2.1.3 GO富集分析气泡图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对于每个比较组而言，展示q值富集的GO条目以及富集的程度，结果展示如下图：</p>                                </div>
                                <br/>
                                <div class="contB">
                                    <figure213></figure213>
                                    <h5>图5 单个组GO条目q值富集图</h5>
                                    注：横坐标代表富集比例（rich ratio），其计算公式为：(该通路的差异基因/所有的差异基因)/(注释到该通路的基因/所有能被注释到的基因) 。纵坐标代表不同的GO条目。每个点的颜色表示该GO条目的富集程度，颜色越趋近于红色表示富集程度越高（q值越小）。每个点的大小表示富集到该GO条目的基因的多少，点越大表示富集到该GO条目的基因越多，反之则越少。为了便于展示，当GO条目少于10条时，展示全部条目；多于10条时，示例图仅展示其中的10个条目，其他结果请查看相应结果文件。                                <br/>
                                </div>
                                    <p>单个组GO条目q值富集图下载链接:</p>
                                <h6>单个组GO条目q值富集图下载链接:</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-214" class="s-page">
                            <h4>2.1.2 GO富集分析柱状图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对于每个比较组而言，展示q值富集的GO条目以及富集的程度，结果展示如下图：</p>                                </div>
                                <br/>
                                <div class="contB">
                                    <figure214></figure214>
                                    <h5>图6 GO富集分析网络图</h5>
                                    注：横坐标代表富集比例（rich ratio），其计算公式为：(该通路的差异基因/所有的差异基因)/(注释到该通路的基因/所有能被注释到的基因) 。纵坐标代表不同的GO条目。每个点的颜色表示该GO条目的富集程度，颜色越趋近于红色表示富集程度越高（q值越小）。每个点的大小表示富集到该GO条目的基因的多少，点越大表示富集到该GO条目的基因越多，反之则越少。为了便于展示，当GO条目少于10条时，展示全部条目；多于10条时，示例图仅展示其中的10个条目，其他结果请查看相应结果文件。                                <br/>
                                </div>
                                    <p>单个组GO条目q值富集图下载链接:</p>
                                <h6>单个组GO条目q值富集图下载链接:</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-221" class="s-page">
                            <h3>2.2 KEGG富集分析</h3>
                            Kyoto Encyclopedia of Genes and Genomes（京都基因与基因组百科全书，KEGG）是一个整合了基因组、化学和系统功能信息的综合数据库。KEGG下属4个大类和17个子数据库，其中有一个数据库叫做KEGG Pathway，专门存储不同物种中的基因通路的信息，也是用的最多的一个。因此，KEGG就被当作一个通路数据库了。

                            在生物体内，不同基因相互协调行使生物学功能，基于Pathway的分析有助于进一步了解基因的生物学功能。Pathway显著性富集分析以KEGG Pathway为单位，应用超几何检验，找出与整个基因组背景相比，在显著性差异表达基因中显著性富集的Pathway。通过Pathway显著性富集能确定差异表达基因参与的最主要生化代谢途径和信号转导途径。
                            <h4>2.2.1 KEGG富集分析表（Table）</h4>
                            <div class="contB"><h5>表4 KEGG结果示例表</h5>
                                <table01></table01>
                            </div>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        （1）Name：通路的名称；<br>
                                        （2）Map：进行富集的map条目；<br>
                                        （3）Count1，Count2，Count3，Count4：进行Fisher检验的四个数据，分别为上面超几何检验公式里的m，M-m，n-m，N-n-M+m；<br>
                                        （4）p：检验后的p值；
                                        （5）q：多重检验校正的p值；<br>
                                        （6）Gene_in_DE：差异表达基因中注释到该通路的差异表达基因名称；<br>
                                        （7）Up_Gene：差异表达基因中注释到该通路的上调基因；<br>
                                        （8）Up_Count：差异表达基因中注释到该通路的上调基因的个数；<br>
                                        （9）Down_Gene：差异表达基因中注释到该通路的下调基因；<br>
                                        （10）Down_Count:差异表达基因中注释到该通路的下调基因的个数；<br>
                                        （11）Links：该通路的KEGG数据库链接；<br>
                                        （12）Result：该通路是否显著。<br>
                                    </p>
                                </div>
                                <!--<br/>
                                <div class="contB">
                                    <table01></table01>
                                    <h5>图5 单个组GO条目q值富集图</h5>
                                    注：横坐标代表富集比例（rich ratio），其计算公式为：(该通路的差异基因/所有的差异基因)/(注释到该通路的基因/所有能被注释到的基因) 。纵坐标代表不同的GO条目。每个点的颜色表示该GO条目的富集程度，颜色越趋近于红色表示富集程度越高（q值越小）。每个点的大小表示富集到该GO条目的基因的多少，点越大表示富集到该GO条目的基因越多，反之则越少。为了便于展示，当GO条目少于10条时，展示全部条目；多于10条时，示例图仅展示其中的10个条目，其他结果请查看相应结果文件。                                <br/>
                                </div>
                                    <p>单个组GO条目q值富集图下载链接:</p>
                                <h6>单个组GO条目q值富集图下载链接:</h6>
                                <div>
                                    <select01></select01>
                                </div>-->
                            </div>
                        </scroll-page>

                        <scroll-page id="page-222" class="s-page">
                            <h4>2.2.2 KEGG富集分析柱状图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对于每个比较组而言，展示q值富集的GO条目以及富集的程度，结果展示如下图：</p>                                </div>
                                <br/>
                                <div class="contB">
                                    <figure222></figure222>
                                    <h5>图7 KEGG富集分析柱状图</h5>
                                    注：横坐标代表富集比例（rich ratio），其计算公式为：(该通路的差异基因/所有的差异基因)/(注释到该通路的基因/所有能被注释到的基因) 。纵坐标代表不同的GO条目。每个点的颜色表示该GO条目的富集程度，颜色越趋近于红色表示富集程度越高（q值越小）。每个点的大小表示富集到该GO条目的基因的多少，点越大表示富集到该GO条目的基因越多，反之则越少。为了便于展示，当GO条目少于10条时，展示全部条目；多于10条时，示例图仅展示其中的10个条目，其他结果请查看相应结果文件。                                <br/>
                                </div>
                                <p>KEGG富集分析柱状图</p>
                                <h6>KEGG富集分析柱状图</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-223" class="s-page">
                            <h4>2.2.3 KEGG富集分析气泡图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对于每个比较组进行q值的KEGG条目的分析，结果展示如下图：</p>                                </div>
                                <br/>
                                <div class="contB">
                                    <figure223></figure223>
                                    <h5>图8 单个组的KEGG富集q值结果图</h5>
                                    注：横坐标为Rich Ritio，纵坐标表示KEGG pathway名称，点的大小代表此pathway中差异基因数量，点的颜色代表每个点表示该KEGG条目的富集程度，颜色越趋近于红色表示富集程度越高。                                </div>
                                <p>单个组的KEGG富集q值结果图下载链接：</p>
                                <h6>单个组的KEGG富集q值结果图下载链接：</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-224" class="s-page">
                            <h4>2.2.4 KEGG富集分析网络图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对于每个比较组进行q值的KEGG条目的分析，结果展示如下图：</p>                                </div>
                                <br/>
                                <div class="contB">
                                    <figure224></figure224>
                                    <h5>图9 KEGG富集分析网络图</h5>
                                    注：横坐标为Rich Ritio，纵坐标表示KEGG pathway名称，点的大小代表此pathway中差异基因数量，点的颜色代表每个点表示该KEGG条目的富集程度，颜色越趋近于红色表示富集程度越高。                                </div>
                                <p>单个组的KEGG富集q值结果图下载链接：</p>
                                <h6>单个组的KEGG富集q值结果图下载链接：</h6>
                                <div>
                                    <select01></select01>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-225" class="s-page">
                            <h4>2.2.5 KEGG富集分析通路图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对每个比较的通路图进行注释，得到的结果如下图所示，红色表示上调差异基因注释在KO上，该KO显示为红色，反之，绿色表示该KO下调。

                                        包含差异基因的KEGG代谢通路图如下：
                                    </p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <figure225></figure225>
                                    <h5>图10 包含差异基因的KEGG代谢通路图</h5>
                                    注：上调差异基因注释在KO上，该KO显示为红色，反之，下调基因对应的KO显示为绿色。KEGG pathway中不同框内数字代表酶的EC编号（EC number），而整个通路由多种酶催化的复杂的生化反应构成，此通路图中与差异表达基因相关的酶均用不同的颜色标出，根据研究目的可重点研究某些关键代谢通路相关基因的差异表达情况，从参与代谢的角度揭示转录水平的调控机制。
                                    <p>单个组的KEGG富集q值结果图下载链接：</p>
                                    <h6>包含差异基因的KEGG代谢通路图下载链接：</h6>
                                <div>
                                    <select01></select01>
                                </div>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-231" class="s-page">
                            <h2><b>2.3 GSEA富集分析</b></h2>
                            Gene Set Enrichment Analysis（基因基因富集分析，GSEA）用来评估一个预先定义的基因集【已知功能的基因集，可以是GO注释、MsigDB的注释，或者其他符合格式的基因集定义】的基因在与表型相关度排序的基因表中的分布趋势，从而判断其对表型的贡献。对基因根据其表型的关联度（也可以理解为表达值的变化）从大到小排序，然后判断基因集内每条注释下的基因是否富集于表型相关度配许后基因表的上部或下部，从而判断基因集内基因协同变化对表型变化的影响。

                            GO和KEGG富集分析是先筛选差异基因，再判断差异基因在哪些注释的通路存在富集；这涉及到阈值的设定，存在一定主观性，且只能用于表达变化较大的基因，即我们丁语的显著差异基因。而GSEA不局限于差异基因，从基因集的富集角度出发，更容易囊括细微但协调性的变化对生物通路的影响。
                            <h4>2.3.1 GSEA富集分析表（Table）（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对每个比较的通路图进行注释，得到的结果如下图所示，红色表示上调差异基因注释在KO上，该KO显示为红色，反之，绿色表示该KO下调。

                                        包含差异基因的KEGG代谢通路图如下：
                                    </p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <h5>表5 GSEA富集分析表</h5>
                                    <table01></table01>
                                    <p>GSEA富集分析表下载链接：</p>
                                    <h6>GSEA富集分析表下载链接：</h6>
                                <div>
                                    <select01></select01>
                                </div>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-232" class="s-page">
                            <h4>2.3.2 GSEA富集分析图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        我们获取了在不同条件下差异表达的基因，通常希望获取该基因集的功能概况，以便更好地了解潜在的生物学过程。基因集富集分析（GSEA）可以分析特定基因集（如关注的GO条目或KEGG通路）在两个生物学状态（如癌症与对照）中是否存在差异。而转录组学技术和蛋白质组学结果通常可以鉴定出数千种用于分析的基因。

                                        传统的富集分析不考虑基因表达量的变化趋势，其算法的核心只关注这些差异表达基因的分布是否跟随机抽样得到的分布一致，并且需要主观设置差异基因筛选阈值，可能过滤掉有用信息，不能反应整体情况。而GSEA富集分析则考虑了差异的上调下调，并且考虑到所有基因，无须主观设置过滤阈值。

                                        结果展示如下图
                                    </p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <figure232></figure232>
                                    <h5>图10 包含差异基因的KEGG代谢通路图</h5>
                                    注：上调差异基因注释在KO上，该KO显示为红色，反之，下调基因对应的KO显示为绿色。KEGG pathway中不同框内数字代表酶的EC编号（EC number），而整个通路由多种酶催化的复杂的生化反应构成，此通路图中与差异表达基因相关的酶均用不同的颜色标出，根据研究目的可重点研究某些关键代谢通路相关基因的差异表达情况，从参与代谢的角度揭示转录水平的调控机制。
                                    <p>单个组的KEGG富集q值结果图下载链接：</p>
                                    <h6>包含差异基因的KEGG代谢通路图下载链接：</h6>
                                    <div>
                                        <select01></select01>
                                    </div>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-31" class="s-page">
                            <h2><b>3 互作网络分析</b></h2>
                            蛋白质-蛋白质相互作用（protein-protein interaction, PPI）是指两个或两个以上的蛋白质分子通过非共价键形成蛋白质复合体（protein complex）的过程，来参与生物信号传递、基因表达调节、能量和物质代谢及细胞周期调控等生命过程的各个环节。研究蛋白之间的相互作用网络，有助于挖掘核心的调控基因。目前已经有很多的蛋白质相互作用的数据库，而STRING数据库绝对是其中覆盖的物种最多，相互作用信息做大的一个。STRING数据库是常用的蛋白质互作网络数据库，收录多个物种预测的和实验验证的蛋白质-蛋白质互作。在本项目中，我们使用了STRING数据库在线工具，提取显著差异基因蛋白质-蛋白质相互作用（PPI），以构建显著差异基因的PPI网络。经STRING数据库筛选后的PPI网络，由R语言（igragh包）进行可视化。
                            <h4>3.1 蛋白互作网络表（Table）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        对每个比较的通路图进行注释，得到的结果如下图所示，红色表示上调差异基因注释在KO上，该KO显示为红色，反之，绿色表示该KO下调。

                                        包含差异基因的KEGG代谢通路图如下：
                                    </p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <h5>表6 蛋白互作网络表</h5>
                                    <table01></table01>
                                    <p>蛋白互作网络表下载链接：</p>
                                    <h6>蛋白互作网络表下载链接：</h6>
                                    <div>
                                        <select01></select01>
                                    </div>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-32" class="s-page">
                            <h4>3.2 蛋白互作网络图（Figure）</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        通过蛋白互作网络分析，可以发现与不同处理或疾病相关的一些关键基因，对这些关键的基因进行功能分析，可以从代谢水平上了解不同处理对基因表达的影响或疾病的发生或发展机制。STRING是收录多个物种预测的和实验验证的蛋白质-蛋白质互作的数据库，包括直接的物理互作和间接的功能相关。针对数据库中包含的物种，结合差异表达分析结果和数据库收录的互作关系对，可直接将差异表达基因集（比如差异基因List）映射到该物种的蛋白互作网络，构建差异表达基因互作网络。

                                        我们提供参考物种蛋白互作网络数据文件（蛋白互作网络参考数据集）和目标基因集，构建蛋白互作网络的网络数据文件可以直接导入Cytoscape软件(Shannon, et al. , 2003)，并根据目标基因集中的基因属性对网络进行可视化编辑。Cytoscape软件使用方法可参考我们提供的使用说明文档（cytoscape.docx, 见下方链接）。您可以针对一些网络的拓扑属性进行统计和标示作图，若某一节点（即基因）相连的边（即基因间互作关系）越多，则表明这些节点会位于较为核心的位置(hub节点)。互作网络图中节点的颜色与此基因的上下调特性相关，若基因上调，则其节点为黄色；若基因下调，则其节点为青色。根据不同的研究目的和需求，您还可以在网络图中进行调整节点位置和颜色、标注表达量水平等操作。详细可参考我们提供的使用说明文档（见网页版下载链接处）。将文件导入Cytoscape软件后的效果图如下：
                                    </p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <figure32></figure32>
                                    <h5>图12 差异基因蛋白互作网络示例图</h5>
                                    注：节点表示基因，边表示两基因间存在互作关系。与节点相连的边越多，其连通性 （度） 越大，表明该节点基因在该网络中的重要性越强。网络图中上调和下调的基因分别用黄色和蓝色标示。                                    <p>单个组的KEGG富集q值结果图下载链接：</p>
                                    <p>差异基因蛋白互作网络图下载链接：</p>
                                    <h6>差异基因蛋白互作网络图下载链接：</h6>
                                    <div>
                                        <select01></select01>
                                    </div>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-41" class="s-page">
                            <h2><b>4 附录</b></h2>
                            <h4>4.1 参考文献</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p><b>
                                        <b>Florea, L., Song, L. & Salzberg, S. L. Thousands of exon skipping events differentiate among splicing patterns in sixteen human tissues. F1000Research (2013).</b><br><br>

                                        <b>Langmead, B., Trapnell, C., Pop, M. & Salzberg, S. Ultrafast and memory-efficient alignment of short DNA sequences to the human genome. Genome Biology 10, R25-10 (2009).</b><br><br>

                                        <b>Li, H. et al. The sequence Alignment/Map format and SAMtools. Bioinformatics (Oxford, England) 25, 2078-2079 (2009).</b><br><br>

                                        <b>Shannon, P. et al. Cytoscape: A software environment for integrated models of biomolecular interaction networks. Genome Research 13, 2498-2504 (2003).</b><br><br>

                                        <b>Love MI, Huber W, Anders S. Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2. Genome Biol. 15(12):550 (2014).</b><br><br>

                                        <b>Sirén J, Välimäki N, Mäkinen V.Indexing Graphs for Path Queries with Applications in Genome Research. IEEE/ACM Trans Comput Biol Bioinform. 11(2):375-88 (2014)</b><br><br>

                                        <b>Thorvaldsdóttir, H., Robinson, J.T. & Mesirov, J. P. Integrative genomics viewer (IGV): high-performance genomics data visualization and exploration. Briefings in bioinformatics 14, 178-192 (2013).</b><br><br>

                                        <b>Trapnell, C. et al. Transcript assembly and quantification by RNA-seq reveals unannotated transcripts and isoform switching during cell differentiation. Nature Biotechnology 28, 511-515 (2010).</b><br><br>

                                        <b>Trapnell, C., Pachter, L. & Salzberg, S. L. TopHat: discovering splice junctions with RNA-seq. Bioinformatics 25, 1105-1111 (2009).</b><br><br>

                                        <b>Wang, L., Feng, Z., Wang, X., Wang, X. & Zhang, X. DEGseq: an r package for identifying differentially expressed genes from RNA-seq data. Bioinformatics 26, 136-138 (2010).</b><br><br>
                                    </b> </p>
                                </div>
                            </div>
                        </scroll-page>

                        <scroll-page id="page-42" class="s-page">
                            <h4>4.2 软件与方法说明</h4>
                            <div class="contentOne">
                                <div class="contA">
                                    <p>
                                        本项目所用分析方法和软件中/英文说明见方法文档。

                                        DEGSeq、DESeq2软件的方法的说明如下：

                                        DEGSeq：基于count值服从二项分布的假设，借鉴MAplot理论，估计M值得近似正态分布，从而计算每个基因在两个样品中不差异表达的概率值p-value，并通过Benjamini矫正或Storey矫正获得q-value（FDR）；

                                        DESeq2: 基于count值服从负二项分布假设，估计样品和基因特异的深度参数，且对离差利用线性回归进行了“收缩”，主要考虑相同表达水平的基因可能具有相似的离差以及每个基因的表达特性。利用线性回归估计基因在各样品中的表达强度，并用Wald test计算每个基因在两组样品中不差异表达的概率值p-value，并通过BH方法对p-value进行校正得到q-value（FDR）。
                                    </p>
                                </div>
                                <br/>
                                <div class="contB">
                                    <p>转录组分析的各种软件说明及分析方法的中英文版介绍下载链接：：</p>
                                    <h6>软件说明及分析方法下载链接：</h6>
                                    <div>
                                        <select01></select01>
                                    </div>
                                </div>
                                <div class="contB">
                                    <p>结题报告文件打开方式说明下载链接：</p>
                                    <h6>文件打开方式指南下载链接：</h6>
                                    <div>
                                        <select01></select01>
                                    </div>
                                </div>
                                <div class="contB">
                                    <p>结题文件解读帮助文档下载链接：</p>
                                    <h6>结题文件解读帮助文档下载链接：</h6>
                                    <div>
                                        <select01></select01>
                                    </div>
                                </div>
                            </div>
                        </scroll-page>

                    </scroll-container>
                </div>
            </el-main>
            <el-footer class="homeFooter">
                <el-switch v-model="toggle" />
            </el-footer>
        </el-container>
    </el-container>
</template>

<script lang="ts">
  import { defineComponent, ref } from "vue";
  import table01 from "../components/table/table";
  import select01 from "../components/download/select";
  import figure01 from "../components/figure/1.4";
  import figure02 from "../components/figure/1.6";
  import figure17 from "../components/figure/1.7";
  import figure212 from "../components/figure/2.1.2";
  import figure213 from "../components/figure/2.1.3";
  import figure214 from "../components/figure/2.1.4";
  // import figure221 from "../components/figure/2.2.1";
  import figure222 from "../components/figure/2.2.2";
  import figure223 from "../components/figure/2.2.3";
  import figure224 from "../components/figure/2.2.4";
  import figure225 from "../components/figure/2.2.5";
  import figure232 from "../components/figure/2.3.2";
  import figure32 from "../components/figure/3.2";


  export default defineComponent({
    props: {},
    components: {
      table01,
      select01,
      figure01,
      figure02,
      figure17,
      figure212,
      figure213,
      figure214,
      // figure221,
      figure222,
      figure223,
      figure224,
      figure225,
      figure232,
      figure32,
    },
    data() {
      return {
        clientHeight: "",
        toggle: true
      };
    },
    setup() {
      const isCollapse = ref(false);
      const handleOpen = (key, keyPath) => {
        console.log(key, keyPath);
      };
      const handleClose = (key, keyPath) => {
        console.log(key, keyPath);
      };
      const handleSelect = (key, keyPath) => {
        console.log(key, keyPath);
      };

      const goAnchor = (selector) => {
        document.getElementById(selector).scrollIntoView();
      };

      return {
        isCollapse,
        handleOpen,
        handleClose,
        handleSelect,
        goAnchor
      };
    },
    watch: {
      // 如果 `clientHeight` 发生改变，这个函数就会运行
      clientHeight: function() {
        this.changeFixed(this.clientHeight);
      }
    },
    methods: {
      changeFixed(clientHeight) { //动态修改样式
        // console.log(clientHeight);
        this.$refs.homePage.$el.style.height = clientHeight - 20 + "px";
      }
    },
    mounted() {
      // 获取浏览器可视区域高度
      this.clientHeight = `${document.documentElement.clientHeight}`;
      //console.log(self.clientHeight);
      window.onresize = function temp() {
        this.clientHeight = `${document.documentElement.clientHeight}`;
      };
    }
  });
</script>

<style scoped lang="scss">
    .el-header {
        background-color: #b3c0d1;
        color: var(--el-text-color-primary);
        line-height: 60px;
    }

    /*scroll-container {
        display: block;
        width: 100%;
        height: 100%;
        overflow-y: scroll;
        scroll-behavior: smooth;
    }*/


    .scroll-page {
        display: flex;
        /* align-items: center;
        justify-content: center; */
        height: 50%;
        width: 100%;
    }

    .homeFooter {
        background-color: rgba(24, 33, 25, 0.09);
        height: 20px;
    }

    .el-aside {
        color: var(--el-text-color-primary);
    }

    .contentOne {
        display: block;
        /* height: 250px; */
    }

    .s-page {
        /*width: 180px;
        height: 180px;
        background-color: green;
        margin-top: 20px;*/
        height: 100px;
        background: #BBE8F2;
        top: 0;
        left: 0;
        width: 100%;
        text-align: left;
    }

    h5 {
        text-align: center;
    }
</style>
