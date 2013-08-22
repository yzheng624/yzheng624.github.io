---
layout: post
title: "Compressed Sense of SIGKDD 2013"
description: ""
category: 
tags: []
---
{% include JB/setup %}

很幸运地在学院的资助下赴 Chicago 参加了 [SIGKDD 2013](http://www.kdd.org/kdd2013/) 学术会议。
可惜的是，一是我校今年 SIGKDD 居然一篇未中！所以我校几乎没有什么教师和博士生参加 SIGKDD（但还是幸运地遇到了吴老师），但水水的本科生却来了有十多个。再有就是发现自己的学到的东西还差得远，Crompressive Sensing, MCMC 什么的之前从来没有听说过，对 SVM 的理解也不够深，别人的 slides 里加几个限制就几乎跟不上了，要好好学学 SVM 和最优化了。

下面就开始随便聊聊那几天的所见所闻了，大概会有很多错误，毕竟我只是个刚刚读完大学二年级的本科生。

### Day One

激动地用蹩脚的英语和服务人员领完证明自己身份的牌子之后就开始了激动的第一天。
至于听哪个 workshop，有什么好说的，当然是去听 [Jiawei Han](http://www.cs.uiuc.edu/~hanj/) 啦！

#### From Social Networks to Heterogeneous Social and Information Networks: A Data Mining Perspective [slides](http://www.ccs.neu.edu/home/yzsun/Tutorials/ASONAM12_tuto_online.pdf)

Heterogeneous Information Network 是最近比较火领域，这种火热得益于 Jiawei Han 的得意门生，去年刚博士毕业就在 Northeastern University 做 Assistant Professor 的 [Yizhou Sun](http://www.ccs.neu.edu/home/yzsun/)。据 Jiawei Han 说，Yizhou Sun 是北大统计系、计算机系双学位，来到 UIUC 之后也在上统计的课程，而且分数全都是 A，所以总能把统计那边有趣的方法施加于 Machine Learning, Data Mining 之上。幸好之前做 SRTP 时接触过和 Heterogeneous Information Network 相关的内容，也读过 [RankClus](http://www.cs.uiuc.edu/~hanj/pdf/edbt09_ysun.pdf) 的那篇论文，Jiawei Han 也确实是一个好老师，语气、语调、停顿、重音，无不处理地相当精彩。Jiawei Han 能在繁忙的研究工作中腾出时间来练习讲课，为什么国内的一些教师讲课却简直没法听。

之后就是按照 Yizhou Sun 的发的论文的时间顺序开始讲。主要分为以下几个部分：

- RankClass
- Meta-Path
- Meta Similarity
- PathPredict (using meta path)
- Classification (using label)

有兴趣的可以去看 slides 和对应的论文，我也就不赘述了。

#### Large Graph Mining – Patterns, tools and cascade analysis [slides](http://www.slideshare.net/BigDataMining/large-graph-mining-patterns-tools-and-cascade-analysis-by-christos-faloutsos)

之前没有接触过 Large Graph 方面的内容，来自 CMU 的 speaker 的口音也比较重，所以只能模模糊糊地听出他的方法大概是什么，但细节什么的就不清楚了。

大概先讲了真实世界的 Graph 会服从的 Power Laws, Triangle Law，然后又说了是因为 self-similarity 才有如此多的 power-laws。那么我们如何运用 self-similarity 来生成一个符合 power law 的 Large Graph 呢？那就可以用分型（fractals）的方法，speaker 举了 Kronecker Graphs 的例子用以说明。

#### Challenging Problems for Scalable Mining of Heterogeneous Social and Information Networks [sildes](http://www.slideshare.net/BigDataMining/challenging-problems-for-scalable-mining-of-heterogeneous-social-and-information-networks-by-jiawei-han)

又见 Jiawei Han。

先是简单地重复一下上午讲得 Heterogeneous Information Network 的方法，之后就是对应 workshop 的名字（BigMine）讲一些 Heterogeneous Network 中 Big Data 的处理方法。

细览 Heterogeneous Network 的几篇文章，就可以知道他们用来 Evaluation 的数据集大多是 [DBLP](http://dblp.uni-trier.de/) 数据集的一个子集。简单[介绍](http://www-student.cse.buffalo.edu/~dlessa/cse462-SP10/r4.pdf)一下 DBLP 数据集，它是一个描绘计算机科学界作者、论文、会议和期刊的数据集，包含了 130 万的文章数据（包含所发表的期刊或会议）和 75 万作者的信息。

看起来挺大的对吧？但在 SIGKDD 谈 Big Data 这还不够，Google, Bing 的研究者可以用 PB 级别的数据进行研究，这 MB 级别的数据有些上不了台面。但 Jiawei Han 说，在 Heterogeneous Network 里做数据挖掘的 Cost 是非常大的，随意相关的几篇论文都没有在整个数据集中进行，而是在一个很小的子集里进行。那么，优化就是非常重要的了，这时就可以用到大数据方面的方法。

他用例子说明如何降低计算代价，大概有如下几个方法：

1. [Vector quantization](http://en.wikipedia.org/wiki/Vector_quantization)
2. 计算 Eigen Values 的时候，因为太长的 Meta Path 是不必要的，所以只要计算 Top-K 就可以。
3. 将重复用的数据预先计算好，存在数据库里。
4. [Co-Clustering](http://en.wikipedia.org/wiki/Co-clustering)

#### KDD Cup Workshop [url](http://www.kdd.org/kddcup2013/)

我也算参加过两届 KDD Cup 的人了（偷笑 ^_^），一次看完题之后就果断放弃（Tecent Weibo），另一次是是用 Sample 代码改了改，提交上去获得了极大的两位数排名，之后就没精力改了。一是因为没有时间，KDD Cup 总是在期中考试左右考试，期末考试之前结束，这就导致了不得不把它的优先级调低。再者，我对 Data Minning 也没有过深的了解，更不用说充满 tricks 的 Data Mining 竞赛了。

Missouri 是个小会场，只能坐 60 个人左右，我也只好站在后面，作为一个一直想认真地参加一次 KDD Cup 的选手，还是有点小激动。

听过几个选手的 slides 才明白，KDD Cup 是一场关于创建有效的 feature 和实现好多算法并进行 ensemble 的比赛。这并不是 research 中的不断完善一个模型直至 state-of-the-art。

最后一组居然是 LIBSVM 的作者 [Chih-Jen Lin](http://www.csie.ntu.edu.tw/~cjlin/) 老师讲，其实也并不意外，Chih-Jen Lin 老师带的学生每年都至少要拿一个第一的。Chih-Jen Lin 老师带领的参赛队有足足三十多人，他解释说他在[国立台湾大学](http://www.ntu.edu.tw/)为 KDD Cup 开了一门课！招的 30 多个学生，在开始的几周会进行 Data Mining 的教学，之后就分组挑战 KDD Cup。这太有趣了，国立台湾大学也很开明，有这么一个项目驱动的课程，自己学下来也会很有动力吧。负责的 TA 甚至为了平衡各组提交答案查看评价而写了一个决策系统。

晚上去 Pei Wei Asian Diner 吃 Traditional Chicken 居然遇到 Philip Yu 和 Jiawei Han 的学生在一起吃饭，看来我们吃的地方也不错嘛~

### Day Two

#### Scale-out Beyond Map-Reduce



#### Document and Topic Models



#### The Online Revolution: Education for Everyone

Andrew Ng!!!

#### Classification

### Day Three

#### Optimization in Learning and Data Analysis

Optimization

#### Graph clustering


#### ACM SIGKDD Business Meeting

遇到了在 Yahoo! Labs 工作的工作人员。


#### Panel: “A Data Scientist’s Guide to Making Money from Start-ups”

#### Scalable Methods for Big Data

#### Social and Information Networks

### Day Four

#### Predicting the Present with Search Engine Data


#### Web Mining


#### Best Papers Session


- 没有和同行交流
- 知识储备不够，Data Mining 太宏观
- 好好学英语，多听风味英语