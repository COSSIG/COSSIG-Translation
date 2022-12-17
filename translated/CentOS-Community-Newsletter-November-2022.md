[#]: subject: "November 2022 Newsletter"
[#]: via: "https://blog.centos.org/2022/11/centos-community-newsletter-november-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "Northurland"
[#]: translator: "fosinoprilsodium"
[#]: reviewer: ""
[#]: publisher: ""
[#]: url: ""

November 2022 Newsletter
======

## 项目新闻

![CentOS Connect][13]

[CentOS Connect][1] 已经官宣成为了 FOSDEM Fringe 活动的一部分。这场不需入场费的活动将在 2023 年 2 月 3 日，也就是 FOSDEM 大会正式举办的前一天进行。如果你有意参加 FOSDEM，在 CentOS Connect 上加入我们，了解有关 CentOS 的更多事情并和开发它的人相互联系。

### <ruby>替代镜像小组<rt>Alternate Images SIG</rt></ruby>

[替代镜像小组][2] 正式地成为了提供额外的操作系统镜像的兴趣小组，提供的内容包括操作系统的可移动介质版以及其他替代形式的安装。他们的[会议][3]每周四 UTC 19时在 #centos-meeting IRC 频道里举行。

### OKD Streams

[OKD][4]项目已经[上马了，发行的OKD Streams][5]是在新引入的 CentOS Stream CoreOS上构建的，稳定的 OKD build。 OKD是红帽OpenShift背后Kubernetes项目的社区发行版。

## SIG 报告

每月，我们都会发布一次从我们的[特别兴趣小组][6]里轮换选出的季度报告。这个月的报告包括了来自 <ruby>Cloud<rt>云</rt></ruby>，<ruby>Promo<rt>推广</rt></ruby> 和 <ruby>Storage<rt>存储</rt></ruby> 这三个小组的。

### [Cloud][7]

### 目标

打包和维护多个基于<ruby>自由和开放源码软件<rt>Free and Open Source Software</rt></ruby>（FOSS）的私有云基础设施应用，大家可以在 CentOS 上原生安装和运行它们。

https://wiki.centos.org/SpecialInterestGroup/Cloud

### 成员更新

继续协助 OKD 和 SCOS 融入社区。OKD 的维护者 Christian Glombek 会填补空缺的 Cloud SIG 联合主席职位。

在下一个季度推出release（如果这下一个季度里没有 CentOS release 的话，就在下一个 CentOS release 推出的时候）

CloudSIG 发布了基于上游 OpenStack Zed 的新版本 RDO Zed。[8]

OKD 工作小组与 CloudSIG 合作，发布了第一个 OKD/SCOS（基于CentOS Stream CoreOS的OKD）的<ruby>MVP<rt>最小化可行产品</rt></ruby>。

### 健康度和活跃度

Cloud SIG 的健康保持地相当不错，并且也在积极寻求其他项目的加入以扩展它的受众。

### [Promo](https://wiki.centos.org/SpecialInterestGroup/Promo)

八月，我们举办了 [DevConf.US 上的 CentOS 道场活动][10]。这是我们疫情后首次回归线下活动，但也可以线上参与。总得来说这次活动进行得不错，并且还有巨大的发展潜力。[完整的活动报告][11]在这里。

我们一直在为[CentOS Connect at FOSDEM][1]这个活动工作着，CentOS Connect 是 CentOS 道场活动的新名字。过去，我们在 FOSDEM 上举办的 CentOS 道场活动一直是规模最大的，并且我们这次计划一个一天承载一百个人的活动。这仍然比疫情前的要更短小精悍一些。

最后值得一提的是，[一个来自中国的兴趣组][12]正式加入了 Promo 兴趣组以便进行区域性和本地化的推广和宣传。我们对他们正在进行的工作感到很兴奋，并且我们希望这为将来更多区域性的宣传活动铺平道路。

### [Storage](https://wiki.centos.org/SpecialInterestGroup/Storage)

自上次报告以来，下列软件包进行了更新：

 - Glusterfs 10 更新至 glusterfs-10.3，软件包可用于 Stream 9 和 Stream 8。
 - Glusterfs 9，更新至 glusterfs-9.6，软件包可用于 Stream 9，Stream 8 和 CentOS 7。
 - Ceph Quincy (17) 更新至 ceph-17.2.5，软件包可用于 Stream 9 和 Stream 8。
 - Ceph Pacific (16) 没有更新，但是 ceph-16.2.11 很快就要来了。
 - Ceph Octopus (15), 更新至 ceph-15.2.17，软件包可用于 Stream 9，Stream 8 和 CentOS 8。这是升级到 ceph-15 的最后一个更新，并且已经赶上了 EOL 上游。
 - NFS-ganesha 4 和 libntirpc 4，没有更新，不过 nfs-ganesha-4.1 和 libntirpc-4.1 的更新马上就要来了。
 - Apache Arrow 在 Stream 9 上更新到了 libarrow-9.0.0，在 Stream 8 上没有更新。
 - Apache ORC 没有更新 liborc.

--------------------------------------------------------------------------------
via: https://blog.centos.org/2022/11/centos-community-newsletter-november-2022/

作者：[CentOS Blog][a]
选题：[Northurland][b]
译者：[fosinoprilsodium](https://github.com/fosinoprilsodium)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org/
[b]: https://github.com/Northurland
[1]: https://connect.centos.org/
[2]: https://wiki.centos.org/SpecialInterestGroup/AltImages
[3]: https://www.centos.org/community/calendar/
[4]: https://www.okd.io/
[5]: https://www.okd.io/blog/2022-10-25-OKD-Streams-Building-the-Next-Generation-of-OKD-together/
[6]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[7]: https://wiki.centos.org/SpecialInterestGroup/Cloud
[8]: https://lists.centos.org/pipermail/centos-devel/2022-November/120679.html
[9]: https://cloud.redhat.com/blog/okd-streams-building-the-next-generation-of-okd-together
[10]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[11]: https://lists.centos.org/pipermail/centos-promo/2022-September/007298.html
[12]: https://www.cossig.org/
[13]: https://connect.centos.org/connect-card-c10.png
