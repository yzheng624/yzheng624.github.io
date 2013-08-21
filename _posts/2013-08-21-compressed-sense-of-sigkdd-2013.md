---
layout: post
title: "Compressed Sense of SIGKDD 2013"
description: ""
category: 
tags: []
---
{% include JB/setup %}

很幸运地在学院的资助下赴 Chicago 参加了 [SIGKDD 2013](http://www.kdd.org/kdd2013/) 学术会议。
可惜的是，一是我校今年 SIGKDD 居然一篇未中！所以我校几乎没有什么教师和博士生参加 SIGKDD（但还是幸运地遇到了吴老师），但水水的本科生却来了有十多个。再有就是发现自己的学到的东西还差得远，Crompressed Sensing, MCMC 什么的之前从来没有听说过，对 SVM 的理解也不够深，别人的 slides 里加几个限制就几乎跟不上了，要好好学学 SVM 和最优化了。

下面就开始随便聊聊那几天的所见所闻了，大概会有很多错误，毕竟我只是个刚刚读完大学二年级的本科生。

### Day One

激动地用蹩脚的英语和服务人员领完证明自己身份的牌子之后就开始了激动的第一天。
至于听哪个 workshop，有什么好说的，当然是去听 [Jiawei Han](http://www.cs.uiuc.edu/~hanj/) 啦！

#### From Social Networks to Heterogeneous Social and Information Networks: A Data Mining Perspective [slides](http://www.ccs.neu.edu/home/yzsun/Tutorials/ASONAM12_tuto_online.pdf)

Heterogeneous Information Network 是最近比较火领域，这种火热得益于 Jiawei Han 的得意门生，去年刚博士毕业就在 Northeastern University 做 Assistant Professor 的 [Yizhou Sun](http://www.ccs.neu.edu/home/yzsun/)。据 Jiawei Han 说，Yizhou Sun 是北大统计系、计算机系双学位，来到 UIUC 之后也在上统计的课程，而且分数全都是 A，所以总能把统计那边有趣的方法施加于 Machine Learning, Data Mining 之上。幸好之前做 SRTP 时接触过和 Heterogeneous Information Network 相关的内容，也读过 [RankClus](http://www.cs.uiuc.edu/~hanj/pdf/edbt09_ysun.pdf) 的那篇论文，Jiawei Han 也确实是一个好老师，语气、语调、停顿、重音，无不处理地相当精彩。Jiawei Han 能在繁忙的研究工作中腾出时间来练习讲课，为什么国内的一些教师讲课却简直没法听。

之后就是按照 Yizhou Sun 的发的论文的时间顺序开始讲。主要分为以下几个部分：

RankClass,
Meta-Path,
Meta Similarity,
PathPredict (using meta path),
Classification (using label)

有兴趣的可以去看 slides 和对应的论文，我也就不赘述了。

#### Large Graph Mining – Patterns, tools and cascade analysis [slides](http://www.slideshare.net/BigDataMining/large-graph-mining-patterns-tools-and-cascade-analysis-by-christos-faloutsos)

之前没有接触过 Large Graph 方面的内容，来自 CMU 的 speaker 的口音也比较重，所以只能模模糊糊地听出他的方法大概是什么，但细节什么的就不清楚了。

大概先讲了真实世界的 Graph 会服从的 Power Laws, Triangle Law，然后又说了是因为 self-similarity 才有如此多的 power-laws。那么我们如何运用 self-similarity 来生成一个符合 power law 的 Large Graph 呢？那就可以用分型（fractals）的方法，speaker 举了 Kronecker Graphs 的例子用以说明。

### Day Two

### Day Three

### Day Four