---
title: 'Introduction to Roll Theory'
date: "2023-05-26"
tags: ["Society", "Math"]
authors: ["Laplx"]
draft: false
---
{{< katex >}}
### 选课学导论

（或许可以更广一些，所有带有一定公开机制、多人参与、多个选项且选项非全同的 game 都属于摇号论 roll theory 的研究范围，如房地产摇号、购车摇号、升学摇号等等）

鉴于🥚的绩点制度（省略一万字），如何选好课对于🥚的学生来说显得尤为重要。按照我目前（完全不成熟）的理论，分为三轮的选课只讨论第一轮。第二轮主要是开始那一刻一哄而上（可以视为是一种无 opening 的 roll，roll 的是网速），跟第三轮一样都有容量人数限制，不存在 roll 的过程。

这里空间太小，我只分享一些最初的想法。我们把一轮选课的 roll 机制视作单次的等注的完全的可以无限更改的 roll（必修课的模型符合程度会更高，毕竟有些选修课可能最后直接就不上了），每个人有一个预先的知识/信息（这个老师怎么样？）\\(u_{0i}\\) 表示\\(i\\)从1到n的所有 choices 的 priori scores，在 opening 即信息公开、众人博弈阶段的人数和课程容量分别为 \\(x_i\\) 和 \\(c_i\\)，这个预选概率为 \\(p_i = c_i / x_i\\)（可以大于1），它同样对决策起到影响——信息既有自己找的，也有通过人数反映的（从众？）——很明显不同人对二者偏倚程度不同，给出一个 \\(s\\) 以描述偏向 \\(p_i\\) 的程度。那么 posteriori scores 可以是一个函数 \\(f(u_{0i},p_i,s)\\) ，它带来的预期收益还要乘以roll上概率的作用——按照行为心理学（行为经济学），来一个概率加权函数 \\(P(p_i)\\) 是比较合适的（具体形式自行参考），如果简便起见直接理性人假设（大学选课还算接近？）那么就等于 \\(p_i\\)。\\(f(u_{0i},p_i,s)\\) 我暂时未经考证的猜测作 \\(f = u_{0i}^{1-s} p_i^s\\)。

那么每个人可以近似的认为追求效用最大化 \\( u_i = f(u_{0i},p_i,s) P(p_i)\\)（注意乘法是未经考虑的），\\(\mathop{max}\limits_i \ u_i\\) 的 choice \\(i = i^*\\)。进一步如果时间足够，可以解出群体的稳态解（或许不止一个）并视为达到稳态。

一些同样非常重要的现象和问题，它们将继续理论的发展：

- 往往最后几个小时选课情况会出现大幅度波动，相当一部分人在最后才来选课，也有一部分人在最后同时做了调整。
- 课程以中间人数出现的时候不多（尤其是通选课等人数池大得多的），要么一般少，要么达到一定数量后迅速收敛到接近满员的状态。
- 人数分布是否反映了老师的受欢迎或课的优秀程度？如果有错位，机制如何？
- 不少学校应该可以加权下注，这个问题更加有趣。