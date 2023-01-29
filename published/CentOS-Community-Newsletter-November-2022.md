[#]: subject: "November 2022 Newsletter"
[#]: via: "https://blog.centos.org/2022/11/centos-community-newsletter-november-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "Northurland"
[#]: translator: "fosinoprilsodium"
[#]: reviewer: "Northurland"
[#]: publisher: ""
[#]: url: ""

November 2022 Newsletter
======

## 项目新闻

![CentOS Connect][13]

[CentOS Connect][1] 已经被正式加入了 FOSDEM 外围活动列表中。这场不需入场费的活动将在 2023 年 2 月 3 日，也就是 FOSDEM 大会正式举办的前一天进行。如果你有意参加 FOSDEM，你也可以参与 CentOS Connect，在活动中你能更深入地了解 CentOS，并和开发它的人相互联系。

### <ruby>替代镜像小组<rt>Alternate Images SIG</rt></ruby>

[替代镜像小组][2] 正式地成为了提供额外的操作系统镜像的兴趣小组，提供的内容包括操作系统的可移动介质版以及其他替代形式的安装。他们的[会议][3]每周四 UTC 19 时在 #centos-meeting IRC 频道里举行。

### OKD Streams

[OKD][4]项目[宣布了 OKD Streams][5]，也就是适用于新上线的 CentOS Core OS 的、稳定的 OKD 版本。OKD 是 Kubernetes 的一个社区发行版，红帽的 OpenShift 项目就依赖于它。

## SIG 报告

每月，我们都会发布一次从我们的[特别兴趣小组][6]里轮流选出的季度报告。这个月的报告包括了来自 <ruby>云<rt>Cloud</rt></ruby>，<ruby>宣传<rt>Promo</rt></ruby> 和 <ruby>存储<rt>Storage</rt></ruby> 这三个小组的。

### [云（Cloud）][7]

### 目标

打包和维护多个基于<ruby>自由且开源的软件<rt>Free and Open Source Software</rt></ruby>（FOSS）的私有云基础设施应用，大家可以在 CentOS 上原生安装和运行它们。

https://wiki.centos.org/SpecialInterestGroup/Cloud

### 成员更新

继续协助 OKD 和 SCOS 融入社区。OKD 的维护者 Christian Glombek 会填补空缺的 Cloud SIG 联合主席职位。

在上一个季度发布了新版本的项目：<br/>
（如果提到的项目在上季度里没有发布记录，这里会写出最近一次进行发布的记录）

[Cloud SIG 发布了基于上游 OpenStack Zed 的新版本 RDO Zed。][8]

OKD 工作小组与 Cloud SIG 合作，发布了第一个 OKD/SCOS（适用于 CentOS Stream CoreOS 的 OKD）的<ruby>MVP<rt>最小化可行产品</rt></ruby>。

### 健康度和活跃度

Cloud SIG 的健康保持得相当不错，并且也在积极寻求其他项目的加入以扩展它的受众。

### [宣传（Promo）](https://wiki.centos.org/SpecialInterestGroup/Promo)

八月，我们举办了 [DevConf.US 上的 CentOS Dojo 活动][10]。这是我们疫情后首次回归线下活动，但也可以线上参与。总得来说这次活动进行得不错，并且还有巨大的发展潜力。[完整的活动报告][11]在这里。

我们一直在为 [FOSDEM 会场的 CentOS Connect][1]这个活动工作着，CentOS Connect 是原 CentOS Dojo 活动的新名字。过去，我们在 FOSDEM 上举办的 CentOS Dojo 活动一直是所有 Dojo 活动中规模最大的。计划中，本次活动为时一天，可以允许 100 人左右到场。这仍然比疫情前的要更短小精悍一些。

最后值得一提的是，[一个来自中国的小组][12]（就是我们 COSSIG - 校对者注）正式加入了 Promo 兴趣小组以便进行区域性和本地化的推广和宣传。我们对他们正在进行的工作感到很兴奋，并且我们希望这为将来更多区域性的宣传活动铺平道路。

### [存储（Storage）](https://wiki.centos.org/SpecialInterestGroup/Storage)

自上次报告以来，下列软件包进行了更新：

 - Glusterfs 10 更新至 glusterfs-10.3，软件包可用于 Stream 9 和 Stream 8。
 - Glusterfs 9，更新至 glusterfs-9.6，软件包可用于 Stream 9，Stream 8 和 CentOS 7。
 - Ceph Quincy (17) 更新至 ceph-17.2.5，软件包可用于 Stream 9 和 Stream 8。
 - Ceph Pacific (16) 没有更新，但是 ceph-16.2.11 很快就要来了。
 - Ceph Octopus (15), 更新至 ceph-15.2.17，软件包可用于 Stream 9，Stream 8 和 CentOS 8。这是 ceph-15 的最后一次版本更新，其本身当前已经被停止支持。
 - NFS-ganesha 4 和 libntirpc 4，没有更新，不过 nfs-ganesha-4.1 和 libntirpc-4.1 的更新马上就要来了。
 - Apache Arrow 在 Stream 9 上更新到了 libarrow-9.0.0，在 Stream 8 上没有更新。
 - Apache ORC：liborc 没有更新.

--------------------------------------------------------------------------------
via: https://blog.centos.org/2022/11/centos-community-newsletter-november-2022/

作者：[CentOS Blog][a]
选题：[Northurland][b]
译者：[fosinoprilsodium](https://github.com/fosinoprilsodium)
校对：[Northurland](https://github.com/Northurland)

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
