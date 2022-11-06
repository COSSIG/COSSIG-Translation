[#]: subject: "CentOS Community Newsletter, October 2022"
[#]: via: "https://blog.centos.org/2022/10/centos-community-newsletter-october-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS 2022 十月社区简报
======

## 项目资讯

### EPEL 8 的模块化 

EPEL团队在 EPEL 8 [正在弃用安装包模块化][1]，模块是在 RHEL 8 时引入的，但是已经被逐渐弃用， EPEL9 中 不会再支持。


### Keylime 的变化

Keylime 团队已经宣布新版本的  `keylime`  和  `keylime-agent-rust` 将会有[配置文件的重大更新][2]。 这些升级是为了简化未来的更新，以及让其与<ruby>传输层安全性协议<rt>TLS</rt></ruby>的配置更加一致。

## <ruby>特别兴趣小组<rt>SIG</rt></ruby>报告

每个月，我们会轮流发布 来自<ruby>[特别兴趣小组][3]<rt>SIG</rt></ruby>季度报告。 这个月包括来自<ruby>汽车<rt>Automotive</rt></ruby>，Hyperscale 和Kmods 小组的报告


### <ruby>汽车小组<rt>Automotive SIG</rt></ruby> 

<ruby>汽车小组<rt>Automotive SIG</rt></ruby>已经发布了他们的季度报告在  [邮件列表][4]。

### Hyperscale 小组

Hyperscale 小组已经发布了他们的季度报告在  [Centos 博客][5]。

### Kmods 小组

这篇报告涵盖了自上次报告起的工作内容。之前的报告在 [这里][6]。

#### 目标

打包和维护 Centos Stream 和 企业版 Linux 内核模块。

#### 成员更新

目前没有成员更新。我们一直欢迎任何对<ruby>特别兴趣小组<rt>SIG</rt></ruby>感兴趣并愿意工作的人的加入和贡献。

####  CentOS Stream 9 / EL9 支持

Kmods 小组 提供了 CentOS Stream 9 and EL9 上的安装包


####  CentOS Stream 8 / EL8 支持

Kmods 小组 继续提供了 CentOS Stream 8 and EL8 上的安装包


#### 新的安装包

查看 [Kmods 小组的文档][7] 上架的安装包列表。这个文档也提供了更多信息，例如如何启用 Kmods 小组仓库。

注意 Kmods 小组提供的内核模块现在并没有私钥签名，所以要禁用<ruby>安全启动<rt>Secure Boot</rt></ruby>使用任何内核模块重的一个。

请在对应的项目里 [gitlab.com/CentOS/kmods][8] 报告任何有关这些包的问题 ，或者在 [这里][9] 报告与特定安装包无关的问题。

#### 近期活动

Kmods 小组已经将所有代码转移到 [gitlab.com/CentOS/kmods][8]。这包括了所有自动检测因 kABI 的变动所需内核模块重建的全部工具 。我们凭借着 GitLab CI 做这些任务。

感谢 Centos<ruby>基础技术团队<rt>Infrastructure team</rt></ruby>的工作。现在已经有为 Kmods 或其他任何小组发布的内核模块的自动化创建<ruby>磁盘驱动程序<rt>Driver Disk</rt></ruby>。


#### 健康和活动

Kmods 小组保持着健康发展的步伐 

#### 通讯

定期会议计划每个月第一周周一 1600 UTC 时间 ，在 #centos-meeting 。欢迎大家加入！你也可以随时和在 #centos-kmods 与小组成员联系。

#### 公开的议题

- 内核模块签名：这需要与<ruby>基础技术小组<rt>Infra SIG</rt></ruby>合作和进一步的讨论。特别是如何安全存储可以用于<ruby>社区构建服务<rt>CBS</rt></ruby> (Community Building Service) 的 <ruby>特别兴趣小组<rt>SIG</rt></ruby>的钥匙，但是不被任何没有授权的人访问。
- EL 包的发布：小组愿提供发布安装包让用户可以在RHEL，或者其分支下运行，并可以轻松的获取。现在的进展可以通过[这里][10]来获取。

#### 理事会的议题

我们这次没有新的议题需理事会关注。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/10/centos-community-newsletter-october-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[RakerZh](https://github.com/RakerZh)
校对：[校对者ID](https://github.com/校对者ID)

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
