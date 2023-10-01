# scTools
Array of Single-cell Tools
## Here is the collections of single-cell Tools
https://github.com/seandavi/awesome-single-cell
### scBridge
[scBridge embraces cell heterogeneity in single-cell RNA-seq and ATAC-seq data integration](https://www.nature.com/articles/s41467-023-41795-5): A multi-omics data integration method (dubbed scBridge) that integrates cells in a heterogeneous manner.
![image](https://github.com/wbszhu/scTools/assets/48794258/9bb00fc5-0ef0-4de3-9f60-404a65e4e218)

**scBridge是一个数据集成和标签转移工具，用于整合具有注释的单细胞RNA测序数据和未标记的单细胞ATAC测序数据。它通过深度神经网络编码器和分类器进行数据集成和标签传递。主要步骤如下：**

**a. 数据输入和初步处理：** scBridge的输入包括带注释的单细胞RNA测序数据和未标记的单细胞ATAC测序数据。这些数据经过处理后传入深度神经编码器和分类器。

**b. 初始化神经网络：** scBridge利用已注释的单细胞RNA测序数据预先训练深度神经编码器和分类器，为后续处理做准备。

**c. 评估ATAC细胞的可靠性：** 根据ATAC细胞的嵌入区分能力和分类损失，scBridge对每个ATAC细胞的可靠性进行建模。

**d. 计算ATAC原型和整合：** 基于估算的可靠性，scBridge计算ATAC原型作为加权平均值，并将其与RNA原型对齐以实现数据集成。

**e. 整合可靠ATAC细胞并更新标签：** 在每次迭代的末尾，scBridge选择最可靠的ATAC细胞并将其合并到已注释数据中，同时使用当前预测为其分配标签。

整个过程通过**重复步骤b到e直至收敛**，使得越来越多的ATAC细胞得以整合，从而实现最终的数据集成和标签转移结果。这个工具帮助将ATAC测序数据与RNA测序数据相结合，为细胞类型分析提供了有力支持。
