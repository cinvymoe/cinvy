+++
title = 'Bilibili C++ Primer 精读精讲 ch0-1 前言'
date = 2024-09-02T02:50:28+08:00
categories = []
tags = ["Bilibili", "C++", "教程"]
+++

Hey 朋友们，今天我们来聊一期系列介绍的视频。

谈一谈我接下来将要在 B 站投稿的 C++ Primer 第五版的系列视频。

名字叫：【大学生】《C++ Primer》精读精讲

## 面向人群

大学生。尤其是大一大二的学生。不限于计算机相关专业，不限文理科。计算机领域是相当包容的。因为是相当于入门课程，所以可能会比较啰唆，甚至是照本宣科，所以，高年级的同学可能没有那么多时间来观看，以及，以高年级同学的知识储备来讲，可能内容偏基础。

## 我希望大家准备的东西

1. 一台电脑。无论是运行 Windows11/10 还是 Linux 的电脑，都可以。
2. 畅通的网络，即可以流畅地访问 Google、GitHub、Stackoverflow 等等。限于某些原因，我无法在这里给大家讲解这部分的内容，但相信大家在网上应该可以找到对应的材料，实在不行，让身边的小伙伴手把手教一下请他/她吃顿饭也成。
## 为什么想要出这一个系列的视频

《C++ Primer》这本书用来打基础是相当好的，但是，这本书有一个缺点，也是我认为的惟一的缺点，那就是，有那么一丢丢阅读的门槛。我相信，很多人都听说过这本书，也读过这本书，但是，真正能把这本书读完的，十中无一。我以前也没有读完，最近重新捡起来读，花费了一个月，每天大概读四五个小时，最终是把这本书读完了。也正是因为仔细读了一遍下来，才知道这本书确实是真正地好书，也就促成了我录这个视频来分享交流的契机。

所以，我这一系列的视频，就是为了打破这个门槛。让初入校园或者刚接触编程或者刚接触 C++ 的同学能够破除阻碍，读下这本书，从而为自己的爱好打下一个良好的基础。
## 使用的教材以及获取方式

教材当时是视频标题的这本《C++ Primer》第五版啦。这本书是十年前出版的，但是，我读完之后，发现其中的内容鞭辟入里，放在今天一点也不过时，同时，结合国内外的评论，发现大家的看法也都是类似的，那就是，推荐。

豆瓣上的评分：<https://book.douban.com/subject/10505113/>。

获取方式如下，

英文版：

- <https://zhjwpku.com/assets/pdf/books/C++.Primer.5th.Edition_2013.pdf>

中文版：

