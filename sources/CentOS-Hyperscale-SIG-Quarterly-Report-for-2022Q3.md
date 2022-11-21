[#]: subject: "CentOS Hyperscale SIG Quarterly Report for 2022Q3"
[#]: via: "https://blog.centos.org/2022/10/centos-hyperscale-sig-quarterly-report-for-2022q3/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

2022 CentOS 超大规模技术小组的第三季度报告
======

这个报告涵盖了七月五号到九月三十号的工作。关于先前报告可以查看[2022第二季度报告][1]。

## 目的
---
[超大规模小组][2]关注于开启 Centos Stream 部署在大规模基建，和促进在安装包和工具上的合作。

## 成员更新
---
自上次更新以来，有两名新成员加入小组，Quentin Deslandes 和 Richard Phibel。

我们一直欢迎任何对此特别兴趣小组感兴趣，并愿意为此工作的人的加入和贡献。可以在维基上查看[会员][3]板块了解现有成员以及如何加入。

## 发布和安装包
---
除特别说明外，安装包可在主仓库获取，可用`dnf install centos-hyperscale-release` 命令来启用。任何有关这些安装包的议题可以在我们的 [package-bugs][4]  追踪器上提交议题。

### 文档
---
我们已持续丰富我们的用户文档网站，最近完成了一个希望能更容易发现和使用内容的重大重构。最近的更新也包括增加和修改围绕[打包][6]和[内核][7]上的小组贡献的文档，重写了我们[分支的政策][8]，和一个新的交流板块，以及围绕我们的[频道][9]的细节，可以在此接触到小组和我们的[直播][10]。

像之前所说，我们非常欢迎任何你可能对文档的反馈和[贡献][11]，可以参阅此文档。

### systemd 
---
超大规模小组的最新 systemd 的版本，在 CentOS stream 8 和 CentOS Stream 9 上的是  251.4。虽然 “hs+fb” 版本已经被标记，并在 Meta 内部推出，我们仍在解决 SELinux 在 “hs” 版本发布和标记前的政策的议题。同时 “hs” 版本可以通过<ruby>社区建构系统<rt>cbs</rt></ruby>获取进行测试。

如果你想了解更多有关我们如何在 Hyperscale 小组中推广 systemd 的话，我们在去年八月的 Centos Dojo 做了一个相关的[演说][12]。你可以在下方会议回顾链接中，获取更多这个季度我们的其他 systemd 相关的会议活动。

### 内核
---
我们发布了一个 el8 内核的新版本，其中包括了 perf 包[漏洞修补][13]，在这之前不能安装。

### 容器镜像
---
我们的容器构建管道现在是完全自动化的。容器镜像正构建在 Centos Open Shift CI/CD 基建上，每周会在 Quay 上发布。

### Spin images
---
Neal 为在 Centos Stream 9 上的 Hyperscale Workstation，Cloud 和 Vargrant 镜像使用 KIWI，一直以来在为镜像构建描述而努力。为支持这个工作，我们和 CentOS 基建一起，获得了使用 KIWI 构建镜像部署在社区构建系统上的支持，现在我们正在测试这个。现在已上线了，尽管现在我们不能通过这个构建发布镜像，因为社区构建系统假设所有发布是 RPM 内容。

### 安装包更新
---
我们基于现有的 Fedora 打包，已经发布了更新过的向后移植在 CentOS Stream 8 上 `wireshark` 和在 CentOS stream 8 和 9 `fio` 。我们也同样更新了`ethtool` 为 CentOS Stream 9 到 5.16 的向后移植。

作为在 EPEL 上打包 QMENU  [进行中的工作 ][16]，我们已经开始在一个超大规模后向移植上开发，让其迭代更简单。作为先前条件，我们在测试的仓库上发布了一个最新的向后移植的 `meson`， `edk2` 和 `SLOF` 。我们也已经申请增加 `edk2` 和 `SLOF` 到 CRB（译者注：[CodeReady Linux Builder][https://developers.redhat.com/blog/2018/11/15/introducing-codeready-linux-builder]）和上游的 Fedora QEMU 打包进行一些构建修复。

### DNF/RPM栈上的Copy-on-write 模式支持
---
The [Copy-on-Write][17] stack was rebuilt on top of the latest upstream changes. We’ve also identified an incompatibility between CoW and some external packages from Microsoft that slightly deviate from the RPM specifications. As a result, we have improved our tooling robustness, and are engaging with Microsoft to get their packages fixed.
Copy-on-Write栈在最新的上游变化中重构建。我们也发现了，Copy-on-Write与其他外来自微软的安装包的不兼容，这偏离了RPM要求。因此我们已经改进了我们工作的鲁棒性，会和微软一起，修复他们的安装包。


## 健康和活动
---
小组保持着健康发展的节奏。

### 会议
---
小组举行定期每[两周会议][18]将在在周三，UTC 时间 16：00。会议会被记录，过去的会议备忘录可以在[此][19]获取。

小组会使用 [`#centos-hyperscale`][20]  IRC 频道进行临时通信 协调工作，这个频道也在 Matrix 上的 [`#centos-hyperscale:fedoraproject.org`][21] 房间。任何异步的讨论和通知，我们通常用 [centos-devel][22] 邮件列表。小组也举行开放[每个月视频会议][23]来促进合作和社会交互。

### 会议谈话
---
会议谈话，我们已经发布了一个在 [CentOS Blog][25] 上过去几个月的[会议活动][24]的回顾。提醒一下，我们同样有一页记录可获取的我们的[会议演讲][26]附带录屏和ppt的链接。

一批小组成员预计参加 2023 二月的 [FOSDEM][27]。

### 直播
---
小组定期会在 Twitch [官方频道][28]上直播。有兴趣的人想要在我们工作的时候看直播或者和我们互动的，应该在Twitch上关注我们来获取我们直播时间的通知。

### Planned work 未来的工作
---
The SIG tracks pending work as issues on our [Pagure repository][29]. Notable projects currently in flight include:
小组追踪了待完成的任务作为在我们的 [Pagure repository][29] 议题。
现在正在进行中的是引人注意的项目是：
- 使用社区构建系统构建我们的spin images 
- 推送更新过的在 EPEL 上 QEMU 安装包
- 整合 btrfs 事务更新作为可选的特性

## 理事会的议题
---
我们这次没有议题需理事会关注。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/10/centos-hyperscale-sig-quarterly-report-for-2022q3/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[RakerZh](https://github.com/RakerZh)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[2]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale
[3]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale#Membership
[4]: https://pagure.io/centos-sig-hyperscale/package-bugs
[5]: https://sigs.centos.org/hyperscale/
[6]: https://sigs.centos.org/hyperscale/contributing/packaging/
[7]: https://sigs.centos.org/hyperscale/contributing/kernel/
[8]: https://sigs.centos.org/hyperscale/policies/branches/
[9]: https://sigs.centos.org/hyperscale/communication/channels/
[10]: https://sigs.centos.org/hyperscale/communication/streams/
[11]: https://sigs.centos.org/hyperscale/internal/documentation/
[12]: https://www.youtube.com/watch?v=PdbyYqrvlnY
[13]: https://pagure.io/centos-sig-hyperscale/package-bugs/issue/18
[14]: https://osinside.github.io/kiwi/
[15]: https://pagure.io/centos-infra/issue/696
[16]: https://pagure.io/centos-sig-hyperscale/sig/issue/67
[17]: https://fedoraproject.org/wiki/Changes/RPMCoW
[18]: https://www.centos.org/community/calendar/#hyperscale-sig
[19]: https://sigs.centos.org/hyperscale/internal/meetings/
[20]: https://wiki.centos.org/irc#A.23centos-hyperscale
[21]: https://matrix.to/#/#centos-hyperscale:fedoraproject.org
[22]: https://lists.centos.org/mailman/listinfo/centos-devel
[23]: https://www.centos.org/community/calendar/#hyperscale-sig-monthly-hangout
[24]: https://blog.centos.org/2022/09/centos-hyperscale-sig-conference-recap/
[25]: https://blog.centos.org
[26]: https://sigs.centos.org/hyperscale/communication/talks/
[27]: https://fosdem.org/2023/
[28]: https://www.twitch.tv/centoshyperscale
[29]: https://pagure.io/centos-sig-hyperscale/sig/issues
