---
title: 'Model for the Nations'
date: "2023-11-24"
tags: ["Model", "Society", "Economy"]
authors: ["Laplx"]
draft: false
---
{{< katex >}}
### 国际关系模型

我想依葫芦画瓢构建一个类似于凯恩斯框架下的简单模型去描述国际关系，方法就是把最原始的宏观经济模型稍作无厘头的扩展。\\(r_{ij}\\) 表示国家 \\(i\\) 和国家 \\(j\\) 的国际出清关系（International Clearing Relationship，ICR），\\(r\\) 越大（姑且作一标量）关系越正面。（这也许可以计量，比如通过文本分析和情感分析，可以构造并量化国家之间官方媒体互相报道或高层互动事件的一个关系指数）

我们要多引入一些将被考虑的内生和外生变量，它们有一些类似于模块化拼装，可以纳入也可能在考察后认为不足轻重而舍去。除了熟知的 \\(Y\\) 产出、\\(A\\) 技术（这里将科教研究水平与技术合一视之了）、\\(C\\) 消费、\\(P\\) 价格水平、\\(T\\) 税收（及其它强制扭曲）等总量以外，我们还有 \\(D\\) 文化富合度（Cultural Affluence）（正面反映了闲暇和文娱时间；同时负向描述了种族、宗教冲突的程度）、\\(W\\) 民众福利（Welfare）、\\(M\\) 武装力量（Millitary Power）、\\(U\\) 意识介度（Consciousness Dissemination）（指出社会意见和思想的传播程度或多元程度；同时一定的反映政权或宣传机器的把控力量）等。还要介绍的有 \\(ID\\) 政治位移（Ideology），不称意识形态的原因是它可以不仅仅是衡量左右，而是一个可以在设定的多个意识评价标准下的多维空间里移动的一个矢量，其决定了政治和经济制度，特别反映在产权组织 \\(PI(ID)\\) 上（跟政府架构等有关，但核心归于 \\(ID\\)）。\\(PI\\)（Property Inequality）将政治光谱（空间）划分开来（或连续化），表示了“生产关系”（比如可以粗分为资本主义、社会主义等）及其导致的分配关系。再如 \\(U\\) 应该也与 \\(ID\\) 有关。

模型的假设（缺陷）包括：

- 市场化（may not be free markets but there must exists an adjusting power not controlling）
- 不考虑预期，且无理性预期（no long-term expectation）
- 仅宏观政策（macroscopic open actions 即没有微观或暗面的操作，如针对个别企业的制裁或间谍行为）
- 无随机扰动（no stochastic terms 不包含概率成分，没有影响国际关系的黑天鹅事件）
- 不考虑能源、移民、生态环境等其他重要因素（only has political interest and economic interest / no key mesoscopic factors 不考虑关键中观领域的作用）
- 无阶层分化（no hierarchy 尽管有 PI 且纳入了分配结构，但并未分群体建模）

影响国家决策的无非是两个方面：一边讲发展，一边要安全（就像投资决策的 \\(\mu\\) 和 \\(\sigma\\) 那样）。或者说，国际关系无非是 Benefit 和 Security 的综合作用（Inner & Outer）。不过我们这里要把原来的 IS-LM-BP model 说的详细一些，把 \\(NX\\) 拆开写为 \\(NX_{ij}(e_{ij},Y_i,Y_j,r_{ij})\\) 表示 \\(i\\) 国向 \\(j\\) 国的净出口。即有 \\(NX_{ij}(e_{ij},Y_i,Y_j,r_{ij})\\) \\(=\\) \\(KF_{ij}(i_i,i_j,K_i,K_j,r_{ij})\\)。注意实际上我们应分写进口 \\(IM\\) 和出口 \\(EX\\) 函数，鉴于双向大量贸易和几乎不贸易在净值上无法区别。总而言之：

$$
Y(L,K,A) = C(Y,\dot{Y},i,T,PI) + I(i,T) + G + NX \tag{IB}
$$

$$
NX(e,Y,r,T) = KF(i,K) \tag{OB}
$$

$$
PO(U,D,W,G_{S},ID) = RE(T,G,Y) \tag{IS}
$$

$$
DT(M,\epsilon,r,ID) = M(G_M,A) \tag{OS}
$$


其中政府开支（外生，但准确来说应受到 \\(PI\\) 制约）\\(G = G_N + G_M + G_A + G_D + G_{S} + G_O\\) ，包括民生、军备、科技、文化、治安及其他不纳入模型的经常性开支 \\(G_O\\)（建设性投资等资本积累已计入 \\(I\\) 中）。\\(DT\\) 即 Deterrence 他国的威慑作为外部安全的需求函数；\\(\epsilon_{ij}\\) 为地缘因子 Geographic factor，表示相互军事力量的威胁程度（当有海外军事基地部署时，\\(\epsilon_{ij} \neq \epsilon_{ji}\\)）（“一切政治首先是地缘政治”）；\\(\lVert ID_i-ID_j \rVert\\) 为可能存在的非主要影响因素。\\(PO\\) 即 Public Order 为内部安全供给，受到包括群众福利在内的多变量影响；\\(RE\\) 即 Regime Exertion 公权力的行使，准确来说应写为各不同部分收支的函数（拆分 \\(G\\)、\\(T\\)，如转移支付、价格管制等），表示内部安全需求。


ICR 需要各国的利益与安全同时出清。

当然，我们还可以纳入增长，要为其他几个变量刻画动态，完善方程组：

$$
\frac{MS}{P} = LQ(i,Y,e,\dot{P}) \tag{LM}
$$

$$
W(C,U,D) = WA(Y,PI,G_N) \tag{SW}
$$

分别代表了流动性均衡与社会福利均衡。（\\(MS\\) 为货币供给。\\(WA\\) 为 Wealth Allocation 财富分配，以提供福利；同时我们默认储蓄对福利的增量很小）其实应设计要素均衡 \\((PF)\\)，如劳动力所有者收入。

$$
\begin{equation}
\tag{XG}
    \begin{split}
    & \dot{L} = \dot{L}(\dot{Y},\dot{P},L,N,D)\\\
    & \dot{K} = I + KF - \delta_K K\\\
    & \dot{A} = \dot{A}(G_A,I,L,A)\\\
    & \dot{N} = \dot{N}(\dot{W},N,\delta_N)\\\
    & \dot{D} = \dot{D}(G_D,I,N,D,U)
    \end{split}
\end{equation}
$$

（其中 \\(\delta_K\\) 为资本折旧率，\\(\delta_N\\) 为死亡率。\\((XG)\\) 增长部分等式并未严谨考量变量）

以上各函数关于各变量偏导的符号自行推断（因此可假设一些简单的数学形式）。篇幅有限（欢迎来讨论 \\(D\\) 和 \\(U\\) 这些变量的问题），就不介绍实例了。（不妨看看朝鲜半岛？这个模型告诉我们会出现南北分立的 buffer contries 吗）

如果你愿意的话，可以叫它 “Chen Model” 或者 BIOS（笑）。