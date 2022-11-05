[#]: subject: "How updates work in CentOS"
[#]: via: "https://blog.centos.org/2022/09/how-updates-work-in-centos/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "fosinoprilsodium"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS中的更新是如何工作的
======

这篇文章旨在解释Fedora Linux, CentOS Stream和RHEL之间的关系，尤其是软件包更新如何在它们之间流动。

## 从Fedora到CentOS Stream

日常的更新发生在Fedora Linux上。Fedora Linux每六个月发行一次release，每个release会维护大约13个月。重大更新应该（也几乎总是）先在Fedora Linux上部署，遵循[更改过程][1]。Fedora的packages源在[dist-git][2]里维护，在[Fedora Koji][3]里构建。

每个CentOS的重大更新（就是`9`, `10`等等）的开发周期开始的时候，发行版都会并入Fedora的分支。历史上来说，会在合并的时候采用目前Fedora的稳定发行版（比如Fedora 34之于CentOS Stream 9）。当发行版被分支合并之后，新的CentOS Stream发行版开发周期才开始。

今时今日，[Fedora ELN][4]通过持续地重构Rawhide（Fedora的开发中版本）帮助准备这个分支过程。这让我们能够知道如果一个新的CentOS Stream版本今天就从Fedora分出去大概会是什么样的，也保证了规格文件的逻辑在任何时候都能保持与未来版本EL宏和build flags的兼容性。

## 从CentOS Stream到RHEL

CentOS Stream的包在[GitLab][5]里面维护，那里也是分支完成之后绝大多数发行版[开发工作][6]发生的地方。包都在[CentOS Stream Koji][7]上构建，作为日常产生的[distribution composes][8]的一部分被分发出去。发行版的compose每周生成两到三次，通常会包括那段时间里发布的更新，但对这些进到Stream里面的更新不做任何保证。

RHEL点发行版本质上是一个有着切实的开发工作在里面的CentOS Stream compose的快照，但不完全是这样。总的来说，一个包首先要经过QA环节，放到Stream里去，接下来才会被整合进下一个RHEL的小更新里。在这个意义上，Stream实际上是下一个RHEL小更新的持续发布的预览版。Aleksandra Fedorova在她的[OpenInfra Summit talk][9]里也说过这个过程的细节。

每当有一个RHEL发行版出来的时候，对应的源码都放在[git.centos.org][10]里，以便RHEL的重构项目（例如Alma Linux和Rocky Linux）使用。

## 深入观察：紧急安全勘误表

正如上面所说的一样，总的设想是一个新的包首先进入CentOS Stream，但有一个例外，就是承担着安全禁令的更新和紧急或重大安全勘误表的那些包。这些是Red Hat开发的，直到安全禁令解除都会存在。它们会先发布到RHEL里，然后再进入Stream。

以下有两个比较实用的情景。

### RHEL和CentOS Stream都有一个NVR（名称，版本，发行）相同的包

当一个给RHEL准备的勘误表发布的时候，包会在那里先升级。这时候你会发现，这同一个给RHEL准备的包也给Stream发布了。

去年十二月的[polkit CVE][11]就是一个很好的例子：RHEL 8和CentOS Stream 8在CVE出现之前都在[polkit-0.115-11.el8_4.1][12]版本，[polkit-0.115-13.el8_5.1][13]给两个系统都修复了CVE。

### CentOS Stream有一个比RHEL版本更大NVR的包

在这个情景里，CentOS Stream的包比RHEL的版本要更新。当给RHEL上的软件包准备的勘误表更新了之后，包会在那里更新，但它的版本还是在Stream的版本后面。这时假设同一个更新也适用于CentOS版，那它也会准备好给Stream的更新，要么是移植修复过的新代码到老软件包里，要么就重建整个软件包。

另一个CVE，这次是libxml2，是一个绝好的例子。RHEL上的版本在CVE出来之前是[libxml2-2.9.7-9.el8][14]，随后发布了一个修复了问题的[libxml2-2.9.7-9.el8_4.2][15]。而在Stream上，这个更新则被包含在了[libxml2-2.9.7-11.el8][16]里。

## 深度观察：CentOS Stream 8

CentOS Stream 8是第一个引入了Stream开发过程的CentOS版本，与以前的版本有着一些显著的不同。最值得注意的是：

- CentOS Stream 8的软件包源代码都在[git.centos.org][10]上托管着（在`c8s`分支下），而不是GitLab上
- 由于技术限制，向CentOS提交contribution的过程是不一样的：标准的PR工作流不被支持，最好的贡献补丁的方法是给它们加在一个针对有关组件的Bugzilla工单上
- CentOS Stream 8的包都在[Koji mbox instance][17]上构建

现在正有将CentOS Stream 8迁移到现有开发流程和工具上的工作，目标是最终最小化甚至消灭这些开发流程上的差异。

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
