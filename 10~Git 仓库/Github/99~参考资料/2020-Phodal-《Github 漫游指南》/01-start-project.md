# 创建开源项目

人们出于不同的目的来创建开源项目，可不论目的是什么，过程都是一样的。

1. 首先，我们需要为我们的项目取一个名字。
2. 然后，为我们的开源项目选择一个合适的 LICENSE
3. 然后再去创建项目

## 取一个好的名字

取名字，从来就不是一件容易的事。

因此，我就长话短说，一般就是取一个有意义的名字，当然没有意义也没有任何问题。

通常而言，如果自己计划有一系列的开源项目，那么我们可以保持一定的命名规则。

## 挑选好 LICENSE

> 在二十世纪而七十年代末和八十年代初，为了防止自己的软件被竞争对手所使用，大多数厂家停止分发其软件源代码，并开始使用版权和限制性软件许可证，来限制或者禁止软件源代码的复制或再分配。随后，Richard Matthew Stallman（Richard Matthew Stallman）发起了自由软件运动，他开创了 Copyleft 的概念：使用版权法的原则来保护使用、修改和分发自由软件的权利，并且是描述这些术语的自由软件许可证的主要作者。最为人所称道的是 GPL（被广泛使用的自由软件协议）。[^rms]

（PS：关于自由软件及 RMS 的更多信息、历史，可以阅读《若为自由故：自由软件之父 - 理查德 斯托曼传》）

[^rms]: https://zh.wikipedia.org/wiki/%E7%90%86%E6%9F%A5%E5%BE%B7%C2%B7%E6%96%AF%E6%89%98%E6%9B%BC

随后，便诞生了开源软件的概念，开源的要求比自由软件宽松一些[^gnu_gpl]。迄今发布的自由软件源代码都是开源软件，而并非所有的开源软件都是自由软件。这是因为不同的许可（协议）赋予用户不同的权利，如 GPL 协议强制要求开源修改过源码的代码，而宽松一点的 MIT 则不会有这种要求。

[^gnu_gpl]: https://www.gnu.org/philosophy/open-source-misses-the-point.zh-cn.html

如下是不同开源许可证的市场占有率及使用情况。

![License 使用情况](https://ngte-superbed.oss-cn-beijing.aliyuncs.com/book/phodal-github/permissive-vs-copylift-license-2.jpg)

又比如，在我们看到的一些外版书籍上，如果拥有代码。那么作者一般就会在前言或者类似的位置里，指明书中代码的版权所属。如：

> 也许你需要在自己的程序或文档中用到本书的代码，但除非大篇幅地使用，否则不必与我们联系取得授权。例如，用本书中的几段代码编写程序无需请求许可，blabla。

于是，选择一个合理的 LICENSE，就变成了一个有趣的话题。为此，笔者做了一个如何进行开源协议选型的流程图：

[![如何选择 License](https://ngte-superbed.oss-cn-beijing.aliyuncs.com/book/phodal-github/licenses.png)](https://github.com/phodal/licenses)

简单地来说，这些 License 之间是一些权利的区别，如当你把代码放置到公有领域，就意味着任何人可以修改，并且不需要标明出注；可如果你想要别人标明出处及作者，你就需要 MIT 协议；而你希望别人闭源的话，那么你就需要 MPL 协议等等。

那么，下面让我们简单地介绍一下不同的几个协议。

### 公有领域

> WTFPL（Do What The Fuck You Want To Public License，中文译名：你他妈的想干嘛就干嘛公共许可证）是一种不太常用的、极度放任的自由软件许可证。它的条款基本等同于贡献到公有领域。[^wtfpl]

[^wtfpl]: https://zh.wikipedia.org/wiki/WTFPL

这就意味着，对于拿到这些代码的其他人，他们想怎么修改就可以怎么修改。

### GPL

由于 GPL 的传染性，便意味着，他人引用我们的代码时，其所写的代码也需要使用 GPL 开源。即：GPL 是有 “传染性” 的 “病毒” ，因为 GPL 条款规定演绎作品也必须是 GPL 的。

而如果我们只针对的是，他人可以使用库，而不开源，则可以用 LGPL。但是修改库则不适用。

### MIT

因此，一般而言，我使用的是 MIT 协议。至少我保留了一个署名权，即你可以修改我的代码，但是在 LICENSE 里必须加上我的名字。

选用 MIT 特别有意思，特别是在最近几年里，发生过：

- [iView “抄袭” Element UI 事件](https://zhuanlan.zhihu.com/p/25739512)
- [AndroidTVLauncher “抄袭” 事件](https://github.com/JackyAndroid/AndroidTVLauncher/issues/22)

等等。这告诫了我们，如果你不想要有这种经历，那么就不要用 MIT 了。

### Creative Commons

是的，当我写 Markdown 的时候，考虑到未来会以纸质书的形式出现，便会使用 CC-BY-NC-ND 协议：

- CC -> Creative Commons
- BY -> 署名（英语：Attribution，by）
- NC -> 非商业性使用（英语：NonCommercial）
- ND -> 禁止演绎（英语：NoDerivs）。

即，任何人可以使用我写的电子书来自由复制、散布、展示及演出，但是不得用于商业用途（作者本人可以）。它可以随意地放在他的博客上，他的各个文章里。但是必须标明出自，并且不得改变、转变或更改本作品。

如果你不介意的话，你可以使用公有领域（Public Domain）。可是这样一来，万一有一天，别人直接拿你的作品出书，你就骂爹了。
