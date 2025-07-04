---
title: 'Theory about Making Friends'
date: "2023-12-29"
tags: ["Model", "Society", "Math"]
authors: ["Laplx"]
draft: false
---
{{< katex >}}
### 交友论

让我们从一个功利的视角建模人们怎么交友。评判朋友的价值可能非常不合适——不过毕竟连精神损失也可以经过鉴定来补偿一定的费用呢，这里姑且做个货币价值的量化，并按邪恶的经济学家们喜欢的方式假设一些理性人，他们打算最大化自己的效用啦。

\\(V_{ji}\\) 表示 \\(j\\) 对 \\(i\\) 而言的价值。我把朋友带来的价值简单的分为两部分：内在价值和外在价值。内在即心理价值，如倾诉、分享、玩乐，都满足了人一定的情感需求；外在即物质价值或现实价值，一般是帮忙或者所谓的”人情“。

\\(C_{ij}\\) 表示 \\(i\\) 对 \\(j\\) 付出的交友成本。不过这里的成本更加通用化，以具体事物作衡量，并不等同于某个人实际感受到的效用（比如对于社牛，可能他们专门出去找好友玩、参加联谊交往活动等并不会感觉有多心累或浪费时间精力）。

\\(\theta_{ji}\\) 表示 \\(j\\) 对 \\(i\\) 的亲密度。想了想我觉得不应直接假设 \\(\theta_{ji} = \theta_{ij}\\)，很可能双方对友谊的认知存在偏差。但或许对于情商高的人，他们能够更快的意识到差距并调整 \\(\left \vert \theta_{ji} - \theta_{ij} \right \vert\\) 趋于 0。\\(\theta\\) 取决于双方对友谊付出的成本多少，及环境外生的互动系数 \\(\mu_{ij} = \mu_{ji}\\)（不同来源性质的好友天生会产生亲密度的差别，比如中学里和同班同学的关系自然会高于一般的非同班同学）。而在某些特殊函数形式下可以造成 \\(\theta_{ji} = \theta_{ij}\\) ——接下来为了简单的解析结果，我们令 \\(\theta_{ji}(C_{ji},C_{ij},\mu_{ji}) = \mu_{ji} C_{ji} C_{ij}\\)。

内在价值可写为 \\(D_{ji}(\theta_{ij},d)\\)，其中 \\(d\\) 为情感偏好程度。令 \\(D_{ji} = d_i \theta_{ji}\\)。现实价值 \\(P_{ji}\\) 又怎么衡量呢？好友是一个期权。

等一下，这并不简单，这个期权不止是美式的，甚至不知道可能有哪些可以行权。再者，我们这里还需要两个假设：不考虑跨人际交往（”我朋友的朋友……“）；不考虑关系网的延伸（\\(i,j \in I\\) 均为已知的一群人）（理论上还应该考虑新认识陌生人可能的”启动成本“）。但我们这里稍稍不讲道理的简化一点，想象一群欧式期权，它们依 \\((S,K,T)\\) 联合概率分布，以表征不确定性。

\\(S\\) 指一些 issues in life（也许是一个向量），\\(K\\) 为使用好友这个”人情“（租）所需要付出的成本。不过这里应写为函数 \\(K_{ji}(\theta_{ji})\\)，令 \\(K_{ji} = (1-\theta_{ji})S_i + \theta_{ji}K_j\\)，\\(S\\) 是到期时的针对issue的花费。那么不难发现 \\(P_{ji}(\theta_{ji})  = \theta_{ji} S_i N(d_1) - \theta_{ji} K_j e^{-rT} N(d_2) = p_{ji} \theta_{ji}\\)，\\(V_{ji} = D_{ji} + P_{ji}  = v_{ji} \theta_{ji}\\)，价值正比于亲密度。

注意到这个式子需要存在交友无套利均衡（有点好笑），并且大家都能对 \\(K_i\\) 了解精准。

于是，最终的选择满足

$$
\max \limits_{\{C_{ji}\}} \sum \limits_{j \neq i} U_i(V_{ji}) - U_i(C_{ji})\\\
s.t. \ C_i = \sum \limits_{j \neq i} C_{ji}
$$

让我们来看一个经典的前景理论的情况，即

$$
U(x)=\left\{\begin{array}{cc}
x^\alpha & x \geq 0 \\\
-\lambda\left(-x\right)^\alpha & x<0
\end{array}\right.
$$

求解这个规划立刻得到 \\(C_{ji} \propto (R_{ji}^\alpha - \lambda_i)^{\frac{1}{1-\alpha}}\\)，其中 \\(R_{ji} = v_{ji} \mu_{ji} C_{ij}\\)，表征了好友 \\(j\\) 对 \\(i\\) 的价值比率。

概括一下主要思想：交友最终还是会达到边际投入等于边际产出；交友多的人无非是他们相对而言投入社交所需的成本小、回报高；交友成本将被更多的投入在高价值的人或爱社交的人身上；对于务实的人，\\(\alpha\\) 较大，或对于不爱社交的人，\\(\lambda\\) （社交厌恶的程度）较大，都会驱使 \\(R\\) 大的项更为突出，他们只会把精力投入到主要的人身上。

好吧，我们至少保证这个理论看上去符合直觉了！……

