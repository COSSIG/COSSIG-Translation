[#]: subject: "How updates work in CentOS"
[#]: via: "https://blog.centos.org/2022/09/how-updates-work-in-centos/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "fosinoprilsodium"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS 中的更新是如何工作的
======

这篇文章旨在解释 Fedora Linux, CentOS Stream 和 RHEL 之间的关系，尤其是软件包更新如何在它们之间流动。

## 从 Fedora 到 CentOS Stream

日常的更新发生在 Fedora Linux 上。Fedora Linux 每六个月发行一次 release ，每个 release 会维护大约13个月。重大更新应该（也几乎总是）先在 Fedora Linux 上部署，遵循 [更改过程][1] 。Fedora 的 packages 源在 [dist-git][2] 里维护，并在 [Fedora Koji][3] 里构建。

每个 CentOS 的重大更新（例如`9`, `10`等等）的开发周期开始的时候，这个发行版都会并入 Fedora 的分支。历史上来说，会在合并的时候采用目前 Fedora 的稳定发行版（比如 Fedora 34 之于 CentOS Stream 9）。当发行版被合并进分支里之后，新的 CentOS Stream 发行版开发周期才开始。

今时今日，[Fedora ELN][4] 通过持续地重构 Rawhide（Fedora 的开发中版本）帮助准备这个分支过程。这让我们能够了解到如果一个新的 CentOS Stream 版本今天就从 Fedora 分出去大概会是什么样的，也保证了规格文件的逻辑在任何时候都能保持与未来版本EL宏和 build flags 的兼容性。

## 从 CentOS Stream 到 RHEL

CentOS Stream 的包在 [GitLab][5] 里面维护，分支完成之后绝大多数发行版 [开发工作][6] 也在那里进行。包都在 [CentOS Stream Koji][7] 上构建，作为日常产生的 [distribution composes][8] 的一部分被分发出去。发行版的 compose 每周生成两到三次，通常会包括那段时间里发布的更新，但对这些进到 Stream 里面的更新不做任何保证。

RHEL 点发行版本质上是一个有着切实的开发工作在里面的 CentOS Stream compose 的快照，但不完全是这样。总的来说，一个包首先要经过QA环节，放到 Stream 里去，接下来才会被整合进下一个 RHEL 的小更新里。在这个意义上，Stream 实际上是针对下一个 RHEL 小更新持续发布的预览版。Aleksandra Fedorova 在她的 [OpenInfra Summit talk][9] 里也提到了这个过程的细节。

每当有一个 RHEL 发行版出来的时候，对应的源码都放在 [git.centos.org][10] 里，以便 RHEL 的重构项目（例如 Alma Linux 和 Rocky Linux）使用。

## 深入观察：紧急安全勘误表

正如上面所说的一样，总的设想是一个新的包首先进入 CentOS Stream里去，但有一个例外，就是承担着安全禁令的更新，还有紧急或重大安全勘误表的那些包。这些更新和勘误表是 Red Hat 开发的，直到安全禁令解除都会存在。它们会先发布到 RHEL 里，然后再进入 Stream。

以下有两个比较实际的情景。

### RHEL 和 CentOS Stream 都有一个 NVR（名称，版本，发行）相同的包

当一个给 RHEL 准备的勘误表发布的时候，包会在 RHEL 那里先升级。这时候你会发现，这同一个给 RHEL 准备的包也给 Stream 发布了。

去年十二月的 [polkit CVE][11] 就是一个很好的例子：RHEL 8 和 CentOS Stream 8 在 CVE 出现之前都在 [polkit-0.115-11.el8_4.1][12] 版本，[polkit-0.115-13.el8_5.1][13] 给两个系统都修复了这个 CVE。

### CentOS Stream 有一个比 RHEL 版本更大 NVR 的包

在这个情景里，CentOS Stream 的包比 RHEL 的版本要更新。当给 RHEL 上的软件包准备的勘误表更新了之后，包会在那里更新，但它的版本还是在 Stream 的版本后面。这时假设同一个更新也适用于 CentOS 版，那它也会准备好给 Stream 的更新，要么是移植修复过的新代码到老软件包里，要么就重建整个软件包。

另一个 CVE，这次是 libxml2，是一个绝好的例子。RHEL 上的版本在 CVE 出来之前是 [libxml2-2.9.7-9.el8][14] ，随后发布了一个修复了问题的 [libxml2-2.9.7-9.el8_4.2][15]。而在 Stream 上，这个更新则被包含在了 [libxml2-2.9.7-11.el8][16] 里。

## 深度观察：CentOS Stream 8

CentOS Stream 8 是第一个引入了 Stream 开发过程的 CentOS 版本，与以前的版本有着一些显著的不同。最值得注意的是：

- CentOS Stream 8 的软件包源代码都在 [git.centos.org][10] 上托管着（在 `c8s` 分支下），而不是 GitLab 上
- 由于技术限制，向 CentOS 提交 contribution 的过程是不一样的：不支持标准的PR工作流，而最好的贡献补丁的方法是把它们加到一个针对有关组件的 Bugzilla 工单上
- CentOS Stream 8 的包都在 [Koji mbox instance][17] 上构建

现在正进行着将 CentOS Stream 8 迁移到现有开发流程和工具上的工作，目标是最小化甚至最终消灭这些开发流程上的差异。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/09/how-updates-work-in-centos/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[fosinoprilsodium](https://github.com/fosinoprilsodium)
校对：[校对者ID](https://github.com/校对者ID)

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
