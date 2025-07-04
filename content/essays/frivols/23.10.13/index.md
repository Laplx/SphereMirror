---
title: 'Stand up and Cheer'
date: "2023-10-13"
tags: ["Model"]
authors: ["Laplx"]
draft: false
---
{{< katex >}}
### 起立欢呼

（我在好多周前的栏目里似乎写过了关于复杂系统涌现的内容……这次又来说两句）

我去看亚运会，观众加油的气氛非常热烈，每每比赛关键时刻或运动员跑过看台前都会给予欢呼。但只有其中一场长跑，虽然没有我国运动员，观众却给出了相当热烈的反应——运动员跑到圈子哪边，那边的观众便会纷纷起立来加油——像波浪一样绕着场馆传递。很明显我想不是这场比赛多么与众不同，倒可能是某部分人先起立了，带动了其他人并潜意识的自动跟着跑步传递下去；我身边的观众虽然在远处起立潮渐近时露出了有点懵的神色但仍然迅速投入了欢呼状态……于是我也站起来了，接着是右边的。

这个现象留下了比较深的印象。很简单的设想，我们每个人有一个起立欢呼的阈值 \\(T\\)，视野范围内受到激发即起立的人比例为 \\(k\\)，自己心里有对比赛质量的偏好 \\(Q\\)；通过一个合适的（群体分布的）考量函数

$$
f(k,Q)+\epsilon,\text{ where }\epsilon \text{ is a random deviation}
$$

其与阈值 \\(T\\) 的大小关系决定了是否鼓掌。再进一步，我们还应该考虑友伴效应——大家总是三五成群跟自己熟悉人落座——亲人的起立行为对你的影响想必大很多。那么我们需要一个预先置好的人群结构 \\(w\\)，\\(w(x,y)\\) 表示 \\(x\\) 的行动对 \\(y\\) 行动的影响权重，且 \\(w(x,y)=w(y,x)\\)。还可以把欢呼和起立分开作为两个变量。（不过对于比赛这里没有考虑到运动员位置这个决定性因素。）

总之，一个起立欢呼模型 \\((I,Q,T,w)\\) 其中 \\(Q\\) 和 \\(T\\) 为定义在参与空间 \\(I\\) 上的函数，\\(w: I \times I \rightarrow \mathbb{R}\\)。场 \\(F: I \rightarrow \mathbb{R}^n\\) 表示了各人的相应情况（鼓掌程度之类的）。我们可以试着作一个演化方程：

$$
\frac{d}{dt}F(x,t) = \tau Q(x)\int \limits_{I} w(y,x)F(y,t)dy
$$

如果 \\(w\\) 恰好是有意思的欧式距离平方反比，那么（怎么解呢？）

$$
\nabla \cdot \frac{F'}{Q} = \kappa F
$$

（如上所述，还可以加入随机性 \\(\epsilon \sim N(0,\sigma^2)\\)）

让我突然想起今天讨论课出现的经典情形：一间教室大家叽叽喳喳一段时间之后总会突然安静上几秒，如此往复。这件事同样很有意思，每个人都在讲了一段时间后暂时无话可说，一旦突破一个阈值，这片安静就会迅速扩散开来，模型基本就是上式。

（说到群体行为，Schelling 有不少出色的模型。以及 NetLogo，作为较不错的复杂系统仿真软件，中文资料却相对缺乏，或许什么时候可以出一份它的简单讲义……画饼ing）

**插播：Shut up the Mouse**

发现自习教室里有机械键盘和机械鼠标声，愈听愈响，难以思考（虽然没什么问题，但很多事就像曼昆所说的那样——飞机靠背往后放是前座的权利还是保有正常空间是后座的权利？），于是打算换一间。突然想到：如果当我走进一个教室，里面已经多一些人入座了且没有使用机械鼠标时，是不是意味着坐在这间教室之后碰到咔咔声的概率要小一些呢？