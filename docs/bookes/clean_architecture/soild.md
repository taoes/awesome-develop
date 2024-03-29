---
title: S.O.I.L.D 原则
date: 2021-11-27
---

通常来说，要想构建一个好的软件系统，应该从写整洁的代码开始做起。毕竟，如果建筑所使用的砖头质量不佳，那么架构所能起到的作用也会很有限。反之亦然，如果建筑的架构设计不佳，那么其所用的砖头质量再好也没有用。这就是 SOLID 设计原则所要解决的问题。

SOLID 原则的主要作用就是告诉我们如何将数据和函数组织成为类，以及如将这些类链接起来成为程序。请注意，这里虽然用到了 “类”这个词，但是并不意味着我们将要讨论的这些设计原则仅仅适用于面向对象编程。这里的类仅仅代表一种数据和函数的分组，每个软件系统都会有自己的分类系统，不管它们各自是不是将其称为“类”，事实上都是 SOLID 原则的适用领域。

一般情况下，我们为软件构建中层结构的主要目标如下：

+ 使软件可容忍被改动。
+ 使软件更容易被理解。
+ 构建可在多个软件系统中复用的组件。

我们在这里之所以会使用“中层”这个词，是因为这些设计原则主要适用于那些进行模块级编程的程序员。SOLID 原则应该直接紧贴于具体的代码逻辑之上，这些原则是用来帮助我们定义软件架构中的组件和模块的。

当然了，正如用好砖也会盖歪楼一样，采用设计良好的中层组件并不能保证系统的整体架构运作良好。正因为如此，我们在讲完 SOLID 原则之后，还会再继续针对组件的设计原则进行更进一步的讨论，将其推进到高级软件架构部分。


## SRP：单一职责原则。
该设计原则是某于康威圧律（Conway's Law）的一个推论——一个软件系统的最佳结构高度依赖于开发这个系统的组织的内部结构。这样，每个软件模块都有且只有一个需要被改变的理由。

## OCP：开闭原则。
该设计原则是由 Bertrand Meyer 在 20 世纪 80 年代大力推广的，其核心要素是：如果软件系统想要更容易被改变，那么其设计就必须允许新增代码来修改系统行为，而非只能靠修改原来的代码。

## LSP：里氏替换原则。
该设计原则是 Barbara Liskov 在 1988 年提出的一个著名的子类型定义。简单来说，这项原则的意思是如果想用可替换的组件来构建软件系统，那么这些组件就必须遵守同一个约定，以便让这些组件可以相互替换。

## ISP：接口隔离原则。
这项设计原则主要告诫软件设计师应该在设计中避免不必要的依赖。

## DIP：依赖反转原则。
该设计原则指出高层策略性的代码不应该依赖实现底层细节的代码，恰恰相反，那些实现底层细节的代码应该依赖高层策略性的代码。


这些年来，这些设计原则在很多不同的出版物中都有过详细描述。在接下来的章节中，我们将会主要关注这些原则在软件架构上的意义，而不再重复其细节信息。如果你对这些原则并不是特别了解，那么我建议你先通过脚注中的文档熟悉一下它们，否则接下来的章节可能有点难以理解。 