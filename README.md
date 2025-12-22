## 论文列表
1. Jingning Zhang, Jianan Zhan, Jin Jin, Cheng Ma, Ruzhang Zhao, Jared O’connell, Yunxuan Jiang, 23andme Research Team, Bertram L Koelsch, Haoyu Zhang. **An Ensemble Penalized Regression Method for Multi-Ancestry Polygenic Risk Prediction**. *Nature Communications*, Vol. 15, No. 1, pp. 3238, 2024. [Notes](), [Source Code]()

## 待解决的问题
- ReferencePanel数据来源？   What is the data source for ReferencePanel?
- PRScice跑EN模型？
- sklearn跑EN模型和MLP模型？重点是输入数据的处理？
- 实验结果文件及图表的含义？
- IMPUTE脚本的结果文件\*.hap和*.legend如何与下载的\*.map匹配作为HAPGEN一组输入？How can the result files *.hap and *.legend from the IMPUTE script be matched with the downloaded *.map as a set of inputs for HAPGEN?
- HAPGEN的输出结果如何转换为.HDF5文件，作为Simulations程序的输入？或者不使用HAPGEN，如何将一组\*.hap、\*.legend和\*.map文件转化为.HDF5文件？How can the output results of HAPGEN be converted into an HDF5 file to serve as the input for the Simulations program? Or, without using HAPGEN, how can a set of *.hap, *.legend and *.map files be transformed into an HDF5 file?
- GWAS Catalog下载的tsv文件如何提取.bed、.fam文件？How to extract the .bed and .fam files from the tsv file downloaded from the GWAS Catalog?
- 其他疾病数据下载后的作用?

