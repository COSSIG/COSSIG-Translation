[#]: subject: "CentOS Hyperscale SIG conference recap"
[#]: via: "https://blog.centos.org/2022/09/centos-hyperscale-sig-conference-recap/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "turbokernel"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS 超大型 SIG 会议回顾
======

在过往的几个月中，CentOS 超大型 SIG 的成员当面地出席了几次会议并分享了 SIG 当前的工作，从某种方面来看也是首次。

我们提供了一个网页用于跟踪 [会议报告][1] Hyperscale 的相关话题。您可以在下方找到本次会谈的参考以及相关视频录像（如有）。

本次会议不仅止步于演示。“走廊轨道” 为偶遇创造了绝佳的机会，并为大家了解和了解彼此提供了很好的场所。

如果以后您想以个人身份和我们面基，请[联系][2]。我们也会在[季度报告][3]中罗列出相关会议计划.

## SCaLE 19x

Anita Zhang、Davide Cavalca 和 Neal Gompa 出席了七月底在洛杉矶举办的 [SCaLE 19x][4]。

Anita 发表了两篇关于 systemd 中 Journal 的回归测试的演讲：[内存增长奇案][5] 以及和 Alvaro Leiva Geisse 一起发表了 systemd 及相关功能的介绍 [ systemd的核心之旅][6]。

Davide 发表了 [使用 CentOS Stream 构建未来][7], 介绍了 CentOS 的发展历程以及与 Meta 社区互动的经验。

SCaLE 的会议视频尚未发布，但相关录播可以在 [YouTube][8] 上找到，也可以从我们的 [追踪页][9] 获取相关链接。

## CentOS Dojo 和 DevConf.US 2022

Anita, Davide, David Duncan, Jack Aboutboul, Neal, 和 Quentin Deslandes 在八月出席了 [DevConf.US 2022][10] 和 [CentOS Dojo][11] 活动。

随着 Daan De Meyer 的远程加入, Anita 在 Dojo 中分享了有关在超大型 SIG 中管理和自动化 systemd 发布的议题[超大规模 systemd 探索][12]。在同一场会议中，Davide 分享了关于[超大规模 SIG 更新][13]最新研发进展。

同场 Dojo 会议中，Neal 分享了[使用 KIWI 自定义CentOS镜像][14]，并线上演示了[一个使用KIWI镜像构建数据文件的仓库][15]。在本周晚些时候，Neal 在DevConf.US上，分享了深入镜像构建的相关话题[大规模扩展镜像的最佳方案][16]。

Shaun McChance 同时也代表[Promo SIG][18]发布了此项互动的[报告]。

## 大型面对面会议

在举办Dojo的前一天，我们还举办了首场面对面[超大规模SIG线下会][19]。Anita、Davide、David、Neal和Quentin莅临现场，Shaun也参加并组织了此次会议。尽管此次是线下会议，我们同样也设置了远程分会场支持远程参会，这允许大家关注会议并根据自己的行程自由安排时间。其中，Daan和Manu Bretelle远程参与了此次会议。

我们在会议上有很多有意义的对话，包括了具体的工作项目、对未来工作的头脑风暴以及工作流程的改进。大家都觉得该场会议意义重大，我们计划在未来组织更多类似的会议。

该场会议没有录像，但有关于探讨的[会议记录][20]，会议的待办事项将很快以工单形式发布在我们的[SIG 追踪系统][21]中。

## Linux Plumbers Conference 2022

Anita、Davide、Daan、Manu和Quentin出席了九月在都柏林召开的[Linux Plumbers Conference 2022][22]会议。该场会议同时支持线上，Michel Salim和Neal远程参与了此次会议。

Anita组织了小型会议[服务管理与systemd][23]，并围绕systemd展开了为期一天的相关演讲和讨论。Daan介绍了他在日志优化上的最新进展[日志的瘦身][24].

该场会议同时也安排了相关类型的环节，并且开展针对相关话题讨论。其中，SIG的成员参与了[systemd BoF][25]和[Btrfs BoF][26]。

LPC的会议视频目前尚未发布，但可以在[YouTube][27]上找到会议直播的录制视频，也可以从我们的[追踪页面][28]中找到相关链接。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/09/centos-hyperscale-sig-conference-recap/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[turbokernel](https://github.com/turbokernel)
校对：[Phodopussungorus](https://github.com/Phodopussungorus)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://sigs.centos.org/hyperscale/communication/talks/
[2]: https://sigs.centos.org/hyperscale/communication/channels/
[3]: https://sigs.centos.org/hyperscale/communication/reports/
[4]: https://www.socallinuxexpo.org/scale/19x
[5]: https://www.socallinuxexpo.org/scale/19x/presentations/curious-case-memory-growth
[6]: https://www.socallinuxexpo.org/scale/19x/presentations/journey-heart-systemd
[7]: https://www.socallinuxexpo.org/scale/19x/presentations/building-future-centos-stream
[8]: https://www.youtube.com/user/socallinuxexpo/videos
[9]: https://www.devconf.info/us/
[10]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[11]: https://www.youtube.com/watch?v=PdbyYqrvlnY
[12]: https://www.youtube.com/watch?v=aXO0eLMkCDI
[13]: https://www.youtube.com/watch?v=RKeFR4R2IeA
[14]: https://pagure.io/centos-kiwi-examples
[15]: https://devconfus2022.sched.com/event/14TEW/golden-images-for-scaling-up-with-the-best-of-them
[16]: https://lists.centos.org/pipermail/centos-promo/2022-September/007298.html
[17]: https://wiki.centos.org/SpecialInterestGroup/Promo
[18]: https://lists.centos.org/pipermail/centos-devel/2022-July/120462.html
[19]: https://pagure.io/centos-sig-hyperscale/sig/blob/main/f/meetups/20220816-boston-meetup.md
[20]: https://pagure.io/centos-sig-hyperscale/sig/issues
[21]: https://lpc.events/event/16/
[22]: https://lpc.events/event/16/sessions/146/
[23]: https://lpc.events/event/16/contributions/1185/
[24]: https://lpc.events/event/16/contributions/1399/
[25]: https://lpc.events/event/16/contributions/1300/
[26]: https://www.youtube.com/c/LinuxPlumbersConference/videos
