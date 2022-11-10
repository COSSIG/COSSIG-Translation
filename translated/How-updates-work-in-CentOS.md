[#]: subject: "How updates work in CentOS"
[#]: via: "https://blog.centos.org/2022/09/how-updates-work-in-centos/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "fosinoprilsodium"
[#]: reviewer: "Northurland"
[#]: publisher: " "
[#]: url: " "

CentOS 中的更新是如何工作的
======

这篇文章旨在解释 Fedora Linux, CentOS Stream 和 RHEL 之间的关系，尤其是软件包更新在它们之间流动的方式。

## 从 Fedora 到 CentOS Stream

Fedora Linux 的更新极为频繁。Fedora 每六个月<ruby>发布<rt>release</rt></ruby>一个版本，每个 <ruby>版本<rt>release</rt></ruby>会维护大约13个月。原则上，重大更新应该先在 Fedora 中部署，遵循 Fedora 社区的 [更改过程][1] ；事实上也几乎总是这样。Fedora 的<ruby>软件包源<rt>packages sources</rt></ruby>在 [dist-git][2] 里维护，并在 [Fedora Koji][3] 里构建。

CentOS 的每个<ruby>大版本<rt>major release</rt></ruby>（例如 `9`, `10` 等等）的开发周期开始的时候，Fedora 都会被引入该版本中。历史上来说，会在合并的时候采用目前 Fedora 的稳定版本（比如 Fedora 34 之于 CentOS Stream 9）。当该版本的 Fedora 被合并进分支里之后，新的 CentOS Stream 发行版开发周期才开始。

如今，通过持续地重构 Rawhide（Fedora 的开发中版本），[Fedora ELN][4] 在这个分支过程中提供了帮助。这让我们能够了解，如果一个新的 CentOS Stream 版本今天就从 Fedora 分出去大概会是什么样的；这也保证了<ruby>规格文件的逻辑<rt>spec file logic</rt></ruby>始终与未来版本 EL 宏和 build flags 兼容。

## 从 CentOS Stream 到 RHEL

CentOS Stream 的包在 [GitLab][5] 中维护；从 Fedora 中分支之后，对应版本的绝大多数 [开发工作][6] 也在那里进行。包都在 [CentOS Stream Koji][7] 上构建，作为日常产生的 [distribution composes][8] 的一部分被分发出去。发行版的 compose 每周生成两到三次，它们通常会包括那段时间里发布的更新，但是不保证具体哪些更新会进入 Stream。

简单来说，RHEL 的每个<ruby>小版本<rt>point release</rt></ruby>都是 CentOS Stream compose 的快照，其发布时间晚于对应的 Stream 版本；但它们的本质并非完全如此。总的来说，一个包首先要经过 QA 环节，然后进入 Stream，接下来才会被整合进下一个 RHEL 的小更新里。在这个意义上，Stream 实际上是针对下一个 RHEL 小更新持续发布的预览版。Aleksandra Fedorova 在她的 [OpenInfra Summit talk][9] 里也提到了这个过程的细节。

当每个 RHEL 版本发布时，对应的源码都放在 [git.centos.org][10] 里，以便 RHEL 的<ruby>下游发行版<rt>rebuild projects</rt></ruby>（例如 Alma Linux 和 Rocky Linux）使用。

## 深入观察：紧急安全勘误表

正如上面所说的一样，新的包几乎总会先进入 CentOS Stream，之后再进入 RHEL。但有一个例外，就是承担着安全<ruby>禁令<rt>embargo</rt></ruby>的更新，和带有紧急 / 重大安全勘误表的那些包。这些更新和勘误表是 Red Hat 开发的，直到安全禁令解除都会存在。它们会先发布到 RHEL 里，然后再进入 Stream。

以下有两个比较实际的情景。

### RHEL 和 CentOS Stream 的包版本相同

当一个给 RHEL 准备的勘误表发布的时候，对应的包会进入 RHEL。这时候你会发现，相同的包也进入了 Stream。

去年十二月的 [polkit CVE][11] 就是一个很好的例子：RHEL 8 和 CentOS Stream 8 在 CVE 出现之前都在 [polkit-0.115-11.el8_4.1][12] 版本，[polkit-0.115-13.el8_5.1][13] 给两个系统都修复了这个 CVE。

### CentOS Stream 的包比 RHEL 中对应的包版本更高

在这个情景里，CentOS Stream 的包比 RHEL 的版本要高。当给 RHEL 的勘误表发布之后，包会在那里更新，但它的版本还是比 Stream 的版本更低。这时，假设同一个更新也适用于 CentOS 版，那么 Stream 也会得到更新；这种更新要么是移植修复过的新代码到最新的 Stream 软件包里，要么就重建整个软件包。

另一个 CVE，这次是 libxml2，是一个绝好的例子。RHEL 的版本在 CVE 出现之前是 [libxml2-2.9.7-9.el8][14] ，随后发布了一个修复了问题的 [libxml2-2.9.7-9.el8_4.2][15]。而在 Stream 上，这个更新则被包含在了 [libxml2-2.9.7-11.el8][16] 里。

## 深入观察：CentOS Stream 8

CentOS Stream 8 是第一个引入了 Stream 开发过程的 CentOS 版本，与以前的版本有着一些显著的不同。最值得注意的是：

- CentOS Stream 8 的软件包源代码都在 [git.centos.org][10] 上托管着（在 `c8s` 分支下），而不是 GitLab 上
- 由于技术限制，向 CentOS 贡献的过程与以往不同：不支持标准的 PR 工作流，贡献补丁的最好方法是把它们加到一个针对有关组件的 Bugzilla 工单上
- CentOS Stream 8 的包都在 [Koji mbox instance][17] 上构建

现在，我们正在将 CentOS Stream 8 迁移到现有的开发流程和工具上，希望能够尽量缩小、乃至于消灭这些开发流程上的差异。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/09/how-updates-work-in-centos/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[fosinoprilsodium](https://github.com/fosinoprilsodium)
校对：[Northurland](https://github.com/Northurland)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://docs.fedoraproject.org/en-US/program_management/changes_policy/
[2]: https://src.fedoraproject.org
[3]: https://koji.fedoraproject.org
[4]: https://docs.fedoraproject.org/en-US/eln/
[5]: https://gitlab.com/redhat/centos-stream/rpms
[6]: https://gitlab.com/groups/redhat/centos-stream/rpms/-/merge_requests
[7]: https://kojihub.stream.centos.org
[8]: https://composes.stream.centos.org/
[9]: https://www.youtube.com/watch?v=yf1wO5Iu8uY
[10]: http://git.centos.org
[11]: https://koji.mbox.centos.org/koji/buildinfo?buildID=17891
[12]: https://koji.mbox.centos.org/koji/buildinfo?buildID=20924
[13]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3541
[14]: https://koji.mbox.centos.org/koji/buildinfo?buildID=14132
[15]: https://koji.mbox.centos.org/koji/buildinfo?buildID=18244
[16]: https://koji.mbox.centos.org/koji/buildinfo?buildID=17568
[17]: https://koji.mbox.centos.org
