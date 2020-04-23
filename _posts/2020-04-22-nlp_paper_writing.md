---
title: '一点NLP论文写作资料的整理'
date: 2020-04-22
permalink: /posts/2020/04/nlp_paper_writing/
tags:
  - NLP
---
<!-- # 一点NLP论文写作资料的整理 -->

很神奇，这一类的资料真的不多，数来数去也就只有数年前清华大学刘洋老师的一个200+页数的PPT、知乎上刘知远老师的一篇文章。后来CCL的学生研讨会也有几个相关的内容，但是也没个录播。直接看PPT真的能吸收60%的内容就不错了。

---

## 1 写作顺序

![](https://imgkr.cn-bj.ufileos.com/bd53248e-62be-40b8-b953-e7bd42ac97e7.png)

这张图截自[2]，道理也很简单，往往学CS的人都会陷入我把实验做好，效果有了，Performance上去了就可以了的错觉。

正确方案还是应该先把Idea固化到纸面上，然后根据写的思路做实验，根据实验结果调整论文内容，如此循环。



![](https://imgkr.cn-bj.ufileos.com/1acb1d22-c835-4fe0-821a-d7140ede7d9e.png)

---

## 2 论文结构

![](https://imgkr.cn-bj.ufileos.com/0e8eeb59-b53a-4c8a-978d-47c5151fe444.png)

基本上会议论文的套路还是很固定，只有Related Work看个人喜好放在不同的位置。

[1]给了长度的建议，虽然不是什么必须遵循的准备，但是基本符合会议论文的普遍情况。

1. **Abstract: 1/4页**
2. **Introduction：1页**
3. **The Problem：1-2页**
4. **Proposed Method：2-5页**
5. **Experiments：1-3页**
6. **Related Work： 1/2页**
7. **Conclusion：1/2页**

### 2.1 Abstract

Abstract一般是放在最后写的，也是全文最凝练的部分，一般需要有四部分：

1. **要解决的问题**
2. **概述提出的方法**
3. **方法的优点**
4. **实验结果**

写Abstract要围绕着一个重要的目的——吸引审稿人。我之前审AAAI的论文是先看Abstract筛选自己想审的，不过今年IJCAI直接摘要reject一半的论文，可想而知这个的重要性了。就我个人感觉摘要也不需要过分套路，还是把方法和优点讲清楚比较重要，实验结果所有人都会说SOTA。



### 2.2 Introduction

Introduction几乎是能够决定论文生死的了。摘要比较简短，凭感觉可能还有概率出错，但是看完了Introduction，感觉不方法work，感觉没讲清楚，感觉很水，最后基本上读了全文也会是一个感觉。

应该有不少老师说写论文就是**“讲故事”**，起码写introduction是个讲故事的技术活。要吸引审稿人和读者，同时要让别人理解你的贡献有哪些。

大概Introduction可以分为两部分，讲问题和前人工作、讲自己的贡献。

1. **讲故事**
   1. **要解决的问题是什么**
   2. **为什么这个问题需要被解决/为什么这个问题有研究意义**
   3. **为什么前人无法解决**
2. **解释自己的贡献**
   1. **自己解决这个问题的方法是什么**
   2. **为什么这个方法有效**

此外[1]还列举了一些建议和禁忌：

- 禁忌(基本上都是废话的那种)

  - ```
    In recent years ...
    ```

  - ```
    The structure of this paper is ...
    ```

- 建议

  - 进行清楚的对比

    - ```
      ...departs from previous work in two ways:
      First, ...
      Second, ...
      ```

    - ```
      Different from ..., which only uses ..., our approach can use ...
      ```

  - 使用图来说明

  - 问问题

    - A question makes the reader want to know the answer!
    - It is also a promise of an answer.

  - 讲清楚自己的贡献

    - 分条列出

### 2.3 The Problem

这一部分其实不见得需要写，但是写上去一定会让读者更容易理解你的方法。一般更多会和Proposed Model放一起写。

1. **写清楚问题的详细定义**
2. **用公式来表达这个问题**
3. **不要在这部分解释提出的方法**
4. **用图例**

### 2.4 Proposed Method

1. 首先**直观地**介绍方法
2. 其次介绍方法的细节

有几个常见的问题：

1. 在直观解释方法前就讲细节，这样读的人会看不懂
2. 细节没有解释清楚
   1. 用公式+图例+算法流程 起码三选二，要把细节写清楚
3. 跟Introduction中提到的方法/贡献不相符合
   1. 这种情况基本上必凉

### 2.5 Experiment

实验模块的两个作用：

1. 支撑和验证自己声明的方法是可行的
2. 与前人的方法做比较

但是不要陷入2中而忽略了1。一般更加详细的实验和样例展示会更具有说服性（还有代码开源）。

1. **Ablation testes**

   ![](https://imgkr.cn-bj.ufileos.com/32765140-4058-4df1-918e-dea0cbbb9522.png)

2. Examples

   1. Better if you can show that examples are not flukes

下面是[1]给出的一个对比表

| Easy to understand                                           | Hard to understand                                   |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| Evaluate on standard data (e.g. WMT, Penn Tree bank, CNN/DM, ACE2005) | Use your own data. Especially not made public.       |
| Use a standard evaluation measure (e.g. BLEU, ROUGE)         | Invent your own evaluation measure.                  |
| Use recent research as a baseline and get better accuracy.   | No comparison, or no statistically significant gain. |

其实只要遵循第一列的内容就可以，虽然自己的数据集和评价指标不是不能用，但是如果真的有，都可以单独写一篇论文了，何必放在这种优化方法的论文里引起审稿人的疑惑。至于不做对比，基本上必挂，而且少引用了前人结果很容易被发现。

### 2.6 Related Work

很多人觉得这一部分和Introduction的前半部分是一样的，或者干脆合到一起写，又或者干脆前后的内容几乎一样。

[1]还是明确了这两者在目的上的不同，Related Work的目的在于：

1. 加深读者对于你这篇论文的理解
2. 讲清楚你和前人方法的不同

而Introduction的主要目的是：

1. 讲清楚问题
2. 引出你的方法

很明显Introduction对前人工作都是一句话的概述，而且，更多的是为解释问题而服务的。

**这里有几个大坑需要注意：**

1. 一定要做好参考文献的整理，缺了相关的文献，

   1. 如果你不知道有这篇论文，说明你工作没有做到位
   2. 如果你知道，说明你故意隐藏不写，可能是抄袭这篇论文

   总之，一定会挂

2. 别攻击别的研究者，太没品，而且容易引起审稿人反感。（万一就是人家审？）

### 2.7 Conclusion

一般就是三句话，重述问题，方法，结果。还有Future Work，用来补窟窿的一个部分，做的不完善的部分，就写在这。

---

## 3 写完了之后

**找人看论文！！！**

1. 最好是专业的人看，导师/同门/同行/同方向的同学
2. 不是一个方向的也可，毕竟如果不做你这个方向的人也看得懂，说明你写的很清楚
3. 把注意力放在“我哪里没写清楚”，而不是“你不懂我这部分写的”

其实最有效的，最有参考价值的是审稿人的审稿意见（但是一般中了可能就没那么在意，没中就很惨还要吐槽审稿人不懂）。就我个人上次EMNLP悲剧的经验，审稿人给了4页A4纸（打印）的审稿意见，真的是打回弟弟本体。但是真的都很有用。所以，投稿吧，被拒还能获得审稿意见，也不亏。



## Reference:

[1] How to Read/Write an International Conference Paper. Graham Neubig

[2] How to write a great research paper. Simon Peyton Jones