
# Data Description
- [HAPGEN](#HAPGEN)
- [PLINK](#PLINK)
- [IMPUTE2](#IMPUTE2)
- [PRSice](#PRSice)


# <span id="HAPGEN">HAPGEN</span>
-[.haps](https://www.cog-genomics.org/plink/2.0/formats#haps)
### \*.haps--input file & output file 
|column| descrption|
|:----  |:----  |
|第1列|  每个 SNP 一行，每个单倍型一列，0、1表示等位基因编码|

### \*.leg--input file & output file
-[.leg](https://www.cog-genomics.org/plink/2.0/formats#legend)
|column| descrption|
|:----  |:----  |
|rs| SNP标识符，用于在不同研究之间对位点进行比较|
|position| 每个 SNP 的碱基对位置，通常以基对（bp）为单位表示|
|x0| 等位基因1，A、G、C、T表示|
|x1| 等位基因2，A、G、C、T表示|

### \*.legend--input file & output file
-[.legend](https://www.cog-genomics.org/plink/2.0/formats#legend)
|column| descrption|
|:----  |:----  |
|rs| SNP标识符，用于在不同研究之间对位点进行比较|
|position| 每个 SNP 的碱基对位置，通常以基对（bp）为单位表示|
|x0| 等位基因1，A、G、C、T表示,通常是次要的|
|x1| 等位基因2，A、G、C、T表示,通常是主要的|

### \*.map--input file

-[.map](https://www.cog-genomics.org/plink/2.0/formats#map)
|column| descrption|
|:----  |:----  
|position| 染色体位置，这一列表示每个位点在基因组上的物理位置，通常以单位为bp（碱基对）表示。物理位置是基于基因组序列的，因此它不受遗传连锁关系的影响|
|COMBINED_rate(cM/Mb)| 标记右侧的以 cM/Mb 为单位的速率|
|Genetic_Map(cM)| 标记左侧的以 cM 为单位的累积速率|


### \*.gen--output file
-[.gen](https://www.cog-genomics.org/plink/2.0/formats#gen)
|column| descrption|
|:----  |:----  |
|SNPID| SNP位点标识符，标识作用|
|rsID| rsID，主要变体ID|
|BP| 碱基对坐标，SNP位点在基因组上的位置|
|A1| 等位基因，以A、G、C、T进行等位基因1、2的标识|
|A2| 等位基因，以A、G、C、T进行等位基因1、2的标识|
|第6列| 单个SNP位点的等位基因情况在N个样本中的信息|
|第n列|同第6列|

   
### \*.sample--output file
-[.sample](https://www.cog-genomics.org/plink/2.0/formats#sample)
|column| descrption|
|:----  |:----  |
|ID_1| 家庭ID，通常是一个数字或字母编号，用于标识家庭|
|ID_2| 家庭内ID，通常也是一个数字或字母编号，用于标识每个个体|
|missing| 该样本是否缺失数据的标志，通常用0或1表示，0表示数据完整，1表示数据缺失|
|sex| 性别代码（'1' = 男性，'2' = 女性，'0' = 未知）|
|pheno| 表型，'0' = 对照，'1' = 病例）或连续表型|


### \*.tags--output file
-[.tags](https://mathgen.stats.ox.ac.uk/genetics_software/hapgen/hapgen2.html#:~:text=will%20be%20outputted.-,%2Dt%20%3Cfile%3E,-Optional)
|column| descrption|
|:----  |:----  |
|第1列|  SNP 子集文件，标记的物理位置，与图例文件中的相匹配。|

# <span id="PLINK">PLINK</span>
### \*.QC--input file
|column| descrption|
|:----  |:----  |
|CHR| 位点所在的染色体编号|
|BP| 碱基对坐标|
|SNP| 单核苷酸多态性（SNP）标识符|
|A1| 主要等位基因（major allele)|
|A2| 次要等位基因（minor allele）|
|N| 该位点的样本数|
|SE| 该位点的标准误差（standard error）|
|P| 评估该位点与研究特征之间的关联程度|
|OR| 用于评估该位点与研究特征之间的关联程度|
|INFO| 该位点的信息度，用于评估该位点的质量和可靠性，正相关|
|MAF| 次要等位基因在样本中的出现频率。|
### \*.bed--input file

-[.bed](https://choishingwan.github.io/PRSice/prset_detail/#bed-files)
|column| descrption|
|:----  |:----  |
|第1列| 位点所在的染色体编号|
|第2列| 染色体或支架中特征的起始位置,染色体中的第一个碱基编号为0|
|第3列| 染色体或支架中特征的结束位置|





### \*.map--input file

-[.map](https://www.cog-genomics.org/plink/2.0/formats#map)
|column| descrption|
|:----  |:----  |
|position| 染色体位置，这一列表示每个位点在基因组上的物理位置，通常以单位为bp（碱基对）表示。物理位置是基于基因组序列的，因此它不受遗传连锁关系的影响|
|COMBINED_rate(cM/Mb)| 标记右侧的以 cM/Mb 为单位的速率|
|Genetic_Map(cM)| 标记左侧的以 cM 为单位的累积速率|

### \*.bim--input file
-[.bim](https://www.cog-genomics.org/plink/2.0/formats#bim)
|column| descrption|
|:----  |:----  |
|第1列| 染色体编号，可以是任意字符串|
|第2列| SNP标识符，可以是任意字符串|
|第3列| 遗传距离，单位为摩根，一般为0|
|第4列| 物理位置，单位为bp（碱基对），一般为实际的基因组物理位置|
|第5列| 等位基因1的名称，一般为字母或数字，通常为次要|
|第6列| 等位基因2的名称，一般为字母或数字，通常为主要|

### \*.fam--input file
-[.fam](https://www.cog-genomics.org/plink/2.0/formats#fam)
|column| descrption|
|:----  |:----  |
|第1列| 家系ID，可以是任意字符串|
|第2列| 个体ID，可以是除‘0’外的任意字符串|
|第3列| 父亲ID，如果没有父亲数据，则为0|
|第4列| 母亲ID，如果没有母亲数据，则为0|
|第5列| 性别，1表示男性，2表示女性，0表示未知|
|第6列| 出生日期，格式为YYYYMMDD，如果未知，则为0|


### \*.clumped--output file
-[.clumped](https://www.cog-genomics.org/plink/1.9/formats#clumped)
|column| descrption|
|:----  |:----  |
|CHR| 该位点所在的染色体编号|
|F| 该位点与最显著信号的关联程度，即该位点的LD值|
|SNP| 该位点的单核苷酸多态性（SNP）标识符|
|BP| 碱基对坐标|
|P| 该位点的P值，用于评估该位点与研究特征之间的关联程度|
|TOTAL| 在该位点的LD窗口内共有多少个位点|
|NSIG| p ≥ 0.05 的聚集变体数|
|S05| 聚类变体的数量，其中 0.01 ≤ p < 0.05|
|S01| 聚类变体的数量，其中 0.001 ≤ p < 0.01|
|S001| 聚类变体的数量，其中 0.0001 ≤ p < 0.001|
|S0001| 聚类变体的数量，P值低于0.0001|
|SP2| p < --clump-p2 阈值的成员的逗号分隔 ID 和文件编号|

# <span id="IMPUTE2">IMPUTE2</span>
### \*.vcf--input file
-[.vcf](https://www.cog-genomics.org/plink/1.9/formats#vcf)
|column| descrption|
|:----  |:----  |
|CHR| 染色体编号，例如 "1"、"2"、"X" 等|
|POS| 位点位置，即在染色体上的位置|
|REF| 参考等位基因，即在参考基因组中所定义的该位点的碱基|
|ALT| 可变等位基因，即在该位点上存在的其他可能的碱基|
|QUAL| 质量分数，表示该位点的可靠程度|
|FILTER| 过滤标记，表示该位点是否通过了质量控制|
|INFO| 包含了一系列的注释信息，例如变异类型、功能影响、频率等|
|FORMAT| 格式标记，表示后续的样本数据的格式。|
|第9列| 样本数据列，包含了每个样本在该位点上的基因型信息，例如 "0/1" 表示该样本的两个等位基因分别为参考等位基因和可变等位基因。这些样本数据列的列名即为样本的编号。|
|第n列| 同第9列|

### \*.haps--output file
-[.haps](https://www.cog-genomics.org/plink/2.0/formats#haps)
|column| descrption|
|:----  |:----  |
|第1列|  每个 SNP 一行，每个单倍型一列，0、1表示等位基因编码|

### \*.leg--output file
-[.leg](https://www.cog-genomics.org/plink/2.0/formats#legend)
|column| descrption|
|:----  |:----  |
|rs| SNP标识符，用于在不同研究之间对位点进行比较|
|position| 每个 SNP 的碱基对位置，通常以基对（bp）为单位表示|
|x0| 等位基因1，A、G、C、T表示|
|x1| 等位基因2，A、G、C、T表示|


# <span id="PRSice">PRSice</span>


### \*.QC--input file
|column| descrption|
|:----  |:----  |
|CHR| 位点所在的染色体编号|
|BP| 碱基对坐标|
|SNP| 单核苷酸多态性（SNP）标识符|
|A1| 主要等位基因（major allele)|
|A2| 次要等位基因（minor allele）|
|N| 该位点的样本数|
|SE| 该位点的标准误差（standard error）|
|P| 评估该位点与研究特征之间的关联程度|
|OR| 用于评估该位点与研究特征之间的关联程度|
|INFO| 该位点的信息度，用于评估该位点的质量和可靠性，正相关|
|MAF| 次要等位基因在样本中的出现频率。|

### \*.bed--input file & output file
-[.bed](https://choishingwan.github.io/PRSice/prset_detail/#bed-files)
|column| descrption|
|:----  |:----  |
|第1列| 位点所在的染色体编号|
|第2列| 染色体或支架中特征的起始位置,染色体中的第一个碱基编号为0|
|第3列| 染色体或支架中特征的结束位置|

### \*.bim--input file & output file
-[.bim](https://www.cog-genomics.org/plink/2.0/formats#bim)
|column| descrption|
|:----  |:----  |
|第1列| 染色体编号，可以是任意字符串|
|第2列| SNP标识符，可以是任意字符串|
|第3列| 遗传距离，单位为摩根，一般为0|
|第4列| 物理位置，单位为bp（碱基对），一般为实际的基因组物理位置|
|第5列| 等位基因1的名称，一般为字母或数字，通常为次要|
|第6列| 等位基因2的名称，一般为字母或数字，通常为主要|

### \*.fam--input file & output file
-[.fam](https://www.cog-genomics.org/plink/2.0/formats#fam)
|column| descrption|
|:----  |:----  |
|第1列| 家系ID，可以是任意字符串|
|第2列| 个体ID，可以是除‘0’外的任意字符串|
|第3列| 父亲ID，如果没有父亲数据，则为0|
|第4列| 母亲ID，如果没有母亲数据，则为0|
|第5列| 性别，1表示男性，2表示女性，0表示未知|
|第6列| 出生日期，格式为YYYYMMDD，如果未知，则为0|

### \*.height--input file
|column| descrption|
|:----  |:----  |
|FID| 家系 ID，表示样本所属的家庭或群体|
|IID| 个体 ID，表示样本的唯一标识符|       
|Height| 身高数据，表型数据与基因型数进行关联分析|
### \*.covariate--input file
-[.cov](https://www.cog-genomics.org/plink/2.0/formats#cov)
|column| descrption|
|:----  |:----  |
|FID| 家系 ID，表示样本所属的家庭或群体|
|IID| 个体 ID，表示样本的唯一标识符|
|Sex| 个体的性别,协变量|


### \*.assoc--output file
-[.assoc](https://www.cog-genomics.org/plink/1.9/formats#assoc)
|column| descrption|
|:----  |:----  |
|SNP| SNP位点的标识符|
|CHR| 该位点所在的染色体编号|
|BP| 碱基对坐标|
|A1| 该位点的第一等位基因（通常次要）|
|A2| 该位点的第二等位基因（通常主要）|
|P| 该位点的 P 值，表示该位点与表型数据之间的关联程度|
|OR| 几率（等位基因 1 | 病例）/几率（等位基因 1 | 对照）|
### \*.pheno--output file
  
|column| descrption|
|:----  |:----  |
|FID| 家系 ID，表示样本所属的家庭或群体|
|IID| 个体 ID，表示样本的唯一标识符|
|Pheno| 表型数据，通常是身高、体重、疾病等|


### \*.best--output file
-[.best](https://choishingwan.github.io/PRSice/step_by_step/#scores-for-each-individual:~:text=the%20Null%20model-,Scores%20for%20each%20individual,-A%20file%20containing)
|column| descrption|
|:----  |:----  |
|FID| 家系 ID，表示样本所属的家庭或群体|
|IID| 个体 ID，表示样本的唯一标识符|
|In_Regression| 是否被包括在回归分析。1已被纳入回归分析；0未被纳入回归分析|
|PRS| 个体多基因风险评分|

