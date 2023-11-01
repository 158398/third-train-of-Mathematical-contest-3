# third-train-of-Mathematical-contest-3
记录数模第三次训练的代码，包括图片，思路和tex代码
# 问题分析
2021年美D题，这道题主要是关于图方面的题，可以说是几次模拟里我们最满意的一次，我们在Pagerank算法中建立了一个加权有向图模型，允许用数值方法测量艺术家的影响。每条边的权重由Pagerank算法和两位艺术家来定义，为了避免不同特征的大小的影响，我们对它们进行了归一化，并使用改进的Tanimoto系数组合权重，可以通过随机森林计算来度量相似度。我们在前一篇论文中应用了相似度度量模型对艺术家和流派进行分析。首先，通过对歌曲特征的分析，得到了识别体裁的重要特征，然后总结了体裁之间的相似性和关联性。我们将特征转换为五类，分别是节奏、能量、情感、抒情诗、旋律，每一类都代表了歌曲的一个方面，并创建它们来分析影响。
# 算法分析
我们的框架采用了网络搜索中常用的PageRank算法，综合考虑了音乐家在所有音乐家之间的关系，对所有音乐家进行排序，允许我们评估音乐家的历史状况。对于所有的音乐特性，我们设计了一个相似度算法基于谷本系数评估歌曲或音乐家之间的相似度，考虑到不同的特性代表不同方面但有相似性在某种程度上，我们添加了一个加权方法基于随机森林模型的算法。即根据信息最大的原理，利用随机森林算法得到权值。每一种音乐的乐器性、能量性、声学性等特征都被转化为音乐的节奏特征、能量特性等。它们代表了音乐的不同方面。更重要的是，我们还设计了一种特殊的算法，使用原始数据来计算音乐的每五个特征的大小，如果两种音乐具有相似的类别特征，就可以证明它们在这个特征上是相似的。音乐的这种特征被量化为一个五维向量。我们将音乐、类型和时间的数量组合成一个统计序列。通过滑动窗口t检验方法，我们能够观察到音乐变化的趋势，然后结合音乐数据的发布，分析了音乐、音乐家和流派之间的关系。我们发现，能量和情感的两个特征随着时间的推移而显著变化，反映了该类型的演变。我们用岭回归模型来表征这种动力学。此外，我们还考察了音乐特征、创作数量、在该流派中持续创作的艺术家受欢迎程度的变化，从而理解音乐家的发展。我们的模型还能够进一步发现音乐家之间的深层关系，计算统计数据，发现音乐革命等。利用PageRank算法、随机森林模型、回归模型模型，提出了系数加权校正，评价音乐特征和相似性模型，建立符合音乐特征可以反映不同音乐特征的差异和统一性，具有较强的科学性和可靠性。这些模型为利用音乐特征数据进行音乐特征分析提供了很好的参考，并可进一步应用于未来的音乐分析。
<br>
在我们的模型中，与行走过程中经常访问的节点相对应的艺术家可以被视为一个重要的影响者，因为许多其他艺术家可以通过定向边追溯到这个影响者，这表明他直接或间接地影响了许多人。从图中提取了最具影响力的艺术家组成的子图，因为这些艺术家非常有影响力，他们之间有价值的影响关系。我们根据子图中的拓扑顺序对图进行了分层。从图1中可以看出，十位有影响力的艺术家之间存在明显的分层结构，显示了他们之间影响关系的层次。
# 文章总结
- 假设没有论证
- 变量命名差
- 无影响深刻的图
- 指标整合差
- 文章刻意的长句太多，难以读懂
- 表格的标题应该在上方
- 因素结果可视化能力差，分析不足
- 摘要排版间距
- 大段大段的文字太多太长