- [C++ Primer 中文版·第五版](https://github.com/bumzy/book/blob/master/C%2B%2B%20%20Primer%E4%B8%AD%E6%96%87%E7%89%88%EF%BC%88%E7%AC%AC%E4%BA%94%E7%89%88%EF%BC%89.pdf)
- 或者，有条件的直接到微信读书开一个会员即可。

也可以到以下网站去检索一下：

- [zlibrary](https://zh.z-lib.gs/?ts=0718)
- [安娜的档案](https://zh.annas-archive.org/)

## 我讲解的方式

- 对于重要的文本，逐字逐句讲解，不落下。
- 对于书中出现的示例代码，一个不落，全部拓展成完整的可以运行的源文件进行测试。并且，全部在视频中手动编写、编译(包括借助 IDE)、运行。代码编排的顺序大概以英文版的页码为主。
- 有时候可能会结合其他材料，比如：网上的技术博客、cppreference 网站、GitHub 讨论区、stackoverflow、reddit 论坛的讨论等等。
- 对于习题，尽量全部讲解，但是更新的速度可能比主要的章节要慢一些。视频主要的节奏还是以非习题的主体部分为主。

我的想法还是，以代码为主，希望大家能够跟我一起边看边敲。有我的视频在，大家在编写、编译、调试、运行代码的过程中，基本上是不会有什么问题的，这样就可以把精力集中在学习编程语言本身这个事情上来。

这里还是要多说一点，就是，我讲解的内容只能保证尽量通俗，大家额外该看的资料肯定是不能少的。也希望大家多多给我提意见，我会不断改进，有好的建议我会做成补充视频的形式，供大家参考。

## 我演示编写代码的工具

### 编译套件

命令行或者 CMake。对于演示和学习而言，这两者足够简单并且够用。

CMake 现在也是编写 C++ 大型项目的主流工具，不过，我们在学习的过程中只会用到很简单很简单的一小部分。

具体到编译器，那么，在 Windows 中使用微软家的 MSVC 编译套件系列；在 Linux 中使用 gcc/g++ 套件。

### 操作系统

- Windows11
- Arch Linux KDE(wayland)

### 代码编辑器/IDE

主要是 Neovim + Neovide。然后借助 Powershell 脚本或者 shell 脚本来自动化 CMake 的编译过程，然后运行。

我的 Neovim 配置是公开的，我把它们放在了我另一个 GitHub 帐号中：

- Windows 中的 Neovim 配置：<https://github.com/fanlumaster/FanyLazyvim>
- Linux 中的 Neovim 配置：<https://github.com/fanlumaster/lazyvim-archlinux>

会介绍 VSCode、Visual Studio、CLion 的使用，大家随意使用。

我自己除了在前期的编程环境配置视频中会使用 IDE 以外，后期应该都会使用 neovim 来进行代码编写。对于代码调试，在 Windows 端我会使用 Visual Studio 或者 VSCode；在 Linux 我会使用 gdb 或者 VSCode。

### 终端工具

或者，大家也可以称其为命令行工具。

- Windows 下，建议使用 Windows Terminal + Powershell7
- Linux 下，建议使用 Kitty + fish

## 大家可能会有的一些疑问

### 有课时的顾虑吗？

当然没有，这里不是大学，不是正式的老师，不用恪守严格的规则。所以，我个人对课时不设限制，不会有大学老师所说的因为课时压缩等等原因而去跳过一些内容。所以，书中所有的内容都会涉及。

### 收费吗？可以转载吗？

我都放在 B 站了(条件允许也会同步到 Youtube)，那当然是不会收费。并且，以后也不会收费。整本书的讲解都不会收费。我争取把整本书讲完，希望能够得到大家的支持。

不管是视频还是博客，任何形式的转载、下载都是可以的，包括商业、非商业。当然，一定要注明出处哈。

### 视频涉及到的文档和代码材料在哪里？

所有的文稿都会放在我这个博客里面。并且在每个视频的简介里面附上 url 地址。

视频中所涉及的代码材料，我都会放在我当前的这个 [GitHub](https://github.com/sonnycalcr) 中。

### up 主会讲解其他的编程语言或者算法题吗？

大概率会。比如，我还有一些书想录制一些视频讲一下，比如，《流畅的 Python》第二版、《C 程序设计语言》K&R 第二版等。

对于数据结构和算法相关，我也想录制一些《算法竞赛入门经典》第二版、《数据结构与算法分析 C 语言描述》这类的视频。

总之，如果时间没有问题的话，我不打算给自己的题材设限。

### 会有一些小项目之类的视频吗？

会有的。目前的想法是先把一门完整的编程语言讲完，后续会录制项目相关视频。

当然，希望大家不要有太多的期待。因为我并不会整一些培训班的项目，可能顶多就是一些小游戏、或者像是在屏幕中显示键盘按下的按键、中文输入法开发这样的小众的项目。这也和我录制这些视频的初衷相吻合，我录制视频的目的并非是面向找工作，而且希望大家真的能够为了自己喜欢的编程奉献一点时间。

### 可以私信问 up 问题吗？

当然可以，不过，更建议以评论的方式留言，这样，我漏掉的时候还会有其他朋友来帮助回答。

欢迎多多评论。无论是在 B 站还是我这个博客下面。

## 声明

本人水平有限，欢迎随便喷。可以在视频的评论区吐槽，可以在博客的评论区留言，如果有理有据，那当然是更好啦，承诺：遇到错误，一定修正。

以及，有时间会做字幕，没空的时候就不加字幕了，望担待。

好，本期视频的前言就介绍到这里，下一期视频，我们将讲解 Windows 和 Linux 系统中 C++ 编程环境的搭建。

