**目录：**

   * [TensorFlow 背后的 community](#tensorflow-背后的-community)
      * [1. Tensorflow简介](#1-tensorflow简介)
         * [1.1. 关于TensorFlow](#11-关于tensorflow)
         * [1.2. TensorFlow的地址](#12-tensorflow的地址)
         * [1.3. TensorFlow的特性](#13-tensorflow的特性)
         * [1.4. TensorFlow与其他开源深度学习框架比较](#14-tensorflow与其他开源深度学习框架比较)
      * [2. TensorFlow社区](#2-tensorflow社区)
      * [3. 成为TensorFlow社区Contributor](#3-成为tensorflow社区contributor)
         * [3.1. TensorFlow有那么多待完善的功能吗？怎么发现它们？](#31-tensorflow有那么多待完善的功能吗怎么发现它们)
         * [3.2. TensorFlow社区值得关注的东西](#32-tensorflow社区值得关注的东西)
         * [3.3. TensorFlow生态中的其他子项目](#33-tensorflow生态中的其他子项目)
         * [3.4. TensorFlow 2.0的标准制定项目——Community](#34-tensorflow-20的标准制定项目community)
      * [4. 总结](#4-总结)
         * [4.1. TensorFlow开源的意义](#41-tensorflow开源的意义)
         * [4.2. 参与开源对我们的意义](#42-参与开源对我们的意义)
      * [5. 参考文献](#5-参考文献)


# TensorFlow 背后的 community

## 1. Tensorflow简介

### 1.1. 关于TensorFlow

TensorFlow是谷歌2015年开源的通用高性能计算库。最初主要是为构建神经网络(NNs)提供高性能的API。然而，随着时间的推移和机器学习(ML)社区的兴起，TensorFlow已经发展为一个完整的机器学习生态系统。

TensorFlow是一个采用数据流图（data flow graphs），用于数值计算的开源软件库。它灵活的架构让我们可以在多种平台上展开计算，例如台式计算机中的一个或多个CPU（或GPU），服务器，移动设备等等。

TensorFlow 最初由Google大脑小组（隶属于Google机器智能研究机构）的研究员和工程师们开发出来，用于机器学习和深度神经网络方面的研究，但这个系统的通用性使其也可广泛用于其他计算领域。

截止2019年11月30日，TensorFlow社区已经收获 **138 k** star, **78.8 k** Fork, 拥有 **2293** 位contributors, 接受了 **73313** 个commit。

### 1.2. TensorFlow的地址

1. Github源码地址：
    https://github.com/tensorflow/tensorflow

2. 非官方接口地址如下：

    Julia: https://github.com/malmaud/TensorFlow.jl <br>
    Node.js https://github.com/node-tensorflow/node-tensorflow <br>
    R: https://github.com/rstudio/tensorflow

### 1.3. TensorFlow的特性

- **高度的灵活性**
    用户也可以自己在Tensorflow基础上写自己的“上层库”；如果发现找不到想要的底层数据操作，也可以自己写一点c++代码来丰富底层的操作。

- **真正的可移植性**
    Tensorflow 在CPU和GPU上运行，比如说可以运行在台式机、服务器、手机移动设备等等。

- **将科研和产品联系在一起**
    使用Tensorflow可以让应用型研究者将想法迅速运用到产品中，也可以让学术性研究者更直接地彼此分享代码，从而提高科研产出率。

- **自动求微分**
    作为Tensorflow用户，我们只需要定义预测模型的结构，将这个结构和目标函数（objective function）结合在一起，并添加数据，Tensorflow将自动计算相关的微分导数。

- **多语言支持(Python / C++)**
    有一个合理的c++使用界面，也有一个易用的python使用界面来构建和执行graphs。

- **性能最优化**   
    Tensorflow 给予了线程、队列、异步操作等以最佳的支持,可以自由地将Tensorflow图中的计算元素分配到不同设备上，Tensorflow可以帮我们管理好这些不同副本。



### 1.4. TensorFlow与其他开源深度学习框架比较

**优点：** 

- 由谷歌开发、维护，因此可以保障支持、开发的持续性。
- 巨大、活跃的社区
- 网络训练的低级、高级接口
- 「TensorBoard」是一款强大的可视化套件，旨在跟踪网络拓扑和性能，使调试更加简单。
- 用 Python 编写（尽管某些对性能有重要影响的部分是用 C++实现的），这是一种颇具可读性的开发语言
- 支持多 GPU。因此可以在不同的计算机上自由运行代码，而不必停止或重新启动程序
- 比基于 Theano 的选项更快的模型编译
- 编译时间比 Theano 短
- TensorFlow 不仅支持深度学习，还有支持强化学习和其他算法的工具

**缺点：**

- 计算图是纯 Python 的，因此速度较慢
- 图构造是静态的，意味着图必须先被「编译」再运行


## 2. TensorFlow社区

TensorFlow在2015年11月刚开源的第一个月就积累了10000+的star。其次，TensorFlow确实在很多方面拥有优异的表现，比如设计神经网络结构的代码的简洁度，分布式深度学习算法的执行效率，还有部署的便利性，都是其得以胜出的亮点。如果一直关注着TensorFlow的开发进度，就会发现基本上每星期TensorFlow都会有1万行以上的代码更新，多则数万行。产品本身优异的质量、快速的迭代更新、活跃的社区和积极的反馈，形成了良性循环，可以想见TensorFlow未来将继续在各种深度学习框架中脱颖而出。


TensorFlow 在中国的下载次数已经超过百万次。在 Google 开发者大会和 TensorFlow Dev Summit 北京分论坛等会议上，广大开发者反应希望有一个 TensorFlow 开发者自助互助、技术交流的平台，众人拾柴火焰高，以论坛的形式建立一个聚集所有中国 TensorFlow 开发者的线上社区这个想法便孕育而生，并最终实现。

***TensorFlow 中文网站***

不久前，TensorFlow 中文网站 ( tensorflow.google.cn )发布，并建立微信公众号，现在，TensorFlow中文社区论坛上线，为中国的开发者们提供一个进行 TensorFlow 以及机器学习技术分享和互动交流的平台。

TensorFlow是一个开放的社区，无论是资深开发者还是学生、研究员或是爱好者，都可以在论坛上就共同感兴趣的话题进行交流分享、问题反馈、互相帮助。让每个人都能学习、使用以及推动机器学习技术，并最终使人人受益。

需要强调的是，和开源的 TensorFlow 技术一样，TensorFlow 中文社区论坛是属于所有关心它和使用它的开发者们的。我们也要积极一同参与到社区建设当中，共同推进 TensorFlow 技术在中国的发展。



## 3. 成为TensorFlow社区Contributor

### 3.1. TensorFlow有那么多待完善的功能吗？怎么发现它们？

其实非常多。TensorFlow一大特点是通用性，希望能够在各种场景下均能够变得成熟。但是这个目的工程量浩大，不免存在Bug，设计不完善，性能不理想，功能不全面等情况。其实在使用TensorFlow建模时就会遇到他们，而且概率不算小。当然我们可以遇到问题选择绕开它们，但这可能也意味着你错失了一个提PR的机会。提PR的前提是我们必须对源码有所了解，而这又是一个工程性的东西，每天看一点TensorFlow源码能够提升我们的一些工程素养。

### 3.2. TensorFlow社区值得关注的东西
TensorFlow是Google重要的算法军火库，Google围绕着TensorFlow本身还做了其他子项目，他们也非常重要。另外，也可以加入讨论组。

### 3.3. TensorFlow生态中的其他子项目
TensorFlow生态中子项目相当丰富，有前端TensorBoard，有易用性框架Estimator等等。这些子项目也同样需要社区贡献力量。

### 3.4. TensorFlow 2.0的标准制定项目——Community

Community子项目其实就是TensorFlow的RFC文档，它是TensorFlow 2.0的标准，里面含有一些模块和接口的设计。我们要关注RFC文档，是因为TensorFlow的发展比较快，经常出现某些模块被弃用，某些新模块将要大力发展的情况。这些信息对于开发者非常重要，如果我们想共享一段代码，但它与社区的发展标准背道而驰，那么将是无用功，所以RFC文档对于避免无用功是非常有用的。但一个标准的提出也需要经过社区的审核和讨论，所以如果我们有自己的想法，可以在Community中提出自己的comments，引入更多的人参与讨论。


具体如何向TensorFlow社区贡献代码的步骤可以看如下链接：

> https://www.cnblogs.com/deep-learning-stacks/p/10424914.html

## 4. 总结
### 4.1. TensorFlow开源的意义

- 谷歌也在开源TensorFlow不断改进自身算法的方式，允许人工智能知识有限的开发人员也能够开发出有用的应用程序。

- TensorFlow并不完美，但其可以帮助用户进行信息筛选，节省大量时间。

- 今天，我们生活在互联经济时代。降低成本以及资产优化不再是绝对的竞争优势，而打造价值生态系统才是真正意义上的竞争优势。相应的能力优势不再是金字塔的顶端，而是在网络中心。
### 4.2. 参与开源对我们的意义

- 更好的技能。优秀的开源项目一般来说生命力很长，如果熟悉精通开源项目的话，一般会很容易在市场中找到一个有竞争力的位置。

- 更好的认可度、知名度。在花时间参与开源项目的技术讨论，反馈开源软件的缺陷，以及将改进贡献回开源项目中，可以得到更多人的认可，并且也会让自己在市场中的竞争力得到提高。

- 在圈子内建立更多的人脉。多参与开源社区可以让工程师与来自不同的公司、文化背景、语言与国际的人进行沟通。在过程中可以更多的积累人脉与了解到别人的思维方式。不容易固化在自己的小圈子里面。


## 5. 参考文献
1. https://www.sohu.com/a/232727519_129720

2. https://www.cnblogs.com/deep-learning-stacks/p/10424914.html

3. http://www.dataguru.cn/thread-745236-1-1.html

4. http://www.tensorfly.cn

5. https://www.jianshu.com/p/cfc31f756a92

6. https://www.oschina.net/news/75397/google-tensorflow-way 

7. https://blog.csdn.net/DP29syM41zyGndVF/article/details/89089775 


