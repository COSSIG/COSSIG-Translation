[#]: subject: "CentOS Community Newsletter, September 2022"
[#]: via: "https://blog.centos.org/2022/09/centos-community-newsletter-september-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "lkxed"
[#]: reviewer: "Northurland"
[#]: publisher: ""
[#]: url: "https://www.cossig.org/530-centos-community-newsletter-september-2022/"

CentOS Community Newsletter, September 2022
======

## 项目新闻

### Tru 退出理事会

Tru Huynh 决定辞去理事会职务。我们感谢他多年来在理事会和整个 CentOS 项目中的辛勤工作。

### Jefro 加入理事会

CentOS 理事会已委任 Jeffrey “Jefro” Osier-Mixon 来填补这个空缺。Jefro 在发展<ruby>[汽车小组][1]<rt>Automotive SIG</rt></ruby>方面发挥了重要作用。

### DevConf 大会上的 Dojo 活动

CentOS 在波士顿 [DevConf.US][3] 大会上举办了一个 [Dojo][2] 活动。这个免费的迷你会议包括了关于企业 Linux 生态系统的各种主题的演讲，共九场。我们还全程直播并回答了远程参与者的问题，我们计划在未来的现场活动中继续这种方式。[活动录音可在 YouTube 上找到][4]。

## 特别兴趣小组（SIG）报告

每个月，我们都会轮流发布来自各个<ruby>[特别兴趣小组][2]<rt>SIG</rt></ruby>的季度报告。本月包括来自<ruby>艺术小组<rt>Artwork SIG</rt></ruby>和<ruby>虚拟化小组<rt>Virtualization SIG</rt></ruby>的报告。

### <ruby>[艺术小组][5a]<rt>Artwork SIG</rt></ruby>

#### 目标

<ruby>CentOS 艺术小组<rt>CentOS Artwork SIG</rt></ruby> 负责 CentOS 项目的视觉设计。请参阅 https://wiki.centos.org/SpecialInterestGroup/Artwork

#### 成员更新

目前没有成员更新。我们一直在寻找新成员～

#### 版本发布

##### CentOS 标志 v2

![CentOS 图标][6]

CentOS 标志 v2 是 CentOS Project 的新<ruby>品牌图标<rt>visual identity</rt></ruby>。我们希望您能积极使用它。它是[最近才通过的][7]，我们也会逐渐过渡到这个新设计。

CentOS 标志 v2 的相关源文件都公开在 [centos-brand][8] 仓库中，这个仓库的目的是：

1. 将 CentOS 标志设计、使用和展示的工作整合到一处。
2. 整合自动化工作，以使 CentOS 标志在不同地方的外观保持一致（例如，通过 GitLab <ruby>管道<rt>pipelines</rt></ruby>，你可以将其包含在你自己的项目中）。

CentOS 标志根据 _[知识共享署名-相同方式共享 4.0 国际公共许可协议][9]_ 的条款发布，其使用受 _[CentOS 商标指南][10]_ 的限制。

之前的标志，也就是 CentOS 标志 v1 还在使用，未来仍将如此，我们会把它称为 <ruby>“CentOS 旧设计”<rt>CentOS Classic</rt></ruby>，而不是 “CentOS”。

#### 健康和活动

##### 健康

组内人员没有出现因健康问题而无法贡献的情况。

##### 近期与网站重新设计相关的活动

![][11]

CentOS 的网站设计在 [jekyll-theme-centos][12] 仓库中进行，这是 [Jekyll][14] 下的 [一个基于 gem 的主题][13]。（译者注：Jekyll 是一个静态页面模板引擎/生成器。）

###### 工具包

我们正在将 jekyll-theme-centos 的开发从 Bootstrap 4 转移到 Bootstrap 5。我们正在减少在 Bootstrap 的默认类上添加的自定义 CSS 类的数量，以便将来更容易地从一个版本过渡到另一个版本。因此，我们也在重写 HTML，让它仅支持 Bootstrap 类，并淘汰所有不支持的类。不过，不支持的类是很少的。

###### 排版

网站中使用的两种字体仍然是 Montserrat 和 Overpass。

###### CentOS 标志可扩展性

<ruby>艺术小组<rt>Artwork SIG</rt></ruby> 的首要任务就是在不同的视觉表现形式下使 CentOS 的品牌观感始终保持一致。我们正在将文件格式从 PNG 更改为 SVG，以解决当 CentOS 标志出现在超高分辨率显示器上时光栅图像质量下降的问题。现代浏览器对 SVG 的支持似乎相当不错。

###### <ruby>页眉<rt>header</rt></ruby>和<ruby>页脚<rt>footer</rt></ruby>的易读性

我们正在淘汰网站<ruby>页眉<rt>header</rt></ruby>和<ruby>页脚<rt>footer</rt></ruby>的艺术主题背景，用纯色代替。当前，它的颜色与 CentOS 标志中使用的颜色相同，以建立与它的视觉联系。页脚和导航栏背景使用较深的颜色来与页眉提供足够的对比度。

更改前：

![][18]

更改后：

![][19]

上一段中提到的艺术主题仍然起到加强不同视觉表现之间联系的作用。因此，它仍然存在于主页中，在 CentOS 发行版屏幕截图中出现。

###### CentOS 发行版

我们正在添加与 CentOS 发行版相关的屏幕截图轮播。这有两个目的：一是将 CentOS 品牌与 CentOS Stream 发行版中默认使用的艺术主题联系起来，二是用图像向世界展示 CentOS Stream 的样子，而不仅仅是文字。

![][20]

###### 新闻、事件和博文

我们正在替换主页标题，从 “Around CentOS” 改为 “Blog posts”。这些部分会被改为水平对齐，而不是垂直对齐。

![][21]

###### CentOS 赞助商

当前，网页中的赞助商板块每隔几秒钟刷新一次，每次展示一张图片。我们正在尝试换用主页末尾的两排滚动图片，每排 6 张图片，其中赞助商图标是从整个活跃赞助商列表中随机加载的。在此布局中，12 个赞助商图标将始终在合理的空间内同时出现，更具视觉吸引力。当下次主页重新加载时，这里会展示另外一组 12 个赞助商，以此类推。

![][22]

截图中使用的图片仅用于测试目的，它们**不代表任何真实的赞助商**。一旦安装了基于 gem 的主题，存储在主题中的赞助商图像将被忽略，而 `assets/img/sponsors/` 使用目录中存储的图像。

“<ruby>成为赞助商<rt>becoming a sponsor</rt></ruby>”链接现在更加明显了。

![][23]

我们将从网站<ruby>页脚<rt>footer</rt></ruby>中移除赞助商部分，以支持网站主页中的赞助商部分。诸如邮件列表之类、需要在<ruby>页脚<rt>footer</rt></ruby>上显示赞助商图像的网站，会继续使用它。

##### 针对理事会的问题

无。

### <ruby>[虚拟化小组][23a]<rt>[Virtualization SIG]</rt><ruby>

在上个季度，上游发布了数个带有二进制文件的版本，这些版本主要通过<ruby> CentOS 虚拟化小组<rt>CentOS Virt SIG</rt></ruby>发行：

- [oVirt 4.5.2][24]
- [oVirt 4.5.1][25]
- [oVirt 4.5.0][26]

我们现在也在为 c9s 构建 kata-containers，最新版本（2.5.0）已经可用。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/09/centos-community-newsletter-september-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[lkxed](https://github.com/lkxed)
校对：[Northurland](https://github.com/Northurland)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/SpecialInterestGroup/Automotive
[2]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[3]: https://www.devconf.info/us/
[4]: https://www.youtube.com/watch?v=5usWZhLnJyA&list=PLuRtbOXpVDjDP1RLkzZmLbp699cCBnn47
[5]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[5a]: https://wiki.centos.org/SpecialInterestGroup/Artwork
[6]: https://gitlab.com/areguera/centos-brand/-/raw/v2/Sources/centos-logo.svg
[7]: https://git.centos.org/centos/board/issue/4#comment-612
[8]: https://gitlab.com/areguera/centos-brand/
[9]: https://creativecommons.org/licenses/by-sa/4.0/legalcode
[10]: https://www.centos.org/legal/trademarks/
[11]: https://i.imgur.com/RRPGRK4.png
[12]: https://gitlab.com/areguera/jekyll-theme-centos/-/tree/migration-to-bootstrap-v5
[13]: https://rubygems.org/gems/jekyll-theme-centos
[14]: https://jekyllrb.com/
[15]: https://areguera.gitlab.io/jekyll-theme-centos/
[16]: https://opensource.org/licenses/MIT
[17]: https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#svg_scalable_vector_graphics
[18]: https://i.imgur.com/jrK4dk1.jpg
[19]: https://i.imgur.com/bQz4828.png
[20]: https://i.imgur.com/J7CWrPo.jpg
[21]: https://i.imgur.com/ydK4Eb2.jpg
[22]: https://i.imgur.com/ScXzGVw.png
[23]: https://i.imgur.com/RqPVH9o.jpg
[23a]: https://wiki.centos.org/SpecialInterestGroup/Virtualization
[24]: https://blogs.ovirt.org/2022/08/ovirt-4-5-2-is-now-generally-available/
[25]: https://blogs.ovirt.org/2022/06/ovirt-4-5-1-is-now-generally-available/
[26]: https://blogs.ovirt.org/2022/04/ovirt-4-5-0-is-now-generally-available/
