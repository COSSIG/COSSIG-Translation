[#]: subject: "CPE Quarterly Update Q3 2022"
[#]: via: "https://blog.centos.org/2022/10/cpe-quarterly-update-q3-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

社区平台工程团队 2022 第三季度 报告
======

这是<ruby>[社区平台工程团队][1]<rt>CPE</rt> </ruby>领导下的工作总结。每个季度，<ruby>社区平台工程团队<rt>CPE</rt> </ruby>都会和 Centos Fedora 代表一起，选择这季度的工作内容。然后，<ruby>社区平台工程团队<rt>CPE</rt> </ruby>会分成几个更小的子小组，在这些计划上完成每日所需的工作。

这次图文并茂的更新有很多细节。如果你想看新的变化，可以看看这个图文。如果你想了解更多细节，可继续阅读。
 ![][2]

## 关于

子小组小组的目标是处理的有关 Centos 和 Fedora 的基础设施的日常事务和Fedora 发布工程任务。它对运行在 Fedora 和 Centos 基础设施上面负责，也准备着新的 Fedora 发布（<ruby>镜像<rt>mirrors</rt></ruby>，<ruby>规模分支<rt>mass branching</rt></ruby>，新的<ruby>命名空间<rt>namespace></rt></ruby>）。这个子小组也调查可能的倡议。这是跟根据正在调查的倡议，由 Infra 和 Releng 子团队成员组成的 ARC（高级侦查队伍）所完成的，

**议题追踪**

- [Fedora 基础设施][3] 
- [CentOS 基础设施][4]
- [Fedora 发布工程][5]

**文档**

- [Fedora 基础设施][6]
- [CentOS 基础设施][7]
- [Fedora 发布工程][8]

## 子小组成员

- Mark O’Brien (Team Lead) (mobrien)
- Kevin Fenzi (nirik)
- Fabian Arrotin (arrfab)
- Pedro Moura (pshmoura)
- Tomáš Hrčka (humaton)
- Anton Medvedev (amedvede)
- Michal Konečný (zlopez)
- Akashdeep Dhar (t0xic0der)
- Vipul Siddharth (siddhartvipul)

## 完成的议题

- CentOS Infrastructure - 112
- Fedora Infrastructure - 150
- Fedora RelEng - 185

## 已完成的小提议

- [配置/部署新的 Duffy CI 实例][9]
- [新的模拟和 systemd-nspawn][10]
- [DNS 小倡议][11]

## 其他完成的任务

- Mass update/reboots
- Mass rebuild for F37

## ARC（高级侦查小组）完成调查

- [更新内核测试应用][12]

## 关于

这个提议是关于 Centos Stream/Emerging RHEL 新的分支成为现实。倡议的目标是维护 Centos Stream 和为此开发新的特性

**状态：:** 进展中。

**议题追踪** 

- [Bugzilla][13]

**文档** 

- [CentOS documentation][14]

**申请链接** 

- [https://centos.org/centos-stream/][15]

## 小组成员


- Brian Stinson (团队领导) (bstinson)
- Adam Samalik (asamalik)
- James Antill (jantill)
- Johnny Hughes
- David Fan (dfan)
- Stephen Gallagher (sgallagher)
- Troy Dawson (tdawson)
- Adam Saleh (asaleh)

## 关于

FMN（FedMsg 通知）是一个项目。当人们感兴趣的消息在消息汇总上触发时，它可以让人在自己的社区收到通知。它让消息汇总对于那些不直接开发，或者运行在我们基础设施上的应用排除故障的人们更有用。

现在的解决方案有很多技术负债，这个倡议会从头开始重写去解决所有问题。

**状态：** 进行中

**议题追踪**

- [Github project][16]

**文档**

- [Initiative proposal][17]
- [ARC investigation][18]
- [Documentation link][19]

**应用链接**

- [FMN Service][20]

## 子小组成员

- Aurelien Bompard (团队领导) (abompard)
- Ryan Lerch (rlerch)
- Nils Philippsen (nils)
- James Richardson (jrichardson)

## 关于

社区构建平台小组用户体验团队正在为 Fedora 上的图形设计，用户体验和用户界面工作。

**状态：** 进行中

**议题追踪**

- [Gitlab][21]

## 子小组成员

- Jess Chitas
- Emma Kidney
- Gbenga Oti

## 关于

Extra Packages 为 Enterprise Linux（或者 EPEL）是一个 Fedora 特别兴趣小组，它为 EPEL，包括但不仅限于 RHEL，CentOS，Scientific Linux（SL）和 Oracle Linux（OL）创造，维护和管理高质量的一系列附加安装包。
EPEL 软件包通常是基于它们的 Fedora 对应软件包，不会与base EPEL 发行版冲突或者替换。EPEL 和Fedora一样使用很多同样的基建，包括构建系统，Bugzilla 实例，更新管理器，镜像管理器等等。

**状态:** 进展中

**议题追踪**

- [Pagure][22]

**文档**

- [EPEL documentation][23]

## 子小组成员

- Carl George (团队领导) (carlwgeorge)
- Diego Herrera

## 关于

社区平台工程团队有一个专门的小组在 Fedora 文档上工作

**状态：** 进行中

**议题追踪**

- [Gitlab project][24]

**应用链接**

- [Fedora documentation][25]

## 子小组成员

- Petr Bokoc (pbokoc)

非常感谢你的阅读，如果你读到这里。如果你想要接触我们，请随时在 #redhat-cpe 频道在 [libera.chat][26] 或者 [matrix.org][27] 上联系。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/10/cpe-quarterly-update-q3-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[RakerZh](https://github.com/RakerZh)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://docs.fedoraproject.org/en-US/cpe/
[2]: https://blog.centos.org/wp-content/uploads/2022/10/Q3_2022_infographics-scaled.jpg
[3]: https://pagure.io/fedora-infrastructure/issues
[4]: https://pagure.io/centos-infra/issues
[5]: https://pagure.io/releng/issues/
[6]: https://docs.fedoraproject.org/en-US/infra/
[7]: https://docs.infra.centos.org/
[8]: https://docs.pagure.org/releng/
[9]: https://pagure.io/centos-infra/issue/821
[10]: https://pagure.io/releng/issue/6967
[11]: https://pagure.io/fedora-infrastructure/issue/9852
[12]: https://pagure.io/cpe/initiatives-proposal/issue/22
[13]: https://bugzilla.redhat.com/buglist.cgi?version=CentOS%20Stream
[14]: https://docs.centos.org/en-US/docs/
[15]: https://centos.org/centos-stream/
[16]: https://github.com/orgs/fedora-infra/projects/13
[17]: https://pagure.io/cpe/initiatives-proposal/issue/10
[18]: https://fedora-arc.readthedocs.io/en/latest/fmn/index.html
[19]: https://fmn.readthedocs.io/en/latest/
[20]: https://apps.fedoraproject.org/notifications/
[21]: https://gitlab.com/groups/fedora/design/team/-/issues
[22]: https://pagure.io/epel/issues
[23]: https://docs.fedoraproject.org/en-US/epel/
[24]: https://gitlab.com/fedora/docs/docs-website/pages/-/issues
[25]: https://docs.fedoraproject.org/
[26]: https://libera.chat/
[27]: https://matrix.org/
