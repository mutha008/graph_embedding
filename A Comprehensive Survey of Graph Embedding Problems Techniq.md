## A Comprehensive Survey of Graph Embedding: Problems, Techniques and Applications

ge = graph embedding

2000年早期，ge算法侧重数据降维

2010年后，1、专注用向量表达图的一部分； 2、向量表达图的全貌



ge主要有两个研究问题：

1、图分析： 挖掘有用的信息

2、表达学习：如何表达易于抽取信息

实际上，用低维的向量去表达一个图，并且保留图的结构



问题定义：

1、embedding input :  同构图、异构图、带属性图、非关系图

2、embedding output：任务驱动；点emb、边emb、混合emb、全图emb



定理：

1、同构图： 所有边和点的类型必须只有一个

2、异构图： 边或点的类型只要大于一个即可

3、三元组（head entity, relation, tail entity）

4、两个节点的一阶相似是边的权重

5、两个节点的二阶相似是节点的邻居相似度



embedding input

1、同构图： 有向、无向；有权重、无权重

​	palapala引用了一堆论文

2、异构图：

​	三种场景：

- 问答类的社区：问题、答案、用户
- 多媒体网络
- 知识图谱

3、带属性图

- 标签：type
- 属性：数值，离散或者连续
- 节点特征：文本或向量
- 信息传播：类似微博中的转发
- 知识库



embedding output

1、点：一阶相似度、二阶相似度

​	难题：定义点相似度的方法

2、边：比如知识图谱中三元组预测，用于链接预测、关系预测

​	难题：边相似度定义，建模边的属性

3、混合：点+边 、 点 + 社区

4、全图：



相关技术

1、矩阵分解 

​	输入： 无关系图  输出：点embedding

- 拉普拉斯特征映射
- Node Proximity Matrix Factorization




2、deep learning

- deep walk  
  - 输出采用了softmax，考虑到性能，采用了两种方法