## 已完成工作
- HAPGEN数据仿真流程及参数设置的含义
- PLINK的使用及跑P+T模型
- PRSice跑P+T模型
- [数据集下载](https://www.internationalgenome.org/data-portal/population/FIN):千人基因组计划中在芬兰地区的测序数据-[90个文件](90-dadaset-links.txt   90-数据集链接.txt)- [Download the dataset](https://www.internationalgenome.org/data-portal/population/FIN): Sequencing data from the 1000 Genomes Project in the Finnish region - [90 files](90-dadaset-links.txt   90-数据集链接.txt)

-----
## 方法框架
<center><a title   标题="framework"   “框架”><img src="framework.png" width   宽度="600"/></a></center>  <中心>

*Datasets: <https://www.internationalgenome.org>  数据集： 
*Simulations: <https://github.com/JasonGrealey/Simulations>  模拟程序： 
*Sourcecode: <https://github.com/xuyu-cam/Deep-learning-for-genetic-prediction-of-complex-traits>

## 软件工具
- HAPGEN
  - [官网](https://mathgen.stats.ox.ac.uk/genetics_software/hapgen/hapgen2.html)- [Official Website](https://mathgen.stats.ox.ac.uk/genetics_software/hapgen/hapgen2.html)
  - 输入：\*.hap, \*.legend, \*.map- Input: \*.hap, \*.legend, \*.map
  - 输出：
    - cases: \*.gen, \*.sample, \*.haps, \*.tags.gen- 文件类型：\*.gen、\*.sample、\*.haps、\*.tags.gen
    - controls: \*.gen, \*.sample, \*.haps, \*.tags.gen- 控制项：\*.gen、\*.sample、\*.haps、\*.tags.gen
    - \*.legend (同输入)
    - \*.summary (日志文件)
- IMPUTE2
  - [官网](https://mathgen.stats.ox.ac.uk/impute/impute_v2.html#home)- [Official Website](https://mathgen.stats.ox.ac.uk/impute/impute_v2.html#home)
  - 输入：\*.vcf
  - 输出：\*.hap, \*.legend   Output: *.hap, *.legend
  - 运行脚本: [vcf2impute_legend_haps.pl](https://mathgen.stats.ox.ac.uk/impute/scripts/vcf2impute_legend_haps)- Run script: [vcf2impute_legend_haps.pl](https://mathgen.stats.ox.ac.uk/impute/scripts/vcf2impute_legend_haps)
- PLINK   ——叮铃声
  - [官网](https://www.cog-genomics.org/plink/)- [Official Website](https://www.cog-genomics.org/plink/)
- PRSice
  - [Tutorial](https://choishingwan.github.io/PRSice/)- [教程](https://choishingwan.github.io/PRSice
- PGS with PLINK/PRSice-2/LDpred-2/lassosum使用 PLINK/PRSice-2/LDpred-2/lassosum 进行的全基因组选择（PGS）
  - [Tutorial](https://choishingwan.github.io/PRS-Tutorial/)- [教程](https://choishingwan.github.io/PRS-Tutorial
- [相关数据说明](data-description.md)- [Data Description](data-description.md)
## 方法模型及实现工具
- **Additive PGS Method** (P+T)- **加性 PGS 方法** (P T
  - PLINK   ——叮铃声
  - PRSice
- **Elastic Net PGS Method** (EN)弹性网络多基因评分法（EN）
  - SparSNPC   ——SparSNPC
- **Nultilayedered Perceptrons PGS Method** (MLP)多层感知器 PGS 方法（MLP）
  - Keras
  - Tensorflow   ——Tensorflow
  - Talos

## 相关资料
- [什么是多基因评分(Polygenic Scores)?](https://zhuanlan.zhihu.com/p/368701300), [英文版介绍](http://polygenicscores.org/explained/)- [What are Polygenic Scores?](https://zhuanlan.zhihu.com/p/368701300), [English Version Introduction](http://polygenicscores.org/explained/)
- [全基因组关联分析(Genome Wide Association Study)](https://baike.baidu.com/item/%E5%85%A8%E5%9F%BA%E5%9B%A0%E7%BB%84%E5%85%B3%E8%81%94%E5%88%86%E6%9E%90/9483732?fr=aladdin)- [Genome Wide Association Study (全基因组关联分析)](https://baike.baidu.com/item/%E5%85%A8%E5%9F%BA%E5%9B%A0%E7%BB%84%E5%85%B3%E8%81%94%E5%88%86%E6%9E%90/9483732?fr=aladdin
- [GWAS实验室](https://gwaslab.com/)- [GWAS Lab](https://gwaslab.com/)
  - 该网站发布了大量关于遗传统计学方面的学习笔记
- 多基因风险分数 PRS( Polygenic risk score)Polygenic risk score (PRS)
  - [系列之一：概念入门](https://zhuanlan.zhihu.com/p/396268778?ivk_sa=1024320u)- [Part One of the Series: Introduction to Concepts](https://zhuanlan.zhihu.com/p/396268778?ivk_sa=1024320u)
  - [系列之二：使用PLINK计算PRS（C+T方法）](https://zhuanlan.zhihu.com/p/401122336)- [Part Two of the Series: Calculating PRS (C T Method) Using PLINK](https://zhuanlan.zhihu.com/p/401122336)
  - [系列之三：使用PRSice计算PRS（C+T方法）](https://zhuanlan.zhihu.com/p/407548340)- [Series 3: Calculating PRS (C T method) with PRSice](https://zhuanlan.zhihu.com/p/407548340)
- [《统计遗传学：第五章 多基因得分(PGS)分析》](https://wenku.baidu.com/view/7a766a30f22d2af90242a8956bec0975f465a496?aggId=7a766a30f22d2af90242a8956bec0975f465a496&fr=catalogMain&_wkts_=1671794745568&bdQuery=Polygenic+scores+%28PGS%29)- [Statistical Genetics: Chapter 5 Polygenic Score (PGS) Analysis](https://wenku.baidu.com/view/7a766a30f22d2af90242a8956bec0975f465a496?aggId=7a766a30f22d2af90242a8956bec0975f465a496&fr=catalogMain&_wkts_=1671794745568&bdQuery=Polygenic%20scores%20%28PGS%29)
- [冯彦斌-项目笔记](https://www.mubucm.com/doc/rpvKpUCTCS)- [Feng Yanbin - Project Notes](https://www.mubucm.com/doc/rpvKpUCTCS)
## 相关文献
- GWAS的介绍[s43586-021-00056-9.pdf](https://github.com/user-attachments/files/22354252/s43586-021-00056-9.pdf)

## 团队成员
- 谌佳伟 24级研究生
- 康国胜 指导老师
- 徐&ensp;&ensp;宇 指导老师   Xu   Teacher Yu
