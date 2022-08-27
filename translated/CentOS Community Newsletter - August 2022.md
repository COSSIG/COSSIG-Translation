[#]: subject: "August 2022 Newsletter"
[#]: via: "https://blog.centos.org/2022/08/centos-community-newsletter-august-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "lkxed"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS 社区通讯：2022 年 8 月
======

## 项目新闻

### DevConf 大会上的 Dojo 活动

CentOS 在波士顿的 DevConf.US 大会上举办了 [Dojo][1] 活动。这是我们第一次恢复举办面对面的活动，我们在 YouTube 直播了这次活动，让没到现场的人也能够远程参加。感谢所有在波士顿或网上加入我们的人。感谢你们在如何同时在线上线下举办活动所提供的反馈。活动录音很快就会发布。

## 特别兴趣小组（SIG）报告

每个月，我们都会轮流发布来自 [特殊兴趣小组][2]（SIG）的季度报告。本月包括来自 Cloud SIG 和 Storage SIG 的报告。

### [Cloud SIG][3]

#### 目标

打包和维护多个基于<ruby>自由和开放源码软件<rt>Free and Open Source Software</rt></ruby>（FOSS）的私有云基础设施应用，大家可以在 CentOS 上原生安装和运行它们。

[https://wiki.centos.org/SpecialInterestGroup/Cloud][3]

#### 成员更新

OKD（OpenShift 社区版）团队联系了 Cloud SIG，他们想知道是否可以加入我们。目前，他们的贡献者正在寻找提供 OKD 和 SCOS（CentOS Stream CoreOS）镜像的最佳方式。如果 OKD 和 SCOS 加入社区，有人建议让他们中的一名贡献者来填补空缺的 Cloud SIG 联合主席职位。

#### 最近一个季度的版本发布

##### RDO

“Yoga” 仍然是 [最新版本][4]。RDO 社区将在几周内打包下一个名为 “Zed” 的版本，该版本仅支持 CentOS Stream 9。谨此提醒，Yoga 是支持 CentOS Stream 8 和 9 的过渡性 Openstack 版本，以便能够将操作系统从一个迁移到另一个操作系统。

#### 健康度和活跃度

Cloud SIG 仍然相当健康。不过，在大多数情况下，它仍然是一个只包含 OpenStack 的单一文化。

### [Storage SIG][5]

自上次报告以来，软件包进行了更新：

- Glusterfs 10 更新至 glusterfs-10.2，软件包可用于 Stream 9 和 Stream 8。
- Glusterfs 9，没有更新。
- Ceph Quincy（17）更新至 ceph-17.2.2，软件包适用于 Stream 9、Stream 8 和 RHEL8。
- Ceph Pacific（16）更新至 ceph-16.2.10，软件包适用于 Stream 9、Stream 8 和 RHEL8。
- Ceph Octopus（15），没有更新。
- NFS-ganesha 4 和 libntirpc 4，没有更新。
- Apache Arrow 更新至 libarrow-8.0.1，软件包可用于 Stream 9、Stream 8。
- Apache ORC 更新至 liborc-1.7.5，软件包可用于 Stream 9、Stream 8。

注：Ceph Quincy（17）及更早版本，并且不在 CoreOS、CBR/PowerTools 或 AppStream 中的依赖项，一直由 Storage SIG 提供的。但是，从 Ceph Reef（18）开始，这些依赖项将由 EPEL 提供。这包括 Apache Arrow（libarrow）、Apache ORC（liborc）和其他相当长的软件包列表。这将简化构建依赖项，只需将它们构建在一个地方即可。许多开发者和最终用户也倾向于更喜欢 EPEL，并在默认情况下启用 EPEL，这将减少或彻底消除 EPEL 中软件包与 Storage SIG 中软件包之间的冲突。不过，Ceph 本身并不会在 EPEL中；它将只在 Storage SIG 中保留。

以下是 Samba 的更新：

- Samba 4.16，在 Stream 9 和 Stream 8 上更新到最新版本 4.16.3。
- Samba 4.15，在 Stream 9 和 Stream 8 上更新到最新版本 4.15.8。RHEL8 版本也可用。
- Samba 4.14，在 CVE 中仅修复模式。

报告的问题：

鉴于 [用户报告][6] 在 Samba 守护进程启动期间的崩溃，我们正在努力确保系统安装的依赖库版本，如 libtalloc、litdb、libtevent 和 libldb 等不会干扰构建中的相应副本。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/08/centos-community-newsletter-august-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[lkxed](https://github.com/lkxed)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org/
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[2]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[3]: https://wiki.centos.org/SpecialInterestGroup/Cloud
[4]: https://blogs.rdoproject.org/2022/04/rdo-yoga-released/
[5]: https://wiki.centos.org/SpecialInterestGroup/Storage
[6]: https://lists.centos.org/pipermail/centos-devel/2022-June/120415.html
