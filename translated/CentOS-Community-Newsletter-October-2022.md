[#]: subject: "CentOS Community Newsletter, October 2022"
[#]: via: "https://blog.centos.org/2022/10/centos-community-newsletter-october-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "RakerZh"
[#]: reviewer: "acyanbird"
[#]: publisher: " "
[#]: url: " "

CentOS 2022 十月社区简报
======

## 项目资讯

### EPEL 8 的模块化 

EPEL 团队将在 EPEL 8 中[弃用模块化安装包][1]，<ruby>模块<rt>Modules</rt></ruby>是在 RHEL 8 时引入的，但是已经被决定弃用， EPEL 9 中将不会再支持<ruby>模块<rt>Modules</rt></ruby>。

（校对注：已于 2022 年 10 月 31 日正式淘汰）


### Keylime 的变化

Keylime 团队已经宣布，新版本的  `keylime`  和  `keylime-agent-rust` 将会进行[配置文件的重大更新][2]。这些改动是为了让配置文件对于用户更加简单易懂，使未来的升级更加方便。

（校对注：newsletter 原文过于令人困惑，想要获取更多信息请直接查阅 keylime 团队的邮件）

## <ruby>特别兴趣小组<rt>SIG</rt></ruby>报告

每个月，我们会轮流发布来自<ruby>[特别兴趣小组][3]<rt>SIG</rt></ruby>季度报告。这个月包括来自<ruby>汽车<rt>Automotive</rt></ruby>，Hyperscale 和 Kmods 小组的报告


### <ruby>汽车小组<rt>Automotive SIG</rt></ruby> 

<ruby>汽车小组<rt>Automotive SIG</rt></ruby>已经在[邮件列表][4]中发布了他们的季度报告。

### Hyperscale 小组

Hyperscale 小组已经在 [CentOS 博客][5]中发布了他们的季度报告。

### Kmods 小组

此次报告涵盖了自上次报告之后的工作内容。之前的报告可以在[这里][6]查看。

#### 目标

打包和维护 Centos Stream 和 企业版 Linux 内核模块。

#### 成员更新

目前没有成员更新。我们一直欢迎任何对此<ruby>特别兴趣小组<rt>SIG</rt></ruby>感兴趣，并愿意为此工作的人的加入和贡献。

####  CentOS Stream 9 / EL9 支持

Kmods 小组提供可用于 CentOS Stream 9 and EL9 上的安装包


####  CentOS Stream 8 / EL8 支持

Kmods 小组将继续提供可用于 CentOS Stream 8 and EL8 上的安装包


#### 新的安装包

查看 [Kmods 小组的文档][7]获取可用的安装包列表。这个文档也提供了更多信息，例如如何启用 Kmods 小组仓库。

注意：Kmods 小组提供的内核模块现在并没有包含私钥签名，所以请在使用任何内核模块之前，禁用<ruby>安全启动<rt>Secure Boot</rt></ruby>。

请在对应的项目里 [gitlab.com/CentOS/kmods][8] 报告有关这些安装包的问题，或者在[这里][9]报告与特定安装包无关的问题。

#### 近期活动

Kmods 小组已经将所有代码转移到 [gitlab.com/CentOS/kmods][8]。其中包括了使用 GitLab CI 的自动化工具，它可以自动检测因为 kABI 变化，需要重新构建的内核模块。

感谢 CentOS <ruby>基础技术团队<rt>Infrastructure team</rt></ruby>的工作。现在 Kmods 或其他兴趣小组发布的内核模块，将会自动化创建<ruby>磁盘驱动程序<rt>Driver Disk</rt></ruby>。


#### 健康和活动

Kmods 小组保持着健康发展的节奏。

#### 通讯

定期会议将在每个月第一周周一，UTC 时间 16：00 在 #centos-meeting 召开。欢迎大家加入！你也可以随时在 #centos-kmods 与小组成员联系。

#### 公开的议题

- 内核模块签名：这需要与<ruby>基础技术小组<rt>Infra SIG</rt></ruby>进一步的讨论和合作。特别是如何安全存储<ruby>特别兴趣小组<rt>SIG</rt></ruby>用于<ruby>社区构建服务<rt>CBS</rt></ruby> (Community Building Service) 的私钥，并保证不被任何无授权者访问。
- EL 包的发布：小组愿提供可用于 RHEL，或者其他分支下运行的安装包。从而使用户能够轻松的获取并使用本小组发布的安装包。现在的进展可以通过[这里][10]来追踪。

#### 理事会的议题

我们这次没有新的议题需理事会关注。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/10/centos-community-newsletter-october-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[RakerZh](https://github.com/RakerZh)
校对：[acyanbird](https://github.com/acyanbird)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://lists.centos.org/pipermail/centos-devel/2022-September/120610.html
[2]: https://lists.centos.org/pipermail/centos-devel/2022-September/120609.html
[3]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[4]: https://lists.centos.org/pipermail/centos-devel/2022-September/120617.html
[5]: https://blog.centos.org/2022/10/centos-hyperscale-sig-quarterly-report-for-2022q3/
[6]: https://blog.centos.org/2022/07/centos-community-newsletter-july-2022/
[7]: https://sigs.centos.org/kmods/
[8]: https://gitlab.com/CentOS/kmods
[9]: https://gitlab.com/CentOS/kmods/sig
[10]: https://pagure.io/centos-infra/issue/643